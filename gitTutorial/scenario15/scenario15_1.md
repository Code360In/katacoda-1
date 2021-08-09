Version control can be very useful when developing data analysis scripts. For that reason, the popular development environment [RStudio](https://www.rstudio.com/) for the R programming language has built-in integration with Git. While some advanced Git features still require the command-line, RStudio has a nice interface for many common Git operations.

RStudio allows us to create a [project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects) associated with a given directory to keep track of various related files. To be able to track the development of the project over time, to be able to revert to previous versions, and to collaborate with others, we version control the Rstudio project with Git. To get started using Git in RStudio, we create a new project:
![Picture1](./assets/RStudio_screenshot_newproject.png)

This will open a dialog asking us how we want to create the project. We have some options here. Let’s say that we want to use RStudio with the planets repository that we already made. Since that repository lives in a directory on our computer, we choose the option “Existing Directory”:
![Picture2](./assets/RStudio_screenshot_existingdirectory.png)

Next, RStudio will ask which existing directory we want to use. Click “Browse…” and navigate to the correct directory, then click “Create Project”:
![Picture3](./assets/RStudio_screenshot_navigateexisting.png)

Ta-da! We have created a new project in RStudio within the existing planets repository. Notice the vertical “Git” menu in the menu bar. RStudio has recognized that the current directory is a Git repository, and gives us a number of tools to use Git:
![Picture4](./assets/RStudio_screenshot_afterclone.png)

<br/>














