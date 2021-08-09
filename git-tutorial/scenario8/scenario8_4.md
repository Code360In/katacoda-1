Now that authentication is setup, we can return to the remote. This command will push the changes from our local repository to the repository on GitHub:
> `git push origin main`{{execute}}

Since Dracula set up a passphrase, it will prompt him for it. If you completed advanced settings for your authentication, it will not prompt for a passphrase.

After it is pushed, the following output is shown:
> ```
> Enumerating objects: 16, done.
> Counting objects: 100% (16/16), done.
> Delta compression using up to 8 threads.
> Compressing objects: 100% (11/11), done.
> Writing objects: 100% (16/16), 1.45 KiB | 372.00 KiB/s, done.
> Total 16 (delta 2), reused 0 (delta 0)
> remote: Resolving deltas: 100% (2/2), done.
> To https://github.com/vlad/planets.git
>  * [new branch]      main -> main
>  ```

Our local and remote repositories are now in this state:
![Picture9](./assets/github-repo-after-first-push.svg)

We can pull changes from the remote repository to the local one as well:
> `git pull origin main`{{execute}}

Pulling has no effect in this case because the two repositories are already synchronized. If someone else had pushed some changes to the repository on GitHub, though, this command would download them to our local repository.

## Proxy 
If the network you are connected to uses a proxy, there is a chance that your last command failed with “Could not resolve hostname” as the error message. To solve this issue, you need to tell Git about the proxy:
> ```
> git config --global http.proxy http://user:password@proxy.url
> git config --global https.proxy https://user:password@proxy.url
> ```{{execute}}

When you connect to another network that doesn’t use a proxy, you will need to tell Git to disable the proxy using:
> ```
> git config --global --unset http.proxy
> git config --global --unset https.proxy
> ```{{execute}}

<br/> 

## Password Managers
If your operating system has a password manager configured, `git push` will try to use it when it needs your username and password. For example, this is the default behavior for Git Bash on Windows. If you want to type your username and password at the terminal instead of using a password manager, type:

> `unset SSH_ASKPASS`{{execute}}

in the terminal, before you run `git push`. Despite the name, [Git uses SSH_ASKPASS for all credential entry](https://git-scm.com/docs/gitcredentials#_requesting_credentials), so you may want to unset `SSH_ASKPASS` whether you are using Git via SSH or https.

You may also want to add `unset SSH_ASKPASS` at the end of your `~/.bashrc` to make Git default to using the terminal for usernames and passwords.

## Uploading files directly in GitHub browser
Github also allows you to skip the command line and upload files directly to your repository without having to leave the browser. There are two options. First you can click the “Upload files” button in the toolbar at the top of the file tree. Or, you can drag and drop files from your desktop onto the file tree. You can read more about this on [this GitHub page](https://help.github.com/articles/adding-a-file-to-a-repository/).

## Key Points
- A local Git repository can be connected to one or more remote repositories.
- Use the SSH protocol to connect to remote repositories.
- `git push` copies changes from a local repository to a remote repository.
- `git pull` copies changes from a remote repository to a local repository.

<br/>
