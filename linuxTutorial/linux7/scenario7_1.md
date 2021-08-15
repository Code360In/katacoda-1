Today’s computers and phones have the sort of graphical and audio capabilities that our 70s terminal users couldn’t even begin to imagine. Yet still text prevails as a means to organise and categorise files. Whether it’s the file name itself, GPS coordintates embedded in photos you take on your phone, or the metadata stored in an audio file, text still plays a vital role in every aspect of computing. It’s fortunate for us that the Linux command line includes some powerful tools for manipulating text content, and ways to join those tools together to create something more capable still.

Let’s start with a simple question. How many lines are there in your _combined.txt_ file? The `wc` (word count) command can tell us that, using the `-l` switch to tell it we only want the line count (it can also do character counts and, as the name suggests, word counts):
> `nano combined.txt`{{execute}}
> ```
> wc combined.txt
> wc -l combined.txt
> ```{{execute}}

Similarly, if you wanted to know how many files and folders are in your home directory, and then tidy up after yourself, you could do this:
> ```
> ls ~ > file_list.txt
> wc -l file_list.txt
> rm file_list.txt
> ```{{execute}}

That method works, but creating a temporary file to hold the output from `ls` only to delete it two lines later seems a little excessive. Fortunately the Unix command line provides a shortcut that avoids you having to create a temporary file, by taking the output from one command (referred to as _standard output_ or _STDOUT_) and feeding it directly in as the input to another command (_standard input_ or _STDIN_). It’s as though you’ve connected a pipe between one command’s output and the next command’s input, so much so that this process is actually referred to as _piping_ the data from one command to another. Here’s how to pipe the output of our `ls` command into `wc`:
> `ls ~ | wc -l`{{execute}}

Notice that there’s no temporary file created, and no file name needed. Pipes operate entirely in memory, and most Unix command line tools will expect to receive input from a pipe if you don’t specify a file for them to work on. Looking at the line above, you can see that it’s two commands, `ls ~` (list the contents of the home directory) and `wc -l` (count the lines), separated by a vertical bar character (”|”). This process of piping one command into another is so commonly used that the character itself is often referred to as the _pipe_ character, so if you see that term you now know it just means the vertical bar.

Note that the spaces around the pipe character aren’t important, we’ve used them for clarity, but the following command works just as well, this time for telling us how many items are in the _/etc_ directory:
> `ls /etc|wc -l`{{execute}}

Phew! That’s quite a few files. If we wanted to list them all it would clearly fill up more than a single screen. As we discovered earlier, when a command produces a lot of output, it’s better to use less to view it, and that advice still applies when using a pipe (remember, press q to quit):

Phew! That’s quite a few files. If we wanted to list them all it would clearly fill up more than a single screen. As we discovered earlier, when a command produces a lot of output, it’s better to use `less` to view it, and that advice still applies when using a pipe (remember, press **q** to quit):
> `ls /etc | less`{{execute}}

Going back to our own files, we know how to get the number of lines in _combined.txt_, but given that it was created by concatenating the same files multiple times, I wonder how many unique lines there are? Unix has a command, `uniq`, that will only output unique lines in the file. So we need to `cat` the file out and pipe it through `uniq`. But all we want is a line count, so we need to use `wc` as well. Fortunately the command line doesn’t limit you to a single pipe at a time, so we can continue to chain as many commands as we need:
> `cat combined.txt | uniq | wc -l`{{execute}}

That line probably resulted in a count that’s pretty close to the total number of lines in the file, if not exactly the same. Surely that can’t be right? Lop off the last pipe to see the output of the command for a better idea of what’s happening. If your file is very long, you might want to pipe it through `less` to make it easier to inspect:
> `cat combined.txt | uniq | less`{{execute}}

It appears that very few, if any, of our duplicate lines are being removed. To understand why, we need to look at the documentation for the `uniq` command. Most command line tools come with a brief (and sometimes not-so-brief) instruction manual, accessed through the `man` (manual) command. The output is automatically piped through your pager, which will typically be `less`, so you can move back and forth through the output, then press **q** when you’re finished:
> `man uniq`{{execute}}

![Picture1](./assets/pic1.png)

Because this type of documentation is accessed via the man command, you’ll hear it referred to as a “man page”, as in “check the man page for more details”. The format of man pages is often terse, think of them more as a quick overview of a command than a full tutorial. They’re often highly technical, but you can usually skip most of the content and just look for the details of the option or argument you’re using.

The `uniq` man page is a typical example in that it starts with a brief one-line description of the command, moves on to a synopsis of how to use it, then has a detailed description of each option or parameter. But whilst man pages are invaluable, they can also be inpenetrable. They’re best used when you need a reminder of a particular switch or parameter, rather than as a general resource for learning how to use the command line. Nevertheless, the first line of the **DESCRIPTION** section for `man uniq` does answer the question as to why duplicate lines haven’t been removed: it only works on _adjacent_ matching lines.

The question, then, is how to rearrange the lines in our file so that duplicate entries are on adjacent lines. If we were to sort the contents of the file alphabetically, that would do the trick. Unix offers a `sort` command to do exactly that. A quick check of `man sort` shows that we can pass a file name directly to the command, so let’s see what it does to our file:
> `sort combined.txt | less`{{execute}}

You should be able to see that the lines have been reordered, and it’s now suitable for piping straight into `uniq`. We can finally complete our task of counting the unique lines in the file:
> `sort combined.txt | uniq | wc -l`{{execute}}

As you can see, the ability to pipe data from one command to another, building up long chains to manipulate your data, is a powerful tool, as well as reducing the need for temporary files, and saving you a lot of typing. For this reason you’ll see it used quite often in command lines. A long chain of commands might look intimidating at first, but remember that you can break even the longest chain down into individual commands (and look at their man pages) to get a better understanding of what it’s doing.

## Many manuals
Most Linux command line tools include a man page. Try taking a brief look at the pages for some of the commands you’ve already encountered: `man ls`, `man cp`, `man rmdir` and so on. There’s even a man page for the man program itself, which is accessed using `man man`, of course.

<br/>
