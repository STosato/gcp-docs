# NoSQL

## Why should you use a NoSQL database?

NoSQL databases are a great fit for many modern applications such as mobile, web, and gaming that require flexible, scalable, high-performance, and highly functional databases to provide great user experiences.

-   **Flexibility:** NoSQL databases generally provide flexible schemas that enable faster and more iterative development. The flexible data model makes NoSQL databases ideal for semi-structured and unstructured data.
-   **Scalability:** NoSQL databases are generally designed to scale out by using distributed clusters of hardware instead of scaling up by adding expensive and robust servers. Some cloud providers handle these operations behind-the-scenes as a fully managed service.
-   **High-performance:** NoSQL database are optimized for specific data models and access patterns that enable higher performance than trying to accomplish similar functionality with relational databases.
-   **Highly functional:** NoSQL databases provide highly functional APIs and data types that are purpose built for each of their respective data models.

## Example: Simple book database
### Relational Database
A book record is often dissembled (or “normalized”) and stored in **separate tables**
**Relationships** are defined by primary and foreign key constraints.

The relational model is designed to enable the database to:
- enforce referential integrity between tables in the database
- normalized to reduce the redundancy
- generally optimized for storage

**Books table** has columns for **ISBN**, **Book Title**, and **Edition Number**,
**Authors** table has columns for **AuthorID** and **Author Name**, 
**Author-ISBN** table has columns for **AuthorID** and **ISBN**


### NoSQL 
A book record is usually stored in a **JSON** document

Data is optimized for intuitive development and horizontal scalability

the item, **ISBN**, **Book Title**, **Edition Number**, **Author Name**, and **AuthorID** are stored as attributes in a single document

-----see "# SQL (relational) vs. NoSQL (nonrelational) databases"  https://aws.amazon.com/nosql/?nc1=h_ls -----