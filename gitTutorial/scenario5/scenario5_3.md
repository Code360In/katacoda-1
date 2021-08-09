Now suppose Dracula adds more information to the file. (Again, we’ll edit with `nano` and then `cat` the file to show its contents; you may use a different editor, and don’t need to `cat`.)

> ## Bash
> `nano mars.txt`{{execute}}
> 
> `cat mars.txt`{{execute}}

> ## Output
> Cold and dry, but everything is my favorite color
> 
> The two moons may be a problem for Wolfman

When we run `git status` now, it tells us that a file it already knows about has been modified:

> ## Bash 
> `git status`{{execute}}

> ## Output
> ```
> On branch main
> 
> Changes not staged for commit:
> 
>   (use "git add <file>..." to update what will be committed)
> 
>   (use "git checkout -- <file>..." to discard changes in working directory)
>  
>        modified:   mars.txt
> 
> no changes added to commit (use "git add" and/or "git commit -a")
> ```
  
The last line is the key phrase: “no changes added to commit”. We have changed this file, but we haven’t told Git we will want to save those changes (which we do with `git add`) nor have we saved them (which we do with `git commit`). So let’s do that now. It is good practice to always review our changes before saving them. We do this using `git diff`. This shows us the differences between the current state of the file and the most recently saved version:

> ## Bash
> `git diff`{{execute}}
  
> ## Output
> ```
> diff --git a/mars.txt b/mars.txt
> 
> index df0654a..315bf3a 100644
>
> --- a/mars.txt
> 
> +++ b/mars.txt
>  
> @@ -1 +1,2 @@
> 
> Cold and dry, but everything is my favorite color
>
> +The two moons may be a problem for Wolfman
> ```

<br/>
  
The output is cryptic because it is actually a series of commands for tools like editors and `patch` telling them how to reconstruct one file given the other. If we break it down into pieces:

1. The first line tells us that Git is producing output similar to the Unix diff command comparing the old and new versions of the file.
2. The second line tells exactly which versions of the file Git is comparing; df0654a and 315bf3a are unique computer-generated labels for those versions.
3. The third and fourth lines once again show the name of the file being changed.
4. The remaining lines are the most interesting, they show us the actual differences and the lines on which they occur. In particular, the + marker in the first column shows where we added a line.

After reviewing our change, it’s time to commit it:
  
> ## Bash
> `git commit -m "Add concerns about effects of Mars' moons on Wolfman"`{{execute}}

> ## Output
> ```
> On branch main
> 
> Changes not staged for commit:
>
>   (use "git add <file>..." to update what will be committed)
>   (use "git checkout -- <file>..." to discard changes in working directory)
>  
> 	      modified:   mars.txt
> 
> no changes added to commit (use "git add" and/or "git commit -a")
> ```
  
<br/>
  
Whoops: Git won’t commit because we didn’t use `git add` first. Let’s fix that:

> ## Bash
> `git add mars.txt`{{execute}}
> `git commit -m "Add concerns about effects of Mars' moons on Wolfman"`{{execute}}

> ## Output
> ```
> [main 34961b1] Add concerns about effects of Mars' moons on Wolfman
>
> 1 file changed, 1 insertion(+)
> ```

<br/>

Git insists that we add files to the set we want to commit before actually committing anything. This allows us to commit our changes in stages and capture changes in logical portions rather than only large batches. For example, suppose we’re adding a few citations to relevant research to our thesis. We might want to commit those additions, and the corresponding bibliography entries, but not commit some of our work drafting the conclusion (which we haven’t finished yet).

To allow for this, Git has a special staging area where it keeps track of things that have been added to the current [changeset](https://swcarpentry.github.io/git-novice/reference.html#changeset) but not yet committed.

<br/>
	


