## Warning
In this next section we’re going to start deleting files and folders. To make absolutely certain that you don’t accidentally delete anything in your home folder, use the `pwd` command to double-check that you’re still in the _/tmp/tutorial_ directory before proceeding.

Now we know how to move, copy and rename files and directories. Given that these are just test files, however, perhaps we don’t really need three different copies of _combined.txt_ after all. Let’s tidy up a bit, using the `rm` (remove) command:
> `rm dir4/dir5/dir6/combined.txt combined_backup.txt`{{execute}}

Perhaps we should remove some of those excess directories as well:
> `rm folder_*`{{execute}}
