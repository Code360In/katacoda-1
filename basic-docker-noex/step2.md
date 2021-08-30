#  Busybox -The Swiss Army Knife of Embedded Linux 

The "Busybox" image combines tiny versions of many common UNIX utilities into a single small executable.  It has been written with size-optimization and limited resources in mind and can run well in small/embedded systems. 

We can first pull the image from Docker hub.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker pull busybox </span>

Check that the image is pulled successfully by using the `docker image ls` command.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker image ls </span>

Next, we run the image as a container.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run busybox </span>

You will not see any output as the container has immediately exited after execution. 

You may append a command to `docker run` to execute when the container starts:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run busybox ls -l </span>

Docker will execute the command `ls -l` inside the container for which you saw the directory listing.

Verify the container status by executing the following command:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps -a </span>

The name and ID of the various containers that you have launched and stopped (exited) will be shown. You may clean up the containers by using the container name/ID. 
- The command `docker rm [container name/ID]` will remove and clean up the stopped containers.

*Exercise*: 
Remove the busybox container you have created by using its container ID.

<br/>
