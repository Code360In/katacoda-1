Most of the examples we’ve looked at so far use relative paths. That is, the place you end up at depends on your current working directory. Consider trying to `cd` into the “etc” folder. If you’re already in the root directory that will work fine:
> ```
> cd /
> pwd
> ```{{execute}}
> ```
> cd etc
> pwd
> ```{{execute}}

But what if you’re in your home directory?
> ```
> cd
> pwd
> ```{{execute}}
> ```
> cd etc
> pwd
> ```{{execute}}

You’ll see an error saying “No such file or directory” before you even get to run the last `pwd`. Changing directory by specifying the directory name, or using `..` will have different effects depending on where you start from. The path only makes sense relative to your working directory.

But we have seen two commands that are <b> absolute </b>. No matter what your current working directory is, they’ll have the same effect. The first is when you run `cd` on its own to go straight to your home directory. The second is when you used `cd /` to switch to the root directory. In fact any path that starts with a forward slash is an <b> absolute path </b>. You can think of it as saying “switch to the root directory, then follow the route from there”. That gives us a much easier way to switch to the `etc` directory, no matter where we currently are in the file system:
> ```
> cd
> pwd
> ```{{execute}}
> ```
> cd /etc
> pwd
> ```{{execute}}

It also gives us another way to get back to your home directory, and even to the folders within it. Suppose you want to go straight to your “Desktop” folder from anywhere on the disk (note the upper-case “D”). In the following command you’ll need to replace USERNAME with your own username, the `whoami` command will remind you of your username, in case you’re not sure:
> `whoami`{{execute}}

There’s one other handy shortcut which works as an absolute path. As you’ve seen, using “/” at the start of your path means “starting from the root directory”. Using the tilde character (”~”) at the start of your path similarly means “starting from my home directory”.
> ```
> cd ~
> pwd
> ```{{execute}}
> ```
> cd ~/index
> pwd
> ```{{execute}}

Now that odd text in the prompt might make a bit of sense. Have you noticed it changing as you move around the file system? On a Ubuntu system it shows your username, your computer’s network name and the current working directory. But if you’re somewhere inside your home directory, it will use “~” as an abbreviation. Let’s wander around the file system a little, and keep an eye on the prompt as you do so:

> `cd`{{execute}}
> 
> `cd /`{{execute}}
> 
> `cd ~/Desktop`{{execute}}
> 
> `cd /etc`{{execute}}
> 
> `cd /var/log`{{execute}}
> 
> `cd ..`{{execute}}
> 
> `cd`{{execute}}

You must be bored with just moving around the file system by now, but a good understanding of absolute and relative paths will be invaluable as we move on to create some new folders and files!

<br/>
