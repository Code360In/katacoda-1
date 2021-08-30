## Showing the contents

The `echo` command will print the string on the screen (standard output) by default
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> echo "hello" </span>

We can redirect the output to a file:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> echo "This is the first line." > text1.txt </span>

Check that the file is created:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> ls </span>

We can show the file content by using the `cat` command:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> cat text1.txt </span>

We can also append a string to a file by using the `>>` operator:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> echo "This is the second line." >> text1.txt </span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> cat text1.txt </span>

<br/>
