# What is Docker?

Docker is an open platform for developing, packaging, shipping, and running applications. It provides the ability to package and run an application in a loosely isolated environment called a container. Containers are lightweight and contain everything needed to run the application and allow you to run many containers simultaneously on a given host. By providing the tooling and a platform for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

# Running your first container - Hello World 

Test your Docker installation by running the following in the command prompt. Execute:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker run hello-world </span>

Here's what happens when you execute the above command:
1. The Docker engine will try to find an image named "hello-world". 
2. When there are no images stored locally (Unable to find image...)
3. The Docker engine will visit [Docker Hub](https://hub.docker.com/) to look for an image named "hello-world".
4. The image will be pulled and run locally in a container, which output the text you see in your terminal
5. The container exits after printing the message.

You can use the `docker image ls` command to see a list of all images on your machine (Docker host). 

Execute: 

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker image ls </span>

Check that the hello-world image is shown.

You can check the status of your containers by running
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps </span>

You will NOT see any container as the container has exited (stopped) after printing the message. 
To list all running and exited containers, run:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps -a </span>

**Exercises**: 
* Execute the following command to understand more about the `docker ps` command.
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps --help </span>

<br/>
