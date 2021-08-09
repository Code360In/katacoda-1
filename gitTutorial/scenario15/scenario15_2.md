To edit the existing files in the repository, we can click on them in the “Files” panel on the lower right. Now let’s add some additional information about Pluto:
![Picture5](./assets/RStudio_screenshot_editfiles.png)

Once we have saved our edited files, we can use RStudio to commit the changes by clicking on “Commit…” in the Git menu:
![Picture6](./assets/RStudio_screenshot_commit.png)

This will open a dialogue where we can select which files to commit (by checking the appropriate boxes in the “Staged” column), and enter a commit message (in the upper right panel). The icons in the “Status” column indicate the current status of each file. Clicking on a file shows information about changes in the lower panel (using output of `git diff`). Once everything is the way we want it, we click “Commit”:
![Picture7](./assets/RStudio_screenshot_review.png)

The changes can be pushed by selecting “Push Branch” from the Git menu. There are also options to pull from the remote repository, and to view the commit history:
![Picture8](./assets/RStudio_screenshot_history.png)

------------

## Are the Push/Pull Commands Grayed Out?
Grayed out Push/Pull commands generally mean that RStudio doesn’t know the location of your remote repository (e.g. on GitHub). To fix this, open a terminal to the repository and enter the command: `git push -u origin main`{{copy}}. Then restart RStudio.

-----------

If we click on “History”, we can see a graphical version of what `git log` would tell us:
![Picture9](./assets/RStudio_screenshot_viewhistory.png)

RStudio creates a number of files that it uses to keep track of a project. We often don’t want to track these, in which case we add them to our `.gitignore` file:
![Picture10](./assets/RStudio_screenshot_gitignore.png)

There are many more features in the RStudio Git menu, but these should be enough to get you started!

---------------
## Key Points
- Using RStudio’s Git integration allows you to version control a project over time.

<br/>
