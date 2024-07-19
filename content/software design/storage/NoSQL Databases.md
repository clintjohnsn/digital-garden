- **flexible schema**, add or remove columns with ease
- great for sparse data
- **horizontally scalable**
- not [[ACID]] compliant
- can store any **type of data** in one place
- great when transactional data is not important, but ease of fetching complex data structures is required


## Types
1. **Key-value** stores
	1. great for fetching key-value pairs efficiently - 
		- caching
	2. Dynamo, Redis, …
3. **Document** databases
	1. documents with different structures grouped into collections
	2. MongoDB, CouchDB, …
4. **Wide-Column** databases
	2. Casandra, HBase,  …
6. **Graph** databases
	1. entities are nodes with properties, edges connect entities based on relationships 
	2. Neo4J, InfiniteGraph, …
