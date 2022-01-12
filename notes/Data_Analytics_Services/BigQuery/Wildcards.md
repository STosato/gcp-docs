# Wildcards
Enables to query **multiple tables at once** using **concise SQL statements**.

Them are just **representation of union** of all the tables matching a particular wildcard espression.

Can be used for tables with:
- similar schema
- same prefix

![[Pasted image 20211230173741.png]]

### Practical example
If having a dataset containing tables with the same schema for every year. say:

*weather2000, weather2001, ... , weather2021*

you can use
```SQL
SELECT ...
FROM `dataset.weather200`
```
to get the union from years 2000 to 2009

## Filtering by suffix
```SQL
SELECT ...
FROM <wildcard>
WHERE _TABLE_SUFFIX = <wanted suffix>
```


## Limitations

1. Supports Big Query storage only. 
    <span class="red">Are not allowed:</span>.
	- <span class="red">External tables</span>
	- <span class="red">Views</span>, even if in a list of tables
2. Chached results are not supported. Every query will be billed
3. Can't be used in Insert/delete/update statements. But it is possible to use wildcards in the `WHERE`
