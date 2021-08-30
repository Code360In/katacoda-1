## Removing files and directories

We can remove a file by using the `rm` command:
> `rm text3.txt`{{execute}}

Also, we can remove a directory:
> `rmdir dir3`{{execute}}

Verify that the directory is removed:
> `ls`{{execute}}

_Important_: You cannot remove a directory if theire are files in it:
> `rmdir dir1`{{execute}}

To recursively remove the file and directory, use the `-r` option of the `rm` command:
> `rm -r dir1`{{execute}}

Check that **dir1** has been removed:
> `ls`{{execute}}

<br/>
