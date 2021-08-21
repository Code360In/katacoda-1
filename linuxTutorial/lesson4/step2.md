## Copying files

Now, we will try to keep a copy in our working directory. The `cp` command copies:
> ```
> cp dir4/dir5/dir6/index.txt .
> ls dir4/dir5/dir6
> ls
> ```{{execute}}

Next, we create another copy of the file with a different name:
> ```
> cp index.txt copy_index.txt
> ls
> ```{{execute}}

When you want to change a file name, `mv` command will help:
> ```
> mv copy_index.txt copy2_index.txt
> ls
> ```{{execute}}

It also works on directories to change names:
> ```
> mv dir1 "dir 1"
> ls
> ```{{execute}}

<br/>
