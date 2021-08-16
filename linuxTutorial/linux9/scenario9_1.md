Before we conclude this tutorial it’s worth mentioning _hidden files_ (and folders). These are commonly used on Linux systems to store settings and configuration data, and are typically hidden simply so that they don’t clutter the view of your own files. There’s nothing special about a hidden file or folder, other than it’s name: simply starting a name with a dot (”.”) is enough to make it disappear.
> ```
> ls > combined.txt
> ls
> mv combined.txt .combined.txt
> ls
> ```{{execute}}

You can still work with the hidden file by making sure you include the dot when you specify its file name:
> ```
> cat .combined.txt
> mkdir .hidden
> mv .combined.txt .hidden
> less .hidden/.combined.txt
> ```{{execute}}

If you run `ls` you’ll see that the `.hidden` directory is, as you might expect, hidden. You can still list its contents using `ls .hidden`, but as it only contains a single file which is, itself, hidden you won’t get much output. But you can use the `-a` (show all) switch to `ls` to make it show everything in a directory, including the hidden files and folders:
> ```
> ls
> ls -a
> ls .hidden
> ls -a .hidden
> ```{{execute}}

Notice that the shortcuts we used earlier, `.` and `..`, also appear as though they’re real directories.

As for our recently installed `tree` command, that works in a similar way (except without an appearance by `.` and `..`):
> ```
> tree 
> tree -a
> ```{{execute}}

Switch back to your home directory (`cd`) and try running `ls` without and then with the `-a` switch. Pipe the output through `wc -l` to give you a clearer idea of how many hidden files and folders have been right under your nose all this time. These files typically store your personal configuration, and is how Unix systems have always offered the capability to have system-level settings (usually in `/etc`) that can be overridden by individual users (courtesy of hidden files in their home directory).

You shouldn’t usually need to deal with hidden files, but occasionally instructions might require you to `cd` into `.config`, or edit some file whose name starts with a dot. At least now you’ll understand what’s happening, even when you can’t easily see the file in your graphical tools.

---------------------

We’ve reached the end of this tutorial, and you should be back in your home directory now (use `pwd` to check, and `cd` to go there if you’re not). It’s only polite to leave your computer in the same state that we found it in, so as a final step, let’s remove the experimental area that we were using earlier, then double-check that it’s actually gone:
> ```
> rm -r /tmp/tutorial
> ls /tmp
> ```{{execute}}

As a last step, let’s close the terminal. You can just close the window, but it’s better practice to log out of the shell. You can either use the `logout` command, or the <kbd> Ctrl-D </kbd> keyboard shortcut. If you plan to use the terminal a lot, memorising <kbd> Ctrl-Alt-T </kbd> to launch the terminal and <kbd> Ctrl-D </kbd> to close it will soon make it feel like a handy assistant that you can call on instantly, and dismiss just as easily.

<br/>
