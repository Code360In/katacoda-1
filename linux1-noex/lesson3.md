## Install software packages

To handle the procedures in using a software package, we will use `apt` command (a command line package manager) to operate: 
- Update list of available packages: `apt update`{{copy}}
- Install the package: `apt install <package name>`{{copy}}
- Uninstall the package: `apt remove <package name>`{{copy}}
- Update only a single app: `apt update <package name>`{{copy}}

<br/>

##### Example:
1. Update list of available packages: <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> apt update </span>

2. Install the package (here we install nginx web server). Enter <kbd> Y </kbd> when asked: <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> apt install nginx </span>

3. Run the nginx web server: <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> nginx </span>

4. Check the default website using `curl`: <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> curl localhost:80 </span>

<br/>

Sample output:

![Picture 3](./assets/pic3.png)

<br/>

You can try to look upon each package available by:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> apt list </span>

Also, you can search the details of a particular package by:
> `apt show <package name>`

For example, we can find the details of **nginx** package:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> apt show nginx </span>

<br/>
