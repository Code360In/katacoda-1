## Using Nano

Nano is a text editor to create, amend and update file content. To open `nano` with an empty buffer, we can just type `nano`{{copy}} in the terminal. You can also create a new buffer with the designated directory and filename. Let's make it to:
> `ls`{{execute}}
> 
> `nano helloworld/greetings.txt`{{execute}}

Let's take a look at the default nano screen.

![Picture 4](./assets/pic4.png)

Several sections in the screen:
1. Name and version number at the top
2. Name of file you are editing
3. Content 
4. Executing status of your file at the bottom with [ ]
5. Shortcuts 

## Shortcuts in Nano editor

There are various shortcuts available in nano and the most common ones are listed at the bottom of the screen. 

The shortcuts are used with <kbd> ctrl </kbd> / <kbd> alt </kbd> and another letter. The common shortcuts function as:
- <kbd> ctrl + G </kbd>: View all the shortcut functions
- <kbd> ctrl + R </kbd>: Insert the contents of another file into your current buffer
- <kbd> alt + 6 </kbd>: Copy text
- <kbd> ctrl + U </kbd>: Paste text
- <kbd> alt + U </kbd>: Undo
- <kbd> alt + E </kbd>: Redo
- <kbd> ctrl + X </kbd>: Exit the editor (system will ask for saving)
- <kbd> ctrl + Z </kbd>: Stop the editor

We will now try these shortcuts. First, in the editor, we type `hello world`{{copy}} to add content. 

Then, we highlight "hello" (The highlight has to exclude the cursor). The sample output is as follow:

![Picture 5](./assets/pic5.png)

And we copy the text by clicking <kbd> alt + 6 </kbd> and place it to the end with <kbd> ctrl + U </kbd>. The sample out is as follow:

![Picture 6](./assets/pic6.png)

We can click <kbd> alt + U </kbd> to undo and <kbd> alt + E </kbd> to redo.

To save the file, click <kbd> ctrl + X </kbd> and click <kbd> Y </kbd>. Press <kbd> ENTER </kbd> when you sure the content is saved in the correct file.

<br/>
