# Assign a name for the container

Previously, a container name will be randomly generated for your containers (e.g. romantic_edison, unruffled_cannon). You may assign a name for your container using the `--name` switch. For instance, to create a container named  `mybusybox` from the busybox image, execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run --name mybusybox busybox ls </span>

Check that the name of the container that you have launched is `mybusybox`. Execute

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps -a </span>

What happens if you create another container with the same name?

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run --name mybusybox busybox ls </span>

To create a new container with the same name, you should first remove the previous container.  You may remove  the container with by using the container name. Execute

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker rm mybusybox </span>

Execute the following command to start another container with the same name. Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run --name mybusybox busybox ls </span>

Check that a new busybox container is created. Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps -a </span>

<br/>
