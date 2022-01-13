 # GCP Database Services

Relies on **NoSQL** databases
Multi-region distribution
It has in-memory database used for accelerating the performances

## Google Cloud SQL
**Fully managed** [[RDBMS]] that simplifies the setup and mantainance.

Supports 3 types of RDBMS:
- MySQL
- PostgreSQL
- Microsoft SQL Server

It delivers scalability, security and reliability of DB instances

## Google Cloud Big Table
Managed [[NoSQL]] database service

Ideal for:
- Large scale & low latency applications
- throughput intensive data processing and analytics

Is an alternative to Apache HBase column-oriented DB

## Google Cloud Spanner
Managed & scalable **Relational DB** (and NOSQL) for **regional and global** application data

It **horizontally scales** across rows, regions and continents

Data is replicated synchronously

Its instances can be:
- R/W
- Read only
- Witness: checks consistency


## Google Cloud Memorystore
Fully-managed [[in-memory data store]] service for [[Redis]].

Are ideal for applications caches providing sub-millisecond data access.

Promises 99.9% availability with automatic [[failover]]

## Use Cases
!["alt"](images/db_services_usecases.png)