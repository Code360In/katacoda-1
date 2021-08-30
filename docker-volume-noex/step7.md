# Docker Volumes (II)

From the host machine,  modify the `index.html` as follows.

```
cat<<END >/var/lib/docker/volumes/web_folder/_data/index.html
<html>
	<body>
		Hello World!!!
	</body>
</html>
END
```{{execute}}


Verify that the website served by the Nginx container at localhost:8080 is updated.

> <span align="left" style="color:#FFF;background:#555;font:Courier New; font-size: 90%;"> curl localhost:8080 </span>

**Question:** 
What is the output of the curl command?

<br/>
