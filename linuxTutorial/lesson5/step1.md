## A bit of plumbing

Linux command line includes some powerful tools for manipulating text content, and ways to join those tools together to create something more capable still.

To check the number of lines in a file, the `wc` (word count) command can tell us that. There are different switches to use:
- `-l` switch: print the number of lines
- `-m` switch: print the character counts
- `-w` switch: print the word counts

Here, we will try the usage of the switches with **_index.txt_** in the _helloworld_ directory. The file contains texts "Hello this is your first text file.":
> ```
> cd helloworld
> wc -l index.txt
> wc -m index.txt
> wc -w index.txt
> ```{{execute}}

To check the number of files and folders in the home directory, we can have a shortcut to pipe the data. `ls ~` lists the contents of the home directory, while `wc -l` helps counting the lines. 
> `ls ~ | wc -l`{{execute}}


