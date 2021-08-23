## Creating files using redirection

Now, we will look into creating files. First, remind yourself what the `ls` command is currently showing:
> `ls`{{execute}}

Suppose we would like to create a text file with all the file names in **_/helloworld_** directory, so we use ">" symbol to write in the content:
> ```
> ls > output.txt
> ls
> ```{{execute}}

Then, we can see the file content with the `cat` command:
> `cat output.txt`{{execute}}

Sample output:

![Picture 2](./asset/pic2.png)

Afterwards, we can also use a new command - `echo`. It is used to print its arguments out on the terminal, and combining it with a redirect, we can easily create small text files:
> ```
> echo "This is the first text file." > text1.txt
> echo "This is the second text file." > text2.txt
> ls
> ```{{execute}}

Just mentioned above, `cat` command can check the file contents, but `cat` can do more than that. If you pass more than one filename to cat it will output each of them, one after the other, as a single block of text: 
> `cat text1.txt text2.txt`{{execute}}

Also, some shortcuts, or wildcard characters, can save typing if the files have similar names. 
- A question mark ("?"): indicate any **_single character_** within the file name
- An asterisk ("*"): indicate zero or more characters

Examples:
> ```
> cat text1.txt text2.txt
> cat text?.txt
> cat text*
> ```{{execute}}

It can be more simplied as the file names are all starting with a **_t_**:
> ```
> cat t* > combined.txt
> cat combined.txt
> ```{{execute}}

When you would like to **append** to the content of the files, we will do with ">>":
> ```
> echo "I've appended a line!" >> combined.txt
> cat combined.txt
> ```{{execute}}

<br/>
