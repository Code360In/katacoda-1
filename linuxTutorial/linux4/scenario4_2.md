Our demonstration folder is starting to look rather full of directories, but is somewhat lacking in files. Let’s remedy that by redirecting the output from a command so that, instead of being printed to the screen, it ends up in a new file. First, remind yourself what the `ls` command is currently showing:
> `ls`{{execute}}

Suppose we wanted to capture the output of that command as a text file that we can look at or manipulate further. All we need to do is to add the greater-than character (”>”) to the end of our command line, followed by the name of the file to write to:
> `ls > output.txt`{{execute}}

This time there’s nothing printed to the screen, because the output is being redirected to our file instead. If you just run `ls` on its own you should see that the output.txt file has been created. We can use the `cat`ca command to look at its content:
> `cat output.txt`{{execute}}

Okay, so it’s not exactly what was displayed on the screen previously, but it contains all the same data, and it’s in a more useful format for further processing. Let’s look at another command, `echo`:
> `echo "This is a test"`{{execute}}

Yes, `echo` just prints its arguments back out again (hence the name). But combine it with a redirect, and you’ve got a way to easily create small test files:
> ```
> echo "This is a test" > test_1.txt
> echo "This is a second test" > test_2.txt
> echo "This is a third test" > test_3.txt
> ls
> ```{{execute}}






