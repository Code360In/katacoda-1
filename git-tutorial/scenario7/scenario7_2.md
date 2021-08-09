The only thing Git notices now is the newly-created `.gitignore` file. You might think we wouldn’t want to track it, but everyone we’re sharing our repository with will probably want to ignore the same things that we’re ignoring. Let’s add and commit `.gitignore`:

> ```
> git add .gitignore
> git commit -m "Ignore data files and the results folder."
> git status
> ```{{execute}}

As a bonus, using `.gitignore` helps us avoid accidentally adding to the repository files that we don’t want to track:
> `git add a.dat`{{execute}}

You can see the system will inform the path is ignored:
> ```
> The following paths are ignored by one of your .gitignore files:
> a.dat
> Use -f if you really want to add them.
> ```


If we really want to override our ignore settings, we can use `git add -f` to force Git to add something. For example, `git add -f a.dat`. We can also always see the status of ignored files if we want:
> `git status --ignored`{{execute}}

The output is as follow:
> ```
> On branch main
> Ignored files:
>  (use "git add -f <file>..." to include in what will be committed)
>         a.dat
>         b.dat
>         c.dat
>         results/
> nothing to commit, working directory clean
> ```

<br/>
  
## Key Points
- The `.gitignore` file tells Git what files to ignore.
  
<br/>
