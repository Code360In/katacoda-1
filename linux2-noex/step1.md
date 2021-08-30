## Creation of folders

First we can use `mkdir` command to create a folder:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> mkdir helloworld </span>

Check that the folder is created:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> ls </span>

You may create more than one folder by specifying more than one arguments:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> mkdir dir1 dir2 dir3 </span>

Check the created folders by using `ls`:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> ls </span>

The `mkdir` command accepts an option `-p` which creates parent directories as needed. For instance, the following command will first create **dir4** and then create **dir5** inside the **dir4** folder:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> mkdir -p dir4/dir5 </span>

Check the created directories. You can see there are only **helloworld**, **dir1**, **dir2**, **dir3** and **dir4**:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> ls </span>

Check the created directory within **dir4**. You can see **dir5** inside:
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%; padding-left: 5px; padding-right: 5px; padding-top: 5px; padding-bottom: 5px;"> ls dir4 </span>

<br/>

