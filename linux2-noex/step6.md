## Plumbing files

To send the output of one program (former part) to another program (latter part) for further processing, we use the _vertical bar character_ `|` as an operator. The following commands will utilize the operator.

The `less` command is to read the content of a text file page by page. We will load a Bash shell script (**.bashrc**), which is a startup script for running a Linux terminal:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> cat ~/.bashrc | less </span>

To navigate the file, you can:
- Press <kbd> SPACE </kbd> to move on next page
- Prees up and down arrow to scroll up and down
- Press <kbd> Q </kbd> to exit

It is important to use `--help` to understand the command options. For example, to know about the options of `ls`, we can do like this:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> ls  --help | less </span>

The `wc` command is to count the number of lines, words in a line and characters in a file:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> cat ~/.bashrc | wc </span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> cat ls --help | wc </span>

<br/>
