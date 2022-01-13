# BigQuery
[[Serverless]], scalable cloud data warehouse

Has built-in BI Engine and Machine Learning

Uses SQL dialect 

Federated queries can process external data sources:
- [[Cloud Storage]]
- [[Cloud Bigtable]]
- Spreadsheets

Keeps 7 days history of history

Can analize big amounts of data in seconds

## [[Architecture]]
## [[UI]]
## [[Execution Plan|how Query Execution Plan works]]

## Query
[[Query settings]]
[[Caching]]
[[Wildcards]]: Enables to query **multiple tables at once** using concise SQL statements
[[Scheduled queries]] and backfilling
[[Saved queries]]

## Schemas
[[Automatic schema detection]]
[[Designing Efficient Schemas]] and [[Designing Efficient Schemas#Nested repeated data]]

## Dataset
[[Managing access]]
[[Copying dataset]]
[[Native operations on Table for Schema change]]
[[Manual operations on Table]]


## Table partitioning
[[Table partitioning]]
[[Ingestion time partition tables]]
[[Field partition]]

# Clustered Tables
[[Clustered Tables]]
[[When to use Clustering or Partitioning or Both]]
==todo== create clustered table
==todo== [[Clustered Tables#Do and Don'ts]]


## Loading & Querying External Data Sources
*It can be in BigTable, CloudStorage, ClousSQL, Google Drive...*

[[Create Cloud Storage bucket]]
[[Create & Query Permanent Table on Cloud Storage bucket]]
[[External data source Limitations]]

## [[Views]]
[[Materialized Views]]

## [[CLI]]

## [[Python lib]]

 [[Example of End-to-end Data Pipeline]]
 [[Build Streaming data pipelines]]

 ## [[Pricing]]

 ## [[Best practices]]