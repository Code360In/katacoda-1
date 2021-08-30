# Removing our container

What happens if we remove our c1 container?

Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker rm -f c1 </span>
> 
The `-f` option will perform a "force removal" of a running container. It will stop the container (if it is running) and then remove the container.

Run the `ls` command again. 

Does the file "hello.txt" exists in the **UpperDir** folder?

<br/>
