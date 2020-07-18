---
title: "How Save Select Query Result as Csv Mysql"
date: 2020-03-27T01:26:26+05:30
draft: false
tags:
- MySql
---

MySql `SELECT ... INTO` command saves query result in to a valriable or file.

We will use it to save select query result to a `csv`  file.

the following code snippet will save the query result to a file `output.cs`. 

```
SELECT * FROM POST 
INTO OUTFILE '/var/lib/mysql-files/output.csv'
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n';
```