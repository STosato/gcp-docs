# Materialized Views
Compared to normal views :
- occupy **disk space**
- are **pre-computed**, so they don't refer to base tables.
- Data can be manually or auto refreshed
- <span class="green">are faster</span>: normal ones firstly are applied to base tables. Instead, material ones are pre-computed
- **smart tuning**: if a query can be served with an already created materialized view, this will be done
## Example
![[creating_materialized-view.png]]
## Create a Materialized view
Simply by using `CREATE MATERIALIZED VIEW name AS ...`

- **aggregation functions** must reference a <span class="red">**single table** only</span>
- <span class="red">No **joins**</span>

Supports only fiew aggregation functions:
-   `ANY_VALUE` (but not over `STRUCT`)
-   `APPROX_COUNT_DISTINCT`
-   `ARRAY_AGG` (but not over `ARRAY` or `STRUCT`)
-   `AVG`
-   `BIT_AND`
-   `BIT_OR`
-   `BIT_XOR`
-   `COUNT`
-   `COUNTIF`
-   `HLL_COUNT.INIT`
-   `LOGICAL_AND`
-   `LOGICAL_OR`
-   `MAX`
-   `MIN`
-   `SUM`

Other infos:
- can be partitioned and clustered
- can be manipulated only by `CREATE, DROP, ALTER`


## How to write optimized materialized views
- Avoiding filtering or computations

## Manual refresh
`CALL BQ.REFRESH_MATERIALIZED_VIEW('view_name'`

## Set auto-refresh
When creating a view
`OPTION (enable_refresh = true)`

or with **ALTER**
`ALTER MATERIALIZED VIEW view_name SET OPTIONS(enable_refresh = true) `

### Interval of refresh
you can add `refresh_interval_minutes=60`

## Limitations
- can't copy with jobs
- Can't export data
- can't load data in it with load query
- can't use DML statements over ita
- should have the same dataset location
- limited aggregation functions
- reference limited to **one single table**
- can't nest other materialized views
- onli standard SQL can be used
- max 20 for base table

