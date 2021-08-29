## Showing the contents

The `echo` command will print the string on the screen (standard output) by default
> `echo "Hello"`{{execute}}

We can redirect the output to a file:
> `echo "This is the first line." > text1.txt`{{execute}}

Check that the file is created:
> `ls`{{execute}}

We can show the file content by using the `cat` command:
> `cat text1.txt`{{execute}}

We can also append a string to a file by using the `>>` operator:
> `echo "This is the second line." >> text1.txt`{{execute}}
> `cat text1.txt`{{execute}}

<br/>
