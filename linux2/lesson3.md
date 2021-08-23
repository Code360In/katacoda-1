## A bit of plumbing

Linux command line includes some powerful tools for manipulating text content, and ways to join those tools together to create something more capable still.

To check the number of lines in a file, the `wc` (word count) command can tell us that. There are different switches to use:
- `-l` switch: print the number of lines
- `-m` switch: print the character counts
- `-w` switch: print the word counts

Here, we will try the usage of the switches with **_combined.txt_** in the _helloworld_ directory. :
> ```
> cd /helloworld
> cat combined.txt
> wc -l combined.txt
> wc -m combined.txt
> wc -w combined.txt
> ```{{execute}}

To check for the file and folder counts in a specific path, we can do like this (Four files in _helloworld_ directory):
> ```
> ls /helloworld
> ls /helloworld | wc -l
> ```{{execute}}

To list the files and folders in a directory, the following command is needed:
> `ls /helloworld | less`{{execute}}

<br/>

## Checking unique lines

Now, we want to see unique lines in _combined.txt_. Unix has a command `uniq` that will only output unique lines in the file. By executing the following line, we can get 1 as the two lines in the files are duplicate:
> `cat combined.txt | uniq | wc -l`{{execute}}

Also, if you want to know the exact string of the unique line, we can do like:
> `cat combined.txt | uniq | less`{{execute}}

<br/>

## Sorting lines

First, we create a file in the directory:
> ```
> echo -e "2\n1" > sort.txt
> cat sort.txt
> ```{{execute}}

To sort the contents of the files alphabetically, we can use the `sort` command:
> `sort sort.txt | less`{{execute}}

<br/>

Exercise: How to sort a file with only unique lines?
Try:
> ```
> cat sort.txt
> sort sort.txt | uniq | less
> ```{{execute}}

<br/>
