## Debian, Ubuntu, Mint, and others
Debian, Ubuntu, Mint, and other Debian-based distributions all use `.deb` files and the dpkg package management system. There are two ways to install apps via this system. You can use the apt application to install from a repository, or you can use the `dpkg` app to install apps from `.deb` files. Let's take a look at how to do both.

Installing apps using `apt` is as easy as: 
> `apt install app_name`{{copy}}

Uninstalling an app via apt is also super easy:
> `apt remove app_name`{{copy}}
  
To upgrade your installed apps, you'll first need to update the app repository:
> `apt update`{{copy}}

Once finished, you can update any apps that need updating with the following:
> `apt upgrade`{{copy}}

What if you want to update only a single app? No problem.
> `apt update app_name`{{copy}}

Finally, let's say the app you want to install is not available in the Debian repository, but it is available as a .deb download. You can install it manually using dpkg, the system that apt helps manage:
> `dpkg -i app_name.deb`{{copy}}

As you can see, installing, uninstalling, and updating Linux apps from the command line isn't hard at all. In fact, once you get used to it, you'll find it's faster than using desktop GUI-based management tools!

For more information on installing apps from the command line, please visit the Debian [Apt wiki](https://wiki.debian.org/Apt), the [Yum cheat sheet](https://access.redhat.com/articles/yum-cheat-sheet), and the [DNF wiki](https://fedoraproject.org/wiki/DNF?rd=Dnf).

<br/>
