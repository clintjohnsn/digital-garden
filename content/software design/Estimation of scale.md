What to consider when estimating scale in system design

1. Traffic Estimation
	1. requests in queries per second
		- how many daily users?
			- how are the users distributed geographically?
			- what are going to be the peak hours 
			- from this data, estimate concurrent users
			- how many requests per sec per user?
			- from this data calculate total requests per sec during peak hours.
		- throughput of data ingestion
			- how often and how much of data is expected to be ingested from the source.
	2.  read-write ratio
		- which of the data and related objects/services are read intensive, which are write intensive, and what is the ratio?
	3. bandwidth
		- scale of read-write actions on servers, databases
		- network bandwidth for data ingestion, output, integrations, pipelines, etc
		- user bandwidth expectation
2. Storage Estimation
	1. how much total data is generated and  where is what stored? databases/caches/archival/data warehouses/lakes
	2. what is the data retention policy?
	3. logging and analytics data. 