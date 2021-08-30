## Cutting sections in file

We can cut out the sections from each line of files and write the result to standard output. There are mainly 3 options to use in the `cut` command:
1. `-d`: indicate a specific symbol to be field delimiter
2. `-f`: select the field that contains no delimiter character, and according to the selected field
3. `-b`: cut sections from each line specified by given byte positions

**_Examples_**
The ' ' space is a separator of each field, and we return the second field **'this'**:
> `echo "Hello this is an example." | cut -d ' ' -f 2`{{execute}}

The terminal will select the fifth byte. Note that the `ü` character takes 2 bytes:
> `echo 'drüberspringen' | cut -b 5`{{execute}}

<br/>

## Unique lines

First we create a file with 3 lines, which two lines are the same:
> ```
> echo "123" >> text1.txt
> echo "123" >> text1.txt
> echo "321" >> text1.txt
> ```{{execute}}
> 
> `ls`{{execute}}
>
> `cat text1.txt`{{execute}}

The `uniq` command is to filter out the repeated lines in a file:
> `uniq text1.txt`{{execute}}

**Exercise**: Find the number of lines, words and characters where only unique lines are considered.

<br/>
