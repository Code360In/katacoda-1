## Checking unique lines

Now, we want to see unique lines in _combined.txt_. Unix has a command `uniq` that will only output unique lines in the file. By executing the following line, we can get 1 as the two lines in the files are duplicate:
> `cat combined.txt | uniq | wc -l`{{execute}}

Also, if you want to know the exact string of the unique line, we can do like:
> `cat combined.txt | uniq | less`{{execute}}

<br/>

## Sorting lines

To sort the contents of the files alphabetically, we can do 
