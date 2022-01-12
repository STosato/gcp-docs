# Automatic schema detection
BigQuery:
1. selects a random file in source, 
2. scans *up to 100 rows* as a sample 
3. examinates each field and attempts to assign data type based on sample values

## Limitations
This feature is only avaiable for CSV and Json file format.

> **Note that:** all columns will be **nullable by default**. 
> Otherwise you will need to insert fields manually


## Headers
It infers headers by **comparing the first row** of the file with other rows.
If the first line contains only strings, and the other lines do not, BigQuery assumes that it is a header row.

Header is'nt taken into consideration while decidingthe schema of table.

## Dates
Must be in `YYYY-MM-DD` format

**Timestamps** can be:
- `hh:mm:ss YYYY-MM-DD`
- `YYYY-MM-DD hh:mm:ss.mm`