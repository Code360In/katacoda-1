[Good commit messages](https://chris.beams.io/posts/git-commit/) start with a brief (<50 characters) statement about the changes made in the commit. Generally, the message should complete the sentence “If applied, this commit will” . If you want to go into more detail, add a blank line between the summary line and your additional notes. Use this additional space to explain why you made changes and/or what their impact will be.

If we run `git status` now:

> ## Bash
> `git status`{{execute}}

> ## Output
> On branch main
> 
> nothing to commit, working directory clean

it tells us everything is up to date. If we want to know what we’ve done recently, we can ask Git to show us the project’s history using `git log`:

> ## Bash 
> `git log`{{execute}}

> ## Output
> commit f22b25e3233b4645dabd0d81e651fe074bd8e73b
> 
> Author: Vlad Dracula <vlad@tran.sylvan.ia>
> 
> Date:   Thu Aug 22 09:51:46 2013 -0400
> 
>     Start notes on Mars as a base

`git log` lists all commits made to a repository in reverse chronological order. The listing for each commit includes the commit’s full identifier (which starts with the same characters as the short identifier printed by the `git commit` command earlier), the commit’s author, when it was created, and the log message Git was given when the commit was created.

# Where Are My Changes?

If we run `ls` at this point, we will still see just one file called `mars.txt`. That’s because Git saves information about files’ history in the special `.git` directory mentioned earlier so that our filesystem doesn’t become cluttered (and so that we can’t accidentally edit or delete an old version

<br/><br/>



