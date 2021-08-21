## A note about case

Unix systems are case-sensitive. The following is an example, where we will have three different files created:
> ```
> echo "Lower case" > a.txt
> echo "Upper case" > A.TXT
> echo "Mixed case" > A.txt
> ls
> ```{{execute}}

Generally you should try to avoid creating files and folders whose name only varies by case. A good naming practice is like:
- keep file names all lower case
- with only letters, numbers, underscores and hyphens

<br/>
