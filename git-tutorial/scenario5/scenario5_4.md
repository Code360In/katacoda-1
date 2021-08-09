If you think of Git as taking snapshots of changes over the life of a project, `git add` specifies what will go in a snapshot (putting things in the staging area), and `git commit` then actually takes the snapshot, and makes a permanent record of it (as a commit). If you don’t have anything staged when you type `git commit`, Git will prompt you to use `git commit -a` or `git commit --all`, which is kind of like gathering everyone to take a group photo! However, it’s almost always better to explicitly add things to the staging area, because you might commit changes you forgot you made. (Going back to the group photo simile, you might get an extra with incomplete makeup walking on the stage for the picture because you used `-a`!) Try to stage things manually, or you might find yourself searching for “git undo commit” more than you would like!

![picture1](./assets/git-staging-area.svg)

<br/>

Let’s watch as our changes to a file move from our editor to the staging area and into long-term storage. First, we’ll add another line to the file:

> ## Bash
> `nano mars.txt`{{execute}}
> 
> `cat mars.txt`{{execute}}

> ## Output
> ```
> Cold and dry, but everything is my favorite color
> 
> The two moons may be a problem for Wolfman
> 
> But the Mummy will appreciate the lack of humidity
> ```

> ## Bash
> `git diff`{{execute}}

> ## Output
> ```
> diff --git a/mars.txt b/mars.txt
> 
> index 315bf3a..b36abfd 100644
> 
> --- a/mars.txt
> 
> +++ b/mars.txt
> 
> @@ -1,2 +1,3 @@
> 
> Cold and dry, but everything is my favorite color
> 
>  The two moons may be a problem for Wolfman
> 
>  +But the Mummy will appreciate the lack of humidity
> ```

<br/>

So far, so good: we’ve added one line to the end of the file (shown with a `+` in the first column). Now let’s put that change in the staging area and see what `git diff` reports:

> ## Bash
> `git add mars.txt`{{execute}}
> 
> `git diff`{{execute}}

There is no output: as far as Git can tell, there’s no difference between what it’s been asked to save permanently and what’s currently in the directory. However, if we do this:

> ## Bash
> `git diff --staged`{{execute}}

> ## Output
> ```
> diff --git a/mars.txt b/mars.txt
> 
> index 315bf3a..b36abfd 100644
> 
> --- a/mars.txt
> 
> +++ b/mars.txt
> 
> @@ -1,2 +1,3 @@
> 
>  Cold and dry, but everything is my favorite color
>  
>  The two moons may be a problem for Wolfman
>  
> +But the Mummy will appreciate the lack of humidity
> ```

It shows us the difference between the last committed change and what’s in the staging area. Let’s save our changes:

> ## Bash
> `git commit -m "Discuss concerns about Mars' climate for Mummy"`{{execute}}

> ## Output
> ```
> [main 005937f] Discuss concerns about Mars' climate for Mummy
> 
> 1 file changed, 1 insertion(+)
> ```

Check our status:

> ## Bash
> `git status`{{execute}}

> ## Output
> ```
> On branch main
> 
> nothing to commit, working directory clean
> ```

<br/>

and look at the history of what we’ve done so far:

> ## Bash
> `git log`{{execute}}

> ## Output
> ```
> commit 005937fbe2a98fb83f0ade869025dc2636b4dad5
> 
> Author: Vlad Dracula <vlad@tran.sylvan.ia>
> 
> Date:   Thu Aug 22 10:14:07 2013 -0400
> 
>     Discuss concerns about Mars' climate for Mummy
>     
> commit 34961b159c27df3b475cfe4415d94a6d1fcd064d
> 
> Author: Vlad Dracula <vlad@tran.sylvan.ia>
> 
> Date:   Thu Aug 22 10:07:21 2013 -0400
> 
>     Add concerns about effects of Mars' moons on Wolfman
>     
> commit f22b25e3233b4645dabd0d81e651fe074bd8e73b
> 
> Author: Vlad Dracula <vlad@tran.sylvan.ia>
> 
> Date:   Thu Aug 22 09:51:46 2013 -0400  
>   
>     Start notes on Mars as a base
> ```

# Word-based diffing
Sometimes, e.g. in the case of the text documents a line-wise diff is too coarse. That is where the `--color-words` option of `git diff` comes in very useful as it highlights the changed words using colors.

<br/>


