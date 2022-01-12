# Clustered Tables
Clustering or Bucketing i a data organization tecnique (*like partition*) for decomposing large datasets into more manageable ports.

Fundamental of it is that when table is bucketed in a column, then all the records with <u>same column name</u> will go to the **same bucket**.

### Example: salaries DB
Bucketing on **salary** column.

A bucket will contain <u>people with same salary</u> (<span class="purple">purple box</span>) and nowhere else

> ***Note:*** a bucket can contain multiple salaries values (<span class="orange">orange box</span>))

![[cluster-example.png]]

## Do and Don'ts
==section 8==


