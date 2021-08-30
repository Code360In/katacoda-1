## Plumbing files

To send the output of one program (former part) to another program (latter part) for further processing, we use the _vertical bar character_ `|` as an operator. The `wc` command is to count the number of lines, words in a line and characters in a file:
> `cat text3.txt | wc`{{execute}}

The `less` command is to read the content of a text file page by page. We will load a Bash shell script (**.bashrc**), which is a startup script for running a Linux terminal:
> `cat ~/.bashrc | less`{{execute}}

To navigate the file, you can:
- Press <kbd> SPACE </kbd> to move on next page
- Prees up and down arrow to scroll up and down
- Press <kbd> Q </kbd> to exit

It is important to use `--help` to understand the command options. For example, to know about the options of `ls`, we can do like this:
> `ls  --help | less`{{execute}}

<br/>
