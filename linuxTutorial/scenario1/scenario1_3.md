There are some basic commands that we are going to look at. The idea is to get you into the process of understanding how commands are structured and build an understanding of what the commands do.

From hereon out, I'm going to assume that you can find out lots of things about commands primarily by looking at info and man pages.

Almost every Linux command can be run from the command line using various switches (or arguments / options) which allow one to change the output of this command in a number of different ways.

## The who command
The `who` command is designed to tell you who's logged on to the system.

If we run the `who` command without any switches, the left hand column shows the user id. This the user currently logged on to the system. In your case, you might be logged on as root, or perhaps as your user. The second column indicates where you are logged in.
> ```
> riaan@debian:~> who
> riaan    :0           Apr 30 11:13 (console)
> riaan    pts/0        Apr 30 11:13
> riaan    pts/3        Apr 30 11:14
> riaan    pts/4        Apr 30 11:30
> riaan    pts/5        Apr 30 13:19
> riaan    pts/6        Apr 30 12:07
> riaan    pts/7        Apr 30 12:09
> riaan@debian:~>
> ```

So if you look at the `who` command output, my user riaan is logged in from :0 which is the X console. He's also logged on to
> ```
> pts/0 and
> pts/1
> ```

These are pseudo terminals, indicating he's also logged into two pseudo terminals.

The final, third column indicates what time the user logged on.

The `who` command tells us about users using our system. That's great!

What are the other switches that we can use with `who`.
> `who --help`{{execute}}

This will show you the various switches that we can use with the who; command. So if we use a:
> `who -H`{{execute}}

it prints a heading line for us. The output should look as follows:
> ```
> $ who -H
> NAME             LINE     TIME         FROM
> heidi            ttyp1    Nov 27 17:29 (168.210.56.177:S)
> mwest            ttyp2    Nov 10 15:04 (apotheosis)
> heidi            ttyp4    Nov 11 13:18 (168.210.56.177:S)
> ```
                
To view a short listing which is the default listing for the who command:
> `who -s`{{execute}}

Using the -u switch:
> `who -u`{{execute}}

will show the users and their process id''s.
> ```
> root     tty2         Aug  4 10:41   .          2839
> riaan    :0           Aug  4 07:53  old         2836 (console)
> ```

In scripts, one can use the same commands as on the command line, including all the switches those commands use. One can run any command and produce standard text output, which one can use. We'll talk about how you can use the output later. Run the command to identify which users are logged into your system and from which processes they are logged on.

This will show how long a terminal has been idle. It will show not only which users are logged on and what process ids they are but also how long that user has been idle. Idle users might have gone out for lunch or they might have left for the day. In default mode, most of these systems don't log you out if you're idle for longer than 10 or 15 minutes. In the old days, most systems were configured to automatically log you out after 15 minutes.

Okay, so that's the who command. We're going to use these commands later to build a system to monitor our system automatically, because we want to be spending our time doing things we enjoy.

<br/>
