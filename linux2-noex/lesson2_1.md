## Moving files

Let's begin by navigating to the **_helloworld_** directory.
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cd /helloworld</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

Then, we try to put our **_combined.txt_** file into our **_dir1_** directory, using the `mv` (move) command:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">mv combined.txt dir1</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls dir1</span>

You can see the **_combined.txt_** file is moved.

Now suppose it turns out that file shouldn't be in **_dir1_** after all. We can use `mv index.txt ..` to move the file into the parent directory after we navigate to **_dir1_**, but here we can use a path shortcut to avoid changing directory as we only have 1 file in the directory:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">mv dir1/* .</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

The "*" has matched with any filename in that directory, saving ourselves a few more keystrokes.

<br/>

The `mv` command also lets us move more than one file at a time. Now we move **_combined.txt_**, all **_textn.txt_** files and **_dir3_** into **_dir2_**.
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">mv combined.txt text*.txt dir3 dir2</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls dir2</span>

We got the files moved into **_dir2_**. But again, the file should be put in the path of **_dir4/dir5/dir6_**. Here is the amendment:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">mv dir2/combined.txt dir4/dir5/dir6</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls dir2</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls dir4/dir5/dir6</span>

Notice how the `mv` command functions. It helps to operate on files and folders in totally different locations. 

<br/>

## Copying files

Now, we will try to keep a copy in our working directory. The `cp` command copies:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cp dir4/dir5/dir6/combined.txt .</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls dir4/dir5/dir6</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

Next, we create another copy of the file with a different name:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cp combined.txt copy_combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

When you want to change a file name, `mv` command will help:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">mv copy_combined.txt copy2_combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>


It also works on directories to change names:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">mv dir1 "dir 1"</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

<br/>
