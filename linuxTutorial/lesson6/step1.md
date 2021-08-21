## Install software packages

To handle the procedures in using a software package, we will use `apt` command (a command line package manager) to operate: 
- Update list of available packages: `apt update`{{copy}}
- Install the package: `apt install <package name>`{{copy}}
- Uninstall the package: `apt remove <package name>`{{copy}}
- Update only a single app: `apt update <package name>`{{copy}}

<br/>

#### Example:
1. Update list of available packages: `apt update`{{execute}}
2. Install the package (here we install nginx web server): `apt install nginx`{{execute}}
3. Run the nginx web server: `nginx`{{execute}}
4. Check the default website using `curl`: `curl localhost:80`{{execute}}


<br/>
