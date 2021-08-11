So, let's get scripting. But first, what is a shell?

The shell, in UNIX and Linux is the equivalent of a command interpreter in Windows. Its job is to accept commands, as typed by the user on the command line, and interpret each of those commands, acting on it however necessary. The shell is a little like DOS operating system in many ways; the only difference being that it's like DOS on steroids. I hope that over the remainder of this course you will you will understand this sentiment.

For example typing:
> `ls -l`{{execute}}
on the command line produces some output. How does UNIX know to call the `ls` command? How does it know to interpret the `-l` as a switch? What about the output? How does the command output know to come to the screen? By chance? Nope. Nothing in Linux happens by chance!

The shell does these things. What about a shell script? 

A shell script is in essence, a whole bunch of shell commands entered together in a file. A little like the DOS batch file, where many shell commands are grouped together to perform some function(s).

What if we wanted to run two commands over and over again? Say,
> ```
> free
> df -h
> ```{{execute}}

One way of doing it would be to type the commands in over and over again. More work!!! Of course it is. We are looking at means of sticking to adage 1.1, not so? So, we could get clever and type both commands on a single line, separated by a semi-colon
> `free;df -h`{{execute}}

We've reduced our finger-work, but not by much. Again the better way of doing this is to put both these commands into a file. For our example we will call this file mycmds.sh:
> ```
> riaan@debian:/tmp> vi mycmds.sh    <To create the script>
> riaan@debian:/tmp> chmod +x mycmds.sh
> riaan@debian:/tmp> ./mycmds.sh
> 	     total       used       free     shared    buffers     cached
> Mem:        321628     317836       3792          0      14644      88536
> -/+ buffers/cache:     214656     106972
> Swap:       506480       1060     505420
> file system            Size  Used Avail Use% Mounted on
> /dev/hda1             5.5G  3.5G  2.1G  63% /
> tmpfs                 158M  4.0K  158M   1% /dev/shm
> riaan@debian:/tmp>
> ```
  
Then all we have to do it execute it, and voila , we have "created a new command", aka mycmds.sh. Now each time, we merely need to run the script and the commands are executed together.
  
<br/>
