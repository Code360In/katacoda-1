What if we have files that we do not want Git to track for us, like backup files created by our editor or intermediate files created during data analysis? Let’s create a few dummy files:
> ```
> mkdir results
> touch a.dat b.dat c.dat results/a.out results/b.out
> git init
> git status
> ```{{execute}}

and see what Git says:

> ```
> On branch master
> No commits yet
> Untracked files:
>   (use "git add <file>..." to include in what will be committed)
> 
>       .bashrc
>       .gitconfig
>       .profile
>       .ssh/
>       a.dat
>       b.dat
>       c.dat
>       results/
> 
> nothing added to commit but untracked files present (use "git add" to track)
> ```
  

Putting these files under version control would be a waste of disk space. What’s worse, having them all listed could distract us from changes that actually matter, so let’s tell Git to ignore them.

We do this by creating a file in the root directory of our project called `.gitignore`:
> `nano .gitignore`{{execute}}
  
and add the following into the file:
> ```
> *.dat
> results/
> ```{{copy}}
  
These patterns tell Git to ignore any file whose name ends in `.dat` and everything in the `results` directory. (If any of these files were already being tracked, Git would continue to track them.)

Once we have created this file, the output of `git status` is much cleaner:
> `git status`{{execute}}
  
> ```
> On branch master
> No commits yet
> Untracked files:
>   (use "git add <file>..." to include in what will be committed)
> 
>       .bashrc
>       .gitconfig
>       .gitignore
>       .profile
>       .ssh/
> 
> nothing added to commit but untracked files present (use "git add" to track)
> ```
  
<br/>
 
  


  
  
  
  
  
  
  
  
  
  
  
  
  
  
