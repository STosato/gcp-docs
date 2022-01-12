# BigQuery CLI
> You can avoid the `bs` command by opening the "bigquery shell" using `bq shell`

### Showing main info
`bq show`

### Showing schema
`bq show -- schema dataset_name.names`


### Listing datasets
`bq ls`
## Execute SQL query
`bg query --use_legacy_sql=false <query>`
### Flags
**--append_table**
**--destination_table**
**--replace:** for overwriting destination table
**--destination_schema:** ir destination table doesn't exist, will be created with the specified schema
**--time_partitioning_field:** partitioning on some time (column name)
**--time_partitioning_type:** ingestion time *ie  day*
**--time_partitioning_expiration**
**--clustering_fields:** up to 4 comma separated columns to cluster
**--destination_kms_key:** resurce id of customer generated encryption key
**--batch:** batch mode
**--maximum_bytes_billed** 
**--label:** applying label to a query job
**--dry_run:** validator flag to check the correctness of a query and bytes to be processed
**--max_rows:** max rows to return
**--require_cache:** only run if can refer to cached results
**--use_cache:** set to `false` if not wanting to use cached results
**--schedule:** makes recurring scheduled query
**--display_name:** schedule's name
**--target_dataset:** destination table for scheduled queryes
**--flatten_results:** for nested and repeated fields


## Flags
```
bq --global_flag1=value .. command --command_spacific_flag1=value .... dataset.tablename
```


## --format
Format of command's output

- pretty
- sparse
- prettyjson
- json
- csv

## --job_id (commands creating job)
Giving a name to the job.

Used with *cp, load, extract..*

==skipping creating dataset and table==

# Cli Exclusive operations
## Making field nullable (relaking field)
```
bq load --schema_update_option ALLOW_FIELD_RELAXARION dataset_name.table_name <filepath> column_name:type,clumn2:type...
```

## Copying selected partitions of a table
```
bq cp -a dataset.origin_table$partition dataset.destination
```