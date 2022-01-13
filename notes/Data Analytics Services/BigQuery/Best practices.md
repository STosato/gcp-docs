# Best Practices

## Performance and cost factors
- How many bytes are read from query
- Shuffling: how many bytes does your query pass to each slot
- Computation: CPU times
- Outputs: how many bytes are written

## Reducing bytes read
- Avoid `SELECT *`
- `LIMIT` does not limit data scanned. Use "[[Maximum bytes billed]]" in query settings instead
- Use partitioning or clustering
- Use [[Normalization-Denormalization|denormalization]]
- Use [[Materialized Views]] to keep aggregated data
- Use cached results
- Avoid external data source

## SQL best practices
- Avoid **self joins** use [[Window function]] instead
- Avoid **cross joins**, pre aggregate data or use [[Window function]]
- Avoid DML single row modifications

