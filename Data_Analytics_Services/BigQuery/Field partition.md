# Field partition

## Null/wrong format
In the partition summary:
`partition_id` will have `_NULL_` or `_UNPARTITIONED_`

### Unpartitioned list
```
SELECT * FROM [dataset.table$__UNPARTITIONED__]
```