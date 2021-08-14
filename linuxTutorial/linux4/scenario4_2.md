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

You should `cat` each of these files to check their contents. But `cat` is more than just a file viewer - its name comes from ‘concatenate’, meaning “to link together”. If you pass more than one filename to `cat` it will output each of them, one after the other, as a single block of text:
> `cat test_1.txt test_2.txt test_3.txt`{{execute}}

Where you want to pass multiple file names to a single command, there are some useful shortcuts that can save you a lot of typing if the files have similar names. A question mark (”?”) can be used to indicate “any single character” within the file name. An asterisk (”*”) can be used to indicate “zero or more characters”. These are sometimes referred to as “wildcard” characters. A couple of examples might help, the following commands all do the same thing:
> ```
> cat test_1.txt test_2.txt test_3.txt
> cat test_?.txt
> cat test_*
> ```{{execute}}

If you look at the output of `ls` you’ll notice that the only files or folders that start with “t” are the three test files we’ve just created, so you could even simplify that last command even further to `cat t*`, meaning “concatenate all the files whose names start with a t and are followed by zero or more other characters”. Let’s use this capability to join all our files together into a single new file, then view it:
> ```
> cat t* > combined.txt
> cat combined.txt
> ```{{execute}}

What do you think will happen if we run those two commands a second time? Will the computer complain, because the file already exists? Will it append the text to the file, so it contains two copies? Or will it replace it entirely? Give it a try to see what happens, but to avoid typing the commands again you can use the <b> Up Arrow </b> and <b> Down Arrow </b> keys to move back and forth through the history of commands you’ve used. Press the <b> Up Arrow </b> a couple of times to get to the first `cat` and press <kbd> Enter </kbd> to run it, then do the same again to get to the second.

As you can see, the file looks the same. That’s not because it’s been left untouched, but because the shell clears out all the content of the file before it writes the output of your `cat` command into it. Because of this, you should be extra careful when using redirection to make sure that you don’t accidentally overwrite a file you need. If you do want to append to, rather than replace, the content of the files, double up on the greater-than character:
> ```
> cat t* >> combined.txt
> echo "I've appended a line!" >> combined.txt
> cat combined.txt
> ```{{execute}}

Repeat the first `cat` a few more times, using the Up Arrow for convenience, and perhaps add a few more arbitrary `echo` commands, until your text document is so large that it won’t all fit in the terminal at once when you use `cat` to display it. In order to see the whole file we now need to use a different program, called a pager (because it displays your file one “page” at a time). The standard pager of old was called `more`, because it puts a line of text at the bottom of each page that says “–More–” to indicate that you haven’t read everything yet. These days there’s a far better pager that you should use instead: because it replaces `more`, the programmers decided to call it `less`.
> `less combined.txt`{{execute}}

When viewing a file through `less` you can use the Up Arrow, Down Arrow, Page Up, Page Down, Home and End keys to move through your file. Give them a try to see the difference between them. When you’ve finished viewing your file, press <kbd> q </kbd> to quit `less` and return to the command line.

<br/>
