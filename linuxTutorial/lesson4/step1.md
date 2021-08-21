## Moving and manipulating files

Let's begin by navigating to the **_helloworld_** directory.
> ```
> cd /helloworld
> ls
> ```{{execute}}

Then, we try to put our **_text1.txt_** file into our **_dir1_** directory, using the `mv` (move) command:
> ```
> mv text1.txt dir1
> ls dir1
> ```{{execute}}

You can see the **_text1.txt_** file is moved. Return to the working directory:
> `cd ..`{{execute}}

Now suppose it turns out that file shouldn't be in **_dir1_** after all. We can use `mv combined.txt ..` to move the file into the parent directory after we navigate to **_dir1_**, but here we can use a path shortcut to avoid changing directory as we only have 1 file in the directory:
> `mv dir1/* .`{{execute}}

The "*" has matched with any filename in that directory, saving ourselves a few more keystrokes.
