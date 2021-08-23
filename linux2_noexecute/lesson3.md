## A bit of plumbing

Linux command line includes some powerful tools for manipulating text content, and ways to join those tools together to create something more capable still.

To check the number of lines in a file, the `wc` (word count) command can tell us that. There are different switches to use:
- `-l` switch: print the number of lines
- `-m` switch: print the character counts
- `-w` switch: print the word counts

Here, we will try the usage of the switches with **_combined.txt_** in the _helloworld_ directory. :
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cd /helloworld</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">wc -l combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">wc -m combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">wc -w combined.txt</span>

To check for the file and folder counts in a specific path, we can do like this (Four files in _helloworld_ directory):
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls /helloworld</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls /helloworld | wc -l</span>

To list the files and folders in a directory, the following command is needed:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls /helloworld | less</span>

<br/>

## Checking unique lines

Now, we want to see unique lines in _unique.txt_. Unix has a command `uniq` that will only output unique lines in the file. By executing the following line, we can get 1 as the two lines in the files are duplicate:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo -e "hello\nhello" > unique.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat unique.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat unique.txt | uniq | wc -l</span>

Also, if you want to know the exact string of the unique line, we can do like:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat unique.txt | uniq | less</span>

<br/>

## Sorting lines

First, we create a file in the directory:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo -e 2\n1" > sort.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat sort.txt</span>

To sort the contents of the files alphabetically, we can use the `sort` command:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">sort sort.txt | less</span>

<br/>

Exercise: How to sort a file with only unique lines?
Try:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat sort.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">sort sort.txt | uniq | less</span>


<br/>
