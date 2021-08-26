## Creating files using redirection

Now, we will look into creating files. First, remind yourself what the `ls` command is currently showing:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

Suppose we would like to create a text file with all the file names in **_/helloworld_** directory, so we use ">" symbol to write in the content:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls > output.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

Then, we can see the file content with the `cat` command:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat output.txt</span>

Sample output:

![Picture 2](./assets/pic2.png)

Afterwards, we can also use a new command - `echo`. It is used to print its arguments out on the terminal, and combining it with a redirect, we can easily create small text files:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo "This is the first text file." > text1.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo "This is the second text file." > text2.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>


Just mentioned above, `cat` command can check the file contents, but `cat` can do more than that. If you pass more than one filename to cat it will output each of them, one after the other, as a single block of text: 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat text1.txt text2.txt</span>

Also, some shortcuts, or wildcard characters, can save typing if the files have similar names. 
- A question mark ("?"): indicate any **_single character_** within the file name
- An asterisk ("*"): indicate zero or more characters

Examples:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat text1.txt text2.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat text?.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat text*</span>

It can be more simplied as the file names are all starting with a **_t_**:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat t* > combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat combined.txt</span>

When you would like to **append** to the content of the files, we will do with ">>":
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo "I've appended a line!" >> combined.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">cat combined.txt</span>

<br/>

## A note about case

Unix systems are case-sensitive. The following is an example, where we will have three different files created:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo "Lower case" > a.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo "Upper case" > A.TXT</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">echo "Mixed case" > A.txt</span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left:10px; padding-right:10px;">ls</span>

Generally you should try to avoid creating files and folders whose name only varies by case. A good naming practice is like:
- keep file names all lower case
- with only letters, numbers, underscores and hyphens

<br/>
