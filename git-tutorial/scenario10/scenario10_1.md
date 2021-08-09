As soon as people can work in parallel, they’ll likely step on each other’s toes. This will even happen with a single person: if we are working on a piece of software on both our laptop and a server in the lab, we could make different changes to each copy. Version control helps us manage these conflicts by giving us tools to [resolve](https://swcarpentry.github.io/git-novice/reference.html#resolve) overlapping changes.

To see how we can resolve conflicts, we must first create one. The file `mars.txt` currently looks like this in both partners’ copies of our `planets` repository:
> `cat mars.txt`{{execute}}

Which the content is as follow:
> ```
> Cold and dry, but everything is my favorite color
> The two moons may be a problem for Wolfman
> But the Mummy will appreciate the lack of humidity
> ```

Let’s add a line `This line added to Wolfman's copy`{{copy}} to the collaborator’s copy only:
> `nano mars.txt`{{execute}}

and then push the change to GitHub:
> ```
> git add mars.txt
> git commit -m "Add a line in our home copy"
> git push origin main
> ```{{execute}}

Now let’s have the owner make a different change to their copy <i> without </i> updating from GitHub `We added a different line in the other copy`{{copy}}:
> `nano mars.txt`{{execute}}

We can commit the change locally:
> ```
> git add mars.txt
> git commit -m "Add a line in my copy
> ```{{execute}}

but Git won’t let us push it to GitHub:
> `git push origin main`{{execute}}

With the output content
> ```
> To https://github.com/vlad/planets.git
>  ! [rejected]        main -> main (fetch first)
> error: failed to push some refs to 'https://github.com/vlad/planets.git'
> hint: Updates were rejected because the remote contains work that you do
> hint: not have locally. This is usually caused by another repository pushing
> hint: to the same ref. You may want to first integrate the remote changes
> hint: (e.g., 'git pull ...') before pushing again.
> hint: See the 'Note about fast-forwards' in 'git push --help' for details.
> ```

![Picture1](./assets/conflict.svg)

Git rejects the push because it detects that the remote repository has new updates that have not been incorporated into the local branch. What we have to do is pull the changes from GitHub, [merge](https://swcarpentry.github.io/git-novice/reference.html#merge) them into the copy we’re currently working in, and then push that. Let’s start by pulling:
> `git pull origin main`{{execute}}

The `git pull` command updates the local repository to include those changes already included in the remote repository. After the changes from remote branch have been fetched, Git detects that changes made to the local copy overlap with those made to the remote repository, and therefore refuses to merge the two versions to stop us from trampling on our previous work. The conflict is marked in in the affected file:
> `cat mars.txt`{{execute}}

The output will show which line is added by a certain collaborator:
> ```
> Cold and dry, but everything is my favorite color
> The two moons may be a problem for Wolfman
> But the Mummy will appreciate the lack of humidity
> <<<<<<< HEAD
> We added a different line in the other copy
> =======
> This line added to Wolfman's copy
> >>>>>>> dabb4c8c450e8475aee9b14b4383acc99f42af1d
> ```

Our change is preceded by `<<<<<<< HEAD`. Git has then inserted `=======` as a separator between the conflicting changes and marked the end of the content downloaded from GitHub with `>>>>>>>`. (The string of letters and digits after that marker identifies the commit we’ve just downloaded.)

It is now up to us to edit this file to remove these markers and reconcile the changes. We can do anything we want: keep the change made in the local repository, keep the change made in the remote repository, write something new to replace both, or get rid of the change entirely. Let’s replace both so that the file looks like this:
> ```
> Cold and dry, but everything is my favorite color
> The two moons may be a problem for Wolfman
> But the Mummy will appreciate the lack of humidity
> We removed the conflict on this line
> ```{{copy}}

To finish merging, we add `mars.txt` to the changes being made by the merge and then commit:
> ```
> git add mars.txt
> git status
> git commit -m "Merge changes from GitHub"
> ```{{execute}}

Now we can push our changes to GitHub:
> `git push origin main`{{execute}}
Showing the following output:
> ```
> Enumerating objects: 10, done.
> Counting objects: 100% (10/10), done.
> Delta compression using up to 8 threads
> Compressing objects: 100% (6/6), done.
> Writing objects: 100% (6/6), 645 bytes | 645.00 KiB/s, done.
> Total 6 (delta 4), reused 0 (delta 0)
> remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
> To https://github.com/vlad/planets.git
>    dabb4c8..2abf2b1  main -> main
> ```

Git keeps track of what we’ve merged with what, so we don’t have to fix things by hand again when the collaborator who made the first change pulls again:
> `git pull origin main`{{execute}}
With the following output:
> ```
> remote: Enumerating objects: 10, done.
> remote: Counting objects: 100% (10/10), done.
> remote: Compressing objects: 100% (2/2), done.
> remote: Total 6 (delta 4), reused 6 (delta 4), pack-reused 0
> Unpacking objects: 100% (6/6), done.
> From https://github.com/vlad/planets
>  * branch            main     -> FETCH_HEAD
>     dabb4c8..2abf2b1  main     -> origin/main
> Updating dabb4c8..2abf2b1
> Fast-forward
>  mars.txt | 2 +-
>  1 file changed, 1 insertion(+), 1 deletion(-)
>  ```
>  

We get the merged file:
> ```
> Cold and dry, but everything is my favorite color
> The two moons may be a problem for Wolfman
> But the Mummy will appreciate the lack of humidity
> We removed the conflict on this line
> ```

We don’t need to merge again because Git knows someone has already done that.

Git’s ability to resolve conflicts is very useful, but conflict resolution costs time and effort, and can introduce errors if conflicts are not resolved correctly. If you find yourself resolving a lot of conflicts in a project, consider these technical approaches to reducing them:
- Pull from upstream more frequently, especially before starting new work
- Use topic branches to segregate work, merging to main when complete
- Make smaller more atomic commits
- Where logically appropriate, break large files into smaller ones so that it is less likely that two authors will alter the same file simultaneously

Conflicts can also be minimized with project management strategies:
- Clarify who is responsible for what areas with your collaborators
- Discuss what order tasks should be carried out in with your collaborators so that tasks expected to change the same lines won’t be worked on simultaneously
- If the conflicts are stylistic churn (e.g. tabs vs. spaces), establish a project convention that is governing and use code style tools (e.g. `htmltidy`, `perltidy`, rubocop, etc.) to enforce, if necessary

---------

## Solving Conflicts that You Create
Clone the repository created by your instructor. Add a new file to it, and modify an existing file (your instructor will tell you which one). When asked by your instructor, pull her changes from the repository to create a conflict, then resolve it.

---------

## Key Points
- Conflicts occur when two or more people change the same lines of the same file.
- The version control system does not allow people to overwrite each other’s changes blindly, but highlights conflicts so that they can be resolved.

<br/>






