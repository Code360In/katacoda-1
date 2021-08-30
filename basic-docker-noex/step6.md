# Running FIGlet in the Ubuntu docker container

FIGlet is a simple command-line utility for creating ASCII text banners or large letters out of ordinary text.

Execute figlet in our Ubuntu container.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> figlet hello </span>

It will generate an error as the program is not installed in the Ubuntu docker image.

`apt` is a command-line utility for installing, updating, removing and managing deb packages on Ubuntu/Debian Linux. Let's install it using `apt` utility. 

First, updates the list of available packages and their versions.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> apt update </span>

After that, install the `figlet` program.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> apt install figlet </span>

Execute the following command again.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> figlet hello </span>

 Sample output:

 ```
 _          _ _       
| |__   ___| | | ___  
| '_ \ / _ \ | |/ _ \ 
| | | |  __/ | | (_) |
|_| |_|\___|_|_|\___/ 

```                  

Exit the docker container.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> exit </span>

Check the container status by executing:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> docker ps -a </span>

What is the status of the two containers that we have executed?

<br/>
