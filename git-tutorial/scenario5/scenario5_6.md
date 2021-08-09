Two important facts you should know about directories in Git.

1. Git does not track directories on their own, only files within them. Try it for yourself:
   > ## Bash
   > `mkdir spaceships`{{execute}}
   > 
   > `git status`{{execute}}
   > 
   > `git add spaceships`{{execute}}
   > 
   > `git status`{{execute}}

   Note, our newly created empty directory `spaceships` does not appear in the list of untracked files even if we explicitly add it (<i> via </i> `git add`) to our repository. This is the reason why you will sometimes see `.gitkeep` files in otherwise empty directories. Unlike `.gitignore`, these files are not special and their sole purpose is to populate a directory so that Git adds it to the repository. In fact, you can name such files anything you like.

2. If you create a directory in your Git repository and populate it with files, you can add all files in the directory at once by:
   > ## Bash
   > `git add <directory-with-files>`{{execute}}

   Try it for yourself:
   > ## Bash
   > `touch spaceships/apollo-11 spaceships/sputnik-1`{{execute}}
   > 
   > `git status`{{execute}}
   > 
   > `git add spaceships`{{execute}}
   > 
   > `git status`{{execute}}

   Before moving on, we will commit these changes.
   > ## Bash
   > `git commit -m "Add some initial thoughts on spaceships"`{{execute}}


<br/>
