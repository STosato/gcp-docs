# Ingestion time partition tables
> Data inserted today will remain in today's partition.

When selecting pseudo-columns, you must use **aliases**.


- `_PARTITIONTIME`
- `_PARTITIONDATE`

## Getting summary

```sql
SELECT * FROM [dataset.table$__PARTITIONS_SUMMARY__]
```

