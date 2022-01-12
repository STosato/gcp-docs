# Pricing
https://cloud.google.com/products/calculator
## Storage
Two types:

**Active storage**= table/partition that has been modified in past 90 days.
Usually 0,02$ per month but <u>first 10Gb are free every month</u>

**Long term storage**: data is not been modified in past 90 days.
Discounted 50% off.
<u>Pro:</u> works also for partitions, if only one is active, the others will remain long-term.


## Queries run

**On-demand** (default): charges only when the query is run. Charges are decided by <u>number of bytes scanned</u>
Usually from 5$ (multi-region) to 9$ per Tb. <u>first 1 Tb are free every month</u> 

**Flat-rate**: pay upfront to get a desired number of dedicated resources/slots for month/year

## Free ops
- copy/delete/export table
- loading from Cloud storage or Local files