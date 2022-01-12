# Caching

> If a query is cached, you won't be charged

To retrieve data from stored cache, the query should be the **exact replica** of the original query.

It must have a size \<10Gb

<br/>

<span class="red">Not cached</span>:
- When the *destination table* is spcidied to **store results in in query**
- If tables/views have **changed**
- In tables with **streaming** ingestion
- If using **non-deterministic functions** like *timestamp(), now(), current_user()*
- Using **external data sources** like *BigTable or CloudStorage*