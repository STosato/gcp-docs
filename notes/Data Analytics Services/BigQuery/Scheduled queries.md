# Scheduled Queries

## Backfilling Mechanism
Running the queries for **previous dates** which the scheduled queries run may have <span class="red">got missed</span>.

### Example
Suppose having:
- a *source table* that is refreshed daily
- a *scheduled query* that runs every day that looks out the *source table* and <u>based on the current date</u> loads it to *another table*

If some day, *source table* is corrupted and <u>not populated</u> for the last 3 days.
Suppose you have **restored the last 3 days** on *source table*.

Is last three days data in the *another table* gone? **No**

**Backfill** allows us to run the query within a <u>pecified date range</u>

### Hou to use Backfill
 Go to BigQuery > Scheduled queries > More *(on top right of the page)* > Schedule backfill. (see image)

Here:
- **start date** is <span class="green">inclusive</span>
- **end date** is <span class="red">exclusive</span>

>***Note:*** here the dates must be in <span class="red">UTC</span>, but *queries schedules in dashboard* are in local timezone

 
!["alt"](../../Images/backfill.png)

 