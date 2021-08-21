## Moving files

Let's begin by navigating to the **_helloworld_** directory.
> ```
> cd /helloworld
> ls
> ```{{execute}}

Then, we try to put our **_index.txt_** file into our **_dir1_** directory, using the `mv` (move) command:
> ```
> mv index.txt dir1
> ls dir1
> ```{{execute}}

You can see the **_index.txt_** file is moved. Return to the working directory:
> `cd ..`{{execute}}

Now suppose it turns out that file shouldn't be in **_dir1_** after all. We can use `mv index.txt ..` to move the file into the parent directory after we navigate to **_dir1_**, but here we can use a path shortcut to avoid changing directory as we only have 1 file in the directory:
> `mv dir1/* .`{{execute}}

The "*" has matched with any filename in that directory, saving ourselves a few more keystrokes.

<br/>

The `mv` command also lets us move more than one file at a time. Now we move **_index.txt_**, all **_textn.txt_** files and **_dir3_** into **_dir2_**.
> ```
> mv index.txt text*.txt dir3 dir2
> ls 
> ls dir2
> ```{{execute}}

We got the files moved into **_dir2_**. But again, the file should be put in the path of **_dir4/dir5/dir6_**. Here is the amendment:
> ```
> mv dir2/index.txt dir4/dir5/dir6
> ls dir2
> ls dir4/dir5/dir6
> ```{{execute}}

Notice how the `mv` command functions. It helps to operate on files and folders in totally different locations. 

<br/>
