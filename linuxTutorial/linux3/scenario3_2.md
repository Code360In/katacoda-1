Now to the command itself. `pwd` is an abbreviation of ‘print working directory’. All it does is print out the shell’s current working directory. But what’s a <b> working directory </b>?

One important concept to understand is that the shell has a notion of a default location in which any file operations will take place. This is its working directory. If you try to create new files or directories, view existing files, or even delete them, the shell will assume you’re looking for them in the current working directory unless you take steps to specify otherwise. So it’s quite important to keep an idea of what directory the shell is “in” at any given time, after all, deleting files from the wrong directory could be disastrous. If you’re ever in any doubt, the `pwd` command will tell you exactly what the current working directory is.

You can change the working directory using the `cd` command, an abbreviation for ‘change directory’. Try typing the following:
> `cd /`{{execute}}
