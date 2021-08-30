## Creation of folders

First we can use `mkdir` command to create a folder:
> `mkdir helloworld`{{execute}}

Check that the folder is created:
> `ls`{{execute}}

You may create more than one folder by specifying more than one arguments:
> `mkdir dir1 dir2 dir3`{{execute}}

Check the created folders by using `ls`:
> `ls`{{execute}}

The `mkdir` command accepts an option `-p` which creates parent directories as needed. For instance, the following command will first create **dir4** and then create **dir5** inside the **dir4** folder:
> `mkdir -p dir4/dir5`{{execute}}

Check the created directories. You can see there are only **helloworld**, **dir1**, **dir2**, **dir3** and **dir4**:
> `ls`{{execute}}

Check the created directory within **dir4**. You can see **dir5** inside:
> `ls dir4`{{execute}}

<br/>

