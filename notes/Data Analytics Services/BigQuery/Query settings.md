# Query settings
- [[Streaming data]]: for data outside google *pub/sub, Cloud Dataflow*
- **Destination**:
	- **tamporary table**: randomly named, saved in a special dataset. 
		- Not sharable
		- not queryable
		- duration of 24 hours
	- permanent table 
- **Job priority**:
	- **Interactive**: <span class="green">running immediately</span>
	- **Batch**: <span class="orange">starts as soon as idle resources are avaiable</span> (few miutes). When available, queries can be done concurrently

## Blocking too heavy queries ($) 
You can set the **[[Maximum bytes billed]]** field to execute only the values with less bytes. 
