>> Q1. Jennifer has made changes to the Python script that she has been working on for weeks, and the modifications she made this morning “broke” the script and it no longer runs. She has spent ~ 1hr trying to fix it, with no luck… Luckily, she has been keeping track of her project’s versions using Git! Which commands below will let her recover the last committed version of her Python script called `data_cruncher.py`?<<
<br/><br/>
( ) $ git checkout HEAD
( ) $ git checkout HEAD data_cruncher.py
( ) $ git checkout HEAD~1 data_cruncher.py
( ) $ git checkout <unique ID of last commit> data_cruncher.py
(*) Both 2 and 4

<br/>

>>Q2: What is the output of the last command in <br/>$ cd planets <br/> $ echo "Venus is beautiful and full of love" > venus.txt <br/> $ git add venus.txt <br/> $ echo "Venus is too hot to be suitable as a base" >> venus.txt <br/> $ git commit -m "Comment on Venus as an unsuitable base" <br/> $ git checkout HEAD venus.txt <br/> $ cat venus.txt #this will print the contents of venus.txt to the screen<<
<br/><br/>
( ) `Venus is too hot to be suitable as a base`
(*) `Venus is beautiful and full of love`
( ) `Venus is beautiful and full of love
    Venus is too hot to be suitable as a base`
( ) `Error because you have changed venus.txt without committing the changes`
      
<br/>     
