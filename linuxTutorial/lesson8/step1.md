## Hidden files

Linux systems commonly stores settings and configuration data as hidden files so that they do not clutter the view of your own files. To create a hidden file, simply starting a name with a dot (".") is enough to make it disappear:
> ```
> cd helloworld
> echo "Hello I am a hidden file." > .hidden.txt
> ls
> ```{{execute}}

You can still work with the hidden file. Make sure you include the dot when you specify its file name:
> `cat .hidden.txt`{{execute}}
> 
> `mkdir .hidden`{{execute}}
> 
> `mv .hidden.txt .hidden`{{execute}}
> 
> `less .hidden/.hidden.txt`{{execute}}

If you run `ls`, it is obvious that we can see nothing. You can still use `ls .hidden` to check the contents. Also, we can use the `-a` switch to `ls` to make it show everything in a directory, including the hidden files and folders:
> `ls`{{execute}}
> 
> `ls -a`{{execute}}
> 
> `ls .hidden`{{execute}}
> 
> `ls -a .hidden`{{execute}}

<br/>

You shouldn’t usually need to deal with hidden files, but occasionally instructions might require you to `cd` into `.config`, or edit some file whose name starts with a dot.

<br/>
