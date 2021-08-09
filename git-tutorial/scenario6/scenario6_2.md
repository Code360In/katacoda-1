Above we used:
> `git checkout f22b25e mars.txt`

to revert `mars.txt` to its state after the commit `f22b25e`. But be careful! The command `checkout` has other important functionalities and Git will misunderstand your intentions if you are not accurate with the typing. For example, if you forget `mars.txt` in the previous command.

> `git checkout f22b25e`{{execute}} (remember to change ID)

It will output a paragraph with a detached HEAD. 
> ```
> Note: checking out 'f22b25e'.
> 
> You are in 'detached HEAD' state. You can look around, make experimental changes and commit them, and you can discard any commits you make in this state without impacting any branches by performing another checkout.
> 
> If you want to create a new branch to retain commits you create, you may do so (now or later) by using -b with the checkout command again. Example:
> 
> git checkout -b <new-branch-name>
> 
> HEAD is now at f22b25e Create a new file
> ```
  
The “detached HEAD” is like “look, but don’t touch” here, so you shouldn’t make any changes in this state. After investigating your repo’s past state, reattach your `HEAD` with git checkout main.

It’s important to remember that we must use the commit number that identifies the state of the repository before the change we’re trying to undo. A common mistake is to use the number of the commit in which we made the change we’re trying to discard. In the example below, we want to retrieve the state from before the most recent commit (HEAD~1), which is commit f22b25e:
  
![picture1](./assets/git-checkout.svg)
  
So, to put it all together, here’s how Git works in cartoon form:
![picture2](./assets/git_staging.svg)
  
## Simplifying the Common Case
If you read the output of `git status` carefully, you’ll see that it includes this hint:
  `(use "git checkout -- <file>..." to discard changes in working directory)`

As it says, `git checkout` without a version identifier restores files to the state saved in `HEAD`. The double dash `--` is needed to separate the names of the files being recovered from the command itself: without it, Git would try to use the name of the file as the commit identifier.
  
<br/>
  
The fact that files can be reverted one by one tends to change the way people organize their work. If everything is in one large document, it’s hard (but not impossible) to undo changes to the introduction without also undoing changes made later to the conclusion. If the introduction and conclusion are stored in separate files, on the other hand, moving backward and forward in time becomes much easier.

## Key Points
- `git diff` displays differences between commits.
- `git checkout` recovers old versions of files.
  
  
