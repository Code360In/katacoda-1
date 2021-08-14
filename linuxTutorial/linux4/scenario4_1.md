In this section we’re going to create some real files to work with. To avoid accidentally trampling over any of your real files, we’re going to start by creating a new directory, well away from your home folder, which will serve as a safer environment in which to experiment:
> ```
> mkdir /tmp/tutorial
> cd /tmp/tutorial
> ```{{execute}}

Notice the use of an absolute path, to make sure that we create the tutorial directory inside /tmp. Without the forward slash at the start the `mkdir` command would try to find a tmp directory inside the current working directory, then try to create a tutorial directory inside that. If it couldn’t find a tmp directory the command would fail.

In case you hadn’t guessed, `mkdir` is short for ‘make directory’. Now that we’re safely inside our test area (double check with `pwd` if you’re not certain), let’s create a few subdirectories:
> `mkdir dir1 dir2 dir3`{{execute}}

There’s something a little different about that command. So far we’ve only seen commands that work on their own (`cd`, `pwd`) or that have a single item afterwards (`cd /`, `cd ~/Desktop`). But this time we’ve added three things after the `mkdir` command. Those things are referred to as parameters or arguments, and different commands can accept different numbers of arguments. The `mkdir` command expects at least one argument, whereas the `cd` command can work with zero or one, but no more. See what happens when you try to pass the wrong number of parameters to a command:
> ```
> mkdir
> cd /etc ~/Desktop
> ```{{exeute}}

Back to our new directories. The command above will have created three new subdirectories inside our folder. Let’s take a look at them with the `ls` (list) command:
> `ls`{{execute}}

If you’ve followed the last few commands, your terminal should be looking something like this:































