Now to the command itself. `pwd` is an abbreviation of ‘print working directory’. All it does is print out the shell’s current working directory. But what’s a <b> working directory </b>?

One important concept to understand is that the shell has a notion of a default location in which any file operations will take place. This is its working directory. If you try to create new files or directories, view existing files, or even delete them, the shell will assume you’re looking for them in the current working directory unless you take steps to specify otherwise. So it’s quite important to keep an idea of what directory the shell is “in” at any given time, after all, deleting files from the wrong directory could be disastrous. If you’re ever in any doubt, the `pwd` command will tell you exactly what the current working directory is.

You can change the working directory using the `cd` command, an abbreviation for ‘change directory’. Try typing the following:
> `cd /`{{execute}}
> `Note that the directory separator is a forward slash (”/”), not the backslash that you may be used to from Windows or DOS systems`

Now your working directory is “/”. If you’re coming from a Windows background you’re probably used to each drive having its own letter, with your main hard drive typically being “C:”. Unix-like systems don’t split up the drives like that. Instead they have a single unified file system, and individual drives can be attached (“mounted”) to whatever location in the file system makes most sense. The “/” directory, often referred to as the root directory, is the base of that unified file system. From there everything else branches out to form a tree of directories and subdirectories.

We will first create a folder in the terminal for the later directions:
> ```
> mkdir home
> pwd
> ```{{execute}}

From the root directory, the following command will move you into the “home” directory (which is an immediate subdirectory of “/”):
> ```
> cd home
> pwd
> ```{{execute}}

To go up to the parent directory, in this case back to “/”, use the special syntax of two dots (..) when changing directory (note the space between cd and .., unlike in DOS you can’t just type cd.. as one command):
> ```
> cd ..
> pwd
> ```{{execute}}

Typing cd on its own is a quick shortcut to get back to your home directory:
> ```
> cd
> pwd
> ```{{execute}}

You can also use .. more than once if you have to move up through multiple levels of parent directories:
> ```
> cd ../..
> pwd
> ```{{execute}}

Notice that in the previous example we described a route to take through the directories. The path we used means “starting from the working directory, move to the parent / from that new location move to the parent again”. So if we wanted to go straight from our home directory to the “etc” directory (which is directly inside the root of the file system), we could use this approach:
> ```
> cd
> pwd
> cd ../../etc
> pwd
> ```{{execute}}

<br/>

