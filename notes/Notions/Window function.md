# SQL Window Function
Performs calculations on a set of rows that are related together. 

But, <u>unlike the aggregate functions</u>, windowing functions **do not collapse the result** of the rows into a single value. 
Instead, all the rows **maintain their original identity** and the calculated **result is returned for every row**.

!["alt"](../Images/SQL-Window_fn.png)

## Windowing with PARTITION BY

The **PARTITION BY** clause is used in conjunction with the OVER clause. It breaks up the rows into different partitions. These partitions are then acted upon by the window function.

For example, to display the total salary per job category for all the rows we would have to modify our original SQL query as follows:

!["alt"](../Images/SQL-window_fn2.png)

## Arranging Rows within Partitions

We know that to arrange rows in a table, we can use the ORDER BY clause. So, to arrange rows within each partition, we have to modify the OVER clause with the ORDER BY clause.

!["alt"](../Images/SQL-window_fn3.png)

## Window functions

[More at](https://www.analyticsvidhya.com/blog/2020/12/window-function-a-must-know-sql-concept/#h2_10)