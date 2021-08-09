First let’s make sure we’re still in the right directory. You should be in the `planets` directory.

> ## Bash 
> `mkdir planets`{{execute}}
> 
> `cd ~/planets`{{execute}}
> 
> `git init`{{execute}}
> 
> `git checkout -b main`{{execute}}

Let’s create a file called `mars.txt` that contains some notes about the Red Planet’s suitability as a base. We’ll use `nano` to edit the file; you can use whatever editor you like. In particular, this does not have to be the `core.editor` you set globally earlier. But remember, the bash command to create or edit a new file will depend on the editor you choose (it might not be `nano`). 

> ## Bash 
> `nano mars.txt`{{execute}}

Type the text below into the mars.txt file:
> `Cold and dry, but everything is my favorite color`{{copy}}

Let’s first verify that the file was properly created by running the list command (`ls`):

> ## Bash 
> `ls`{{execute}}

> ## Output
> `mars.txt`

`mars.txt` contains a single line, which we can see by running:

> ## Bash
> `cat mars.txt`{{execute}}

> ## Output
> `Cold and dry, but everything is my favorite color`

If we check the status of our project again, Git tells us that it’s noticed the new file:

> ## Bash 
> `git status`{{execute}}

> ## Output
> ```
> On branch main
> 
> No commits yet
> 
> Untracked files:
> 
>    (use "git add <file>..." to include in what will be committed)
>
>         mars.txt
>
>  nothing added to commit but untracked files present (use "git add" to track)
> ```
  
The “untracked files” message means that there’s a file in the directory that Git isn’t keeping track of. We can tell Git to track a file using `git add`:
  
> ## Bash 
> `git add mars.txt`{{execute}}
>
> `git status`{{execute}} 

> ## Output
> ```
> On branch main
>
> No commits yet
>
> Changes to be committed:
>
>   (use "git rm --cached <file>..." to unstage)
>
>        new file:   mars.txt
> ```

<br/>
  
Git now knows that it’s supposed to keep track of `mars.txt`, but it hasn’t recorded these changes as a commit yet. To get it to do that, we need to run one more command:
  
> ## Bash 
> `git commit -m "Start notes on Mars as a base"`{{execute}}

> ## Output
> [main (root-commit) f22b25e] Start notes on Mars as a base
>
>  1 file changed, 1 insertion(+)
>
>  create mode 100644 mars.txt

<br/>

When we run `git commit`, Git takes everything we have told it to save by using `git add` and stores a copy permanently inside the special `.git` directory. This permanent copy is called a [commit](https://swcarpentry.github.io/git-novice/reference.html#commit) (or [revision](https://swcarpentry.github.io/git-novice/reference.html#revision)) and its short identifier is `f22b25e`. Your commit may have another identifier.

We use the `-m` flag (for “message”) to record a short, descriptive, and specific comment that will help us remember later on what we did and why. If we just run `git commit` without the `-m` option, Git will launch `nano` (or whatever other editor we configured as `core.editor`) so that we can write a longer message.

<br/><br/>
