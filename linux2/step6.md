## Plumbing files

First we create a file with 3 lines, which two lines are the same:
> ```
> echo "123" >> text3.txt
> echo "123" >> text3.txt
> echo "321" >> text3.txt
> ```{{execute}}
> 
> `ls`{{execute}}
>
> `cat text3.txt`{{execute}}

To send the output of one program (former part) to another program (latter part) for further processing, we use the _vertical bar character_ `|` as an operator. The `wc` command is to count the number of lines, words in a line and characters in a file:
> `cat text3.txt | wc`{{execute}}

The `less` command is to read the content of a text file one page at a time:
> `less text3.txt`{{execute}}

The `uniq` command is to filter out the repeated lines in a file:
> `uniq text3.txt`{{execute}}

**Exercise**: Find the number of lines, words and characters where only unique lines are considered.

<br/>
