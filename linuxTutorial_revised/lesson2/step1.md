## Basics
You can see the terminal is started on the right section. Let's run our first command. Make sure your keystrokes are on the terminal, then execute the following command:
> `pwd`{{execute}}

You should see a directory path printed out (probably something like `/root`).

![Picture1](./assets/pic1.png)

From the picture, we have a couple of basics to understand. First is that when you type a commandit appears on the same line as the odd text. The $ is there to tell you the terminal is ready to accept a command. It is usually referred to as the **_prompt_**. The second thing to understand is that when you run a command any output it produces will usually be printed directly in the terminal, then another prompt is shown once it's finished. Some commands can output a lot of text, others will operate silently and won’t output anything at all.

<br/>

## The importance of case
Be extra careful with case when typing in the command line. Typing `PWD` instead of `pwd` will produce an error, but sometimes the wrong case can result in a command appearing to run, but not doing what you expected.

<br/>

## A sense of location
Now to the command itself. `pwd` is an abbreviation of ‘**p**rint **w**orking **d**irectory’. All it does is print out the shell’s current _working directory_. One important concept to understand is that the shell has a notion of a default location in which any file operations will take place. This is its working directory. 

If you do any actions, the shell will assume the actions perform in the current working directory unless you take steps to specify otherwise. Therefore, keep in mind of what directory the shell is in at anytime, especially when you want to delete files. If you have any doubt, the `pwd` command will tell you exactly what the current working directory is.

<br/>
