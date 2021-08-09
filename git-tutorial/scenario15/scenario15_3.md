## Do You See a “Version Control” Option?

Although we’re not going to use it here, there should be a “version control” option on this menu. That is what you would click on if you wanted to create a project on your computer by cloning a repository from GitHub. If that option is not present, it probably means that RStudio doesn’t know where your Git executable is, and you won’t be able to progress further in this lesson until you tell RStudio where it is.

<b> Find your Git Executiable </b>
First let’s make sure that Git is installed on your computer. Open your shell on Mac or Linux, or on Windows open the command prompt and then type:
- `which git` (Mac, Linux)
- `where git` (Windows)

If there is no version of Git on your computer, please follow the [Git installation instructions](https://swcarpentry.github.io/git-novice/setup.html) in the setup of this lesson to install Git now. Next open your shell or command prompt and type `which git` (Mac, Linux), or `where git` (Windows). Copy the path to the git executable.

e.g. On one Windows computer which had GitHub Desktop installed on it, the path was: `C:/Users/UserName/AppData/Local/GitHubDesktop/app-1.1.1/resources/app/git/cmd/git.exe`

NOTE: The path on your computer will be somewhat different.

<b> Tell RStudio where to find GitHub </b>
In RStudio, go to the `Tools` menu > `Global Options` > `Git/SVN` and then browse to the git executable you found in the command prompt or shell. Now restart RStudio. Note: Even if you have Git installed, you may need to accept the XCode license if you are using macOS.

<br/>
