## Relative and absolute paths

Most of the examples in the previous steps use **_relative_** paths. That is, the place you end up at depends on your currect working directory. Try the following to see the difference:
> ```
> cd /
> pwd
> cd etc
> pwd
> ```{{execute}}

> ```
> cd 
> pwd
> cd etc
> pwd
> ```{{execute}}

You will see an error saying "No such file or directory". Changing directory by specifying the directory name, or using `..` will have different effects depending on where you start from. The path only makes sense **_relative_** to your working directory.

In fact any path that starts with a forward slash is an absolute path. So, for the second execution, we should add a "/" to indicate the absolute path for the "etc" directory:
> ```
> cd 
> pwd
> cd /etc
> pwd
> ```{{execute}}

Also, we can use `whoami` command to remind your home directory:
> `whoami`{{execute}}

At last, there is a handy shortcut which works as an abolute path. Using the tilde character (”~”) at the start of your path similarly means “starting from my home directory”.
> ```
> cd ~
> pwd
> ```{{execute}}

<br/>
