## Hidden files

Linux systems commonly stores settings and configuration data as hidden files so that they do not clutter the view of your own files. To create a hidden file, simply starting a name with a dot (".") is enough to make it disappear:
> ```
> echo "Hello I am a hidden file." > .hidden.txt
> ls
> ```{{execute}}

You can still work with the hidden file. Make sure you include the dot when you specify its file name:
> ```
> cat .hidden.txt
> mkdir .hidden
> mv .hidden.txt .hidden
> less .hidden/.hidden.txt
> ```{{execute}}
