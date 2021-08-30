
# Docker Commit

Start another Ubuntu container by running the Ubuntu docker image again:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run --name c2 -it ubuntu bash </span>

Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> figlet </span>

Is the `figlet` program installed in the new container? Why?

Exit the docker container.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> exit </span>

If we need something installed in our container, we should build a custom Docker image. We can

* Use  the `docker commit`  to commit a container's file changes or settings into a new image. 

* Write a Docker file to build a Docker image. 

In this exercise, we will focus on approach 1. Execute in the terminal (replace [container ID] with the ID of the container with figlet installed):

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker commit c1 ubuntu-figlet </span>

Verify that a new image named  `ubuntu-figlet` is created.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker image ls </span>

Execute the following  command to check if `figlet` is installed in the image.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run ubuntu-figlet figlet Hello PolyU </span>

Sample Output:

```
 _   _      _ _         ____       _       _   _ 
| | | | ___| | | ___   |  _ \ ___ | |_   _| | | |
| |_| |/ _ \ | |/ _ \  | |_) / _ \| | | | | | | |
|  _  |  __/ | | (_) | |  __/ (_) | | |_| | |_| |
|_| |_|\___|_|_|\___/  |_|   \___/|_|\__, |\___/ 
                                     |___/       
```

<br/>
