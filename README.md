# SQL-error---secure-file-priv-solution
Here are some steps to solve the error  --secure-file-priv   while loading data into table

**********if we want to load data info sql table automatically by using query:**********
**********And we are getting error----->    --secure-file-priv        **********************
Follow a to h steps:
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
>>Querirs are
1) SHOW GLOBAL VARIABLES LIKE 'local_infile';
2)set global local_infile = 1;
3)OPT_LOCAL_INFILE=1
4)SET SESSION sql_mode = ""
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
a) Execute the ---->1) SHOW GLOBAL VARIABLES LIKE 'local_infile';    query first by pesting it  anywhere at workbench.
b) Execute the ---->2) set global local_infile = 1;       query first by pesting it  anywhere at workbench.
c) both the query should execute one by one.
d) Now completely close the workbench
e) open it again and "right click on--> local instance MYSQL80 box----> hit "edit the connection".
f) Go to Advance button----> others box-----> pest     OPT_LOCAL_INFILE=1    at bottom of others box(without deleting its old data)
g) After doing this  -----> 4)SET SESSION sql_mode = "" ----->  query execute.
h) If still same error is getting then-------> write---> local -----> In the query   LOAD DATA local INFILE 'E:\Dress Sales.csv'
