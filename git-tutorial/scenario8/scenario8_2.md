The next step is to connect the two repositories. We do this by making the GitHub repository a [remote](https://swcarpentry.github.io/git-novice/reference.html#remote) for the local repository. The home page of the repository on GitHub includes the string we need to identify it:
![picture6](./assets/github-find-repo-string.png)

Click on the ‘SSH’ link to change the [protocol](https://swcarpentry.github.io/git-novice/reference.html#protocol) from HTTPS to SSH.
![picture7](./assets/github-change-repo-string.png)

We use SSH here because, while it requires some additional configuration, it is a security protocol widely used by many applications. The steps below describe SSH at a minimum level for GitHub. A supplemental episode to this lesson discusses advanced setup and concepts of SSH and key pairs, and other material supplemental to git related SSH.

Copy that URL from the browser, go into the local `planets` repository, and run this command in the terminal:
> `git remote add origin git@github.com:vlad/planets.git`{{copy}}
<b> Remember to change the SSH link to your own one. </b>

`origin` is a local name used to refer to the remote repository. It could be called anything, but `origin` is a convention that is often used by default in git and GitHub, so it’s helpful to stick with this unless there’s a reason not to.

We can check that the command has worked by running `git remote -v`:
> `git remote -v`{{execute}}

The output is like:
> ```
> origin   git@github.com:vlad/planets.git (fetch)
> origin   git@github.com:vlad/planets.git (push)
> ```

We’ll discuss remotes in more detail in the next episode, while talking about how they might be used for collaboration.

<br/>
