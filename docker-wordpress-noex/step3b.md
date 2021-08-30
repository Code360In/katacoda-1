
# Exploring the MySQL Server container

Start a bash shell into the msyql container

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> docker exec -it mysql bash </span>

Login to the mysql database server using the `wordpress` account.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> mysql -u wordpress -p </span>

Input `12345` as password.

To show the databases, execute:

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> show databases; </span>

Change to the `wordpress` database. Execute:

> `use wordpress`{{execute}}

To list all the tables, execute:

> `show full tables;`{{execute}}

To describe and get data from the `wp_posts` table, execute:

> `describe wp_posts`{{execute}}

> `select ID, post_title, post_author, post_date from wp_posts;`{{execute}}

Exit the mysql client.

> `exit`{{execute}}

Exit the `mysql` container.

> `exit`{{execute}}

