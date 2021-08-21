## A bit of plumbing

Linux command line includes some powerful tools for manipulating text content, and ways to join those tools together to create something more capable still.

To check the number of lines in a file, the `wc` (word count) command can tell us that. There are different switches to use:
- `-l` switch: print the number of lines
- `-m` switch: print the character counts
- `-w` switch: print the word counts

Here, we will try the usage of the switches with **_combined.txt_** in the _helloworld_ directory. :
> ```
> cd helloworld
> cat combined.txt
> wc -l combined.txt
> wc -m combined.txt
> wc -w combined.txt
> ```{{execute}}

To check the number of files and folders in the home directory, we can have a shortcut to pipe the data. `ls ~` lists the contents of the home directory, while `wc -l` helps counting the lines. 
> ```
> ls ~
> ls ~ | wc -l
> ```{{execute}}

To check for the file and folder counts in a specific path, we can do like this (Two files in _helloworld_ directory):
> ```
> ls /root/helloworld
> ls /root/helloworld | wc -l
> ```{{execute}}

To list the files and folders in a directory, the following command is needed:
> `ls /root/helloworld | less`{{execute}}

<br/>
