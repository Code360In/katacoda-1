
# Exploring the MySQL Server container

Start a bash shell into the msyql container

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker exec -it mysql bash </span>

Login to the mysql database server using the `wordpress` account.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> mysql -u wordpress -p </span>

Input `12345` as password.

To show the databases, execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> show databases; </span>

Change to the `wordpress` database. Execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> use wordpress; </span>

To list all the tables, execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> show full tables; </span>

**\*Note\***: You should first complete the installation of wordpress in the previous step to view the wordpress tables.

To describe and get data from the `wp_posts` table, execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> describe wp_posts; </span>
>
> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> select ID, post_title, post_author, post_date from wp_posts; </span>

Exit the mysql client.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> exit </span>

Exit the `mysql` container.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> exit </span>

<br/>
