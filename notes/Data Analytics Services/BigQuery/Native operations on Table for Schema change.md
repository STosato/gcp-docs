# Native operations on Table for Schema change

By using the BigQuery's UI ("Edit Schema" button) you can do only limited  of table schema changes:

## Adding new fields
Them can only be:
- nullable
- repeated

<u>required</u> ones <u>arent'possible</u>

### Updating existing data with new fields values
Can be done by "create table" with the **same name as the destination table** and setting.

In **Advanced Options**, set **write preferences** as <u>overwrite table</u>. So the **table will be updated**.

> You'll need to insert the new schema when creating the "new" table

### Appending rows
Same as updating but in **advanced options**, set **append**.

