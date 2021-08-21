## Change working directory using the `cd` command

You can change the working directory using the cd command, an abbreviation for ‘change directory’. Try typing the following:
> ```
> cd /
> pwd
> ```{{execute}}

Now your working directory is "/". The “/” directory, often referred to as the **_root_** directory, is the base of that unified file system. From there everything else branches out to form a tree of directories and subdirectories.

From the root directory, the following command will move you into the “home” directory:
> ```
> cd home
> pwd
> ```{{execute}}

To go up to the parent directory (in this case back to "/"), we will use the special syntax of two dots (`..`) when changing directory. Be cautious of the space between `cd` and `..`:
> > ```
> cd ..
> pwd
> ```{{execute}}

A quick shortcut to get back to your home directory is:
> ```
> cd 
> pwd
> ```{{execute}}

You can also use .. more than once if you have to move up through multiple levels of parent directories, which we will go straight to the "etc" directory:
> ```
> cd ../../etc
> pwd
> ```{{execute}}

Sample output of the above commands:
![Picture2](./assets/pic2.png)

<br/>
