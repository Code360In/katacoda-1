# Running the docker image


Run the docker image by executing

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker run myimage </span>

If a command is provided after the image name, the specified command will be executed instead.

What will be the output of the following command?

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker run myimage figlet docker is fun </span>
> 
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker run myimage ls -l </span>


You can also launch an interactive bash shell to the created container.  Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker run -it myimage bash </span>

Execute the following command to quit the shell.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> exit </span>

<br/>
