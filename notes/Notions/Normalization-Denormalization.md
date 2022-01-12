# Normalization and Denormalization (database)

## Normalization
Data is stored in **separate logical tables** and attempt to **minimize redundant data**. 
We may strive to have only one copy of each piece of data in database.

Usially **core data** is organized in one main table. Other data is on other tables.


!["alt"](../../images/normalization.png)

Has the **<span class="red">con</span>** of slowing down queries .


## Denormalization
Denormalization is a database **optimization technique** in which we add redundant data to one or more tables.

***Note that*** denormalization <u>does not mean not doing normalization</u>. It is an optimization technique that is applied **after doing normalization**.

**Pros:** 

1.  Retrieving data is faster since we do fewer joins
2.  Queries to retrieve can be simpler(and therefore less likely to have bugs),   
    since we need to look at fewer tables.

**Cons:**  

1.  Updates and inserts are more expensive.
2.  Denormalization can make update and insert code harder to write.
3.  Data may be inconsistent . Which is the “correct” value for a piece of data?
4.  Data redundancy necessitates more storage.