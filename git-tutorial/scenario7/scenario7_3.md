>> Q1. Given a directory structure that looks like: <br/> `results/data` <br/> `results/plots` <br/> What would you type in .gitignore file to ignore only `results/plots` and not `results/data`?<<
=== results/plots/

<br/> 

>> Q2. Let us assume you have many .dat files in different subdirectories of your repository. For example, you might have: <br/> `results/a.dat data/experiment_1/b.dat` <br/> `data/experiment_2/c.dat` <br/> `data/experiment_2/variation_1/d.dat` <br/> How do you ignore all the `.dat` files, without explicitly listing the names of the corresponding folders? <<
( ) /.dat
(*) **/*.dat
( ) */**.dat

<br/>
