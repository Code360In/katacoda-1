## Manipulating files

We may rename the file by using the `mv` command:
> `mv text1.txt text2.txt`{{execute}}

Check that the file **text1.txt** is renamed to **text2.txt**:
> `ls`{{execute}}
> 
> `cat text2.txt`{{execute}}

We may move a file to a folder:
> `mv text2.txt dir1`{{execute}}

Check the file **text2.txt** is no longer in the current folder:
> `ls`{{execute}}

The file should have been moved inside the **dir1** folder:
> `ls dir1`{{execute}}

We may copy a file by using the `cp` command:
> `cp dir1/text2.txt text3.txt`{{execute}}

Show the content of **text3.txt**:
> `cat text3.txt`{{execute}}
> 
> `ls`{{execute}}

<br/>
