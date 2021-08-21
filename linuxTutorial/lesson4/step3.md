## Deleting files and folders

At this stage, we will delete files:
> ```
> rm dir4/dir5/dir6/index.txt copy2_index.txt
> ```{{execute}}

And we can try to delete directories:
> ```
> rm folder*
> ```{{execute}}

Sample output:

![Picture 1](./assets/pic1.png)

As we used wildcard character "*" in the directory removal, the system has triggered a safety net to prevent accidental delete. As a result, in order to remove a directory (after serious consideration), we can use `rmdir` command to do the job:
> ```
> rmdir folder*
> ls
> ```{{execute}}


