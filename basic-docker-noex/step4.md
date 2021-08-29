# Running an interactive Busybox container

You can launch an interactive shell to the container by using the `-it` option.
- The `-i` option specify that you want an interactive session.
- The `-t` option allocates a pseudo  terminal connected to the container.

Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker run -it busybox </span>

Execute the command `hostname`{{execute T1}} in the busybox container. The container ID of your container will be used as the hostname of your container.

Sample output:
```
/ # hostname
bd835eb307ab
```
Your output will be different than the one shown above as you will get different a container ID.

Try the following commands in the busybox container's shell
- > <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> whoami </span>

- > <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> pwd </span>

- > <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> ps </span>

- > <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> echo 'hello 12345' </span>

- > <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> ping google.com </span> Press Ctrl+C to stop the ping command.

Exit the docker container.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> exit </span>

You may visit the https://busybox.net/downloads/BusyBox.html to understand more about the Linux commands available in Busybox 

<br/>
