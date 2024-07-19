- based on the principle of [[Locality of Reference]]
- store copies of frequently accessed or computationally expensive data in a **cache** to improve performance
- can be used at all levels of architecture  - frontend & backend

## Global and distributed caches
When caching at a node level in [[Distributed Systems]], if the load balancer ([[Load Balancing]]) randomly distributes requests, it leads to increased cache misses. The solution in such scenarios is to use global or [[Distributed Caches]].

## Cache Invalidation
Process of removing or updating stale cached data in a cache system to ensure that the data remains coherent with the source of truth.
### Write-Around Cache
- write to database, bypassing cache
- leads to higher cache miss → higher latency for recently updated data
- cache invalidation 
	- **time-based expiration**: invalidate cache after a time
	- **event-based invalidation**: throw event after database write
### Write-Through Cache
- write both in cache and database for every write operation
- no issues in case of any system interruption
- higher latency for write operations
### Write-Back Cache
- write to cache alone and send back confirmation to client
- write to database after some set intervals
- low latency for **write-intensive apps**
- risk of data loss - since the data is only in the cache for some time, cache is the only source of truth

## Cache Eviction Policies
- [[FIFO]]: First In First Out
- [[LIFO]]: Last In First Out
- [[LRU]]: Least Recently Used
- [[LFU]] : Least Frequently Used
- Random Replacement