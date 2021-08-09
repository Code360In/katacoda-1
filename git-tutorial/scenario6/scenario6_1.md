As we saw in the previous episode, we can refer to commits by their identifiers. You can refer to the <i> most recent commit </i> of the working directory by using the identifier `HEAD`.

We’ve been adding one line at a time to `mars.txt`, so it’s easy to track our progress by looking, so let’s do that using our `HEAD`s. Let's begin with `mars.txt` and creating a repository.

> ```
> mkdir planets
> cd planets
> git init
> nano mars.txt
> ```{{execute}}

Add the following line into `mars.txt` and save the file:
> `Cold and dry, but everything is my favorite color. `{{execute}}

Then, we add the file into the repository:
> ```
> git add mars.txt
> git status
> git commit -m "Create a new file"
> ```{{execute}}

You can see that we create a new file mars.txt. Now, we will modify the file:
> `nano mars.txt`{{execute}}

Add the following line into `mars.txt` and save the file:
> `The two moons may be a problem for Wolfman`{{execute}}
> 
> ```
> git add mars.txt
> git status
> git diff HEAD mars.txt 
> ```{{execute}}

Now, let's see what we get:
> ```  
> diff --git a/mars.txt b/mars.txt
> index b36abfd..0848c8d 100644
> --- a/mars.txt
> +++ b/mars.txt
> @@ -1,2 +1,3 @@
>  Cold and dry, but everything is my favorite color
> +The two moons may be a problem for Wolfman
> ```

To exit the commit, we can click <kbd> ctrl+Z </kbd>.

The real goodness in all this is when you can refer to previous commits. We do that by adding `~1` to refer to the commit one before HEAD. If we want to see the differences between older commits we can use git diff again, but with the notation `HEAD~1`, `HEAD~2`, and so on, to refer to them.

We could also use `git show` which shows us what changes we made at an older commit as well as the commit message, rather than the differences between a commit and our working directory that we see by using `git diff`.

> `git show HEAD mars.txt`{{execute}}

Now, we have the commit ID:
> ```
> commit f22b25e3233b4645dabd0d81e651fe074bd8e73b
> Author: Katacoda Scenario <scenario@katacoda.com>
> Date:   Sun Aug 8 15:51:20 2021 +0000
> 
>     Create a new file
>     
> diff --git a/mars.txt b/mars.txt
> index b36abfd..0848c8d 100644
> --- a/mars.txt
> +++ b/mars.txt
> @@ -1,2 +1,3 @@
>  Cold and dry, but everything is my favorite color
> +The two moons may be a problem for Wolfman
> ```

<br/> 

In this way, we can build up a chain of commits. The most recent end of the chain is referred to as HEAD; we can refer to previous commits using the ~ notation, so HEAD~1 means “the previous commit”, while HEAD~123 goes back 123 commits from where we are now.

We can also refer to commits using those long strings of digits and letters that git log displays. These are unique IDs for the changes, and “unique” really does mean unique: every change to any set of files on any computer has a unique 40-character identifier. Our first commit was given the ID `f22b25e3233b4645dabd0d81e651fe074bd8e73b`, so let’s try this:
> `git diff f22b25e3233b4645dabd0d81e651fe074bd8e73b mars.txt`{{copy}} (amend according to your ID)

We can also use just the first few characters (typically seven for normal size projects):
> `git diff f22b25e  mars.txt`{{copy}}

All right! So we can save changes to files and see what we’ve changed. Now, how can we restore older versions of things? Let’s suppose we change our mind about the last update to `mars.txt` (the “ill-considered change”).

`git status` now tells us that the file has been changed, but those changes haven’t been staged:
> `git status`{{execute}}

## Recover old commit version
We can put things back the way they were by using git checkout:
> ```
> git checkout HEAD mars.txt
> cat mars.txt
> ```{{execute}}

As you might guess from its name, `git checkout` checks out (i.e., restores) an old version of a file. In this case, we’re telling Git that we want to recover the version of the file recorded in `HEAD`, which is the last saved commit. If we want to go back even further, we can use a commit identifier instead (Again, change the ID to yours):
> ```
> git checkout f22b25e  mars.txt
> ```{{copy}}
> ```
> cat mars.txt
> git status
> ```{{execute}}

Notice that the changes are currently in the staging area. Again, we can put things back the way they were by using git checkout:
> `git checkout HEAD mars.txt`{{execute}}
