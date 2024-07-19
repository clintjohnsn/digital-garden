
Computer systems composed of multiple interconnected computers that communicate and coordinate their actions through message passing to achieve a common goal. Examples -  [[Microservices]], cloud-computing platforms, peer-to-peer networks, [[Blockchains]] and [[Distributed Databases]].

## Why distributed systems?

1. **Scalable**
	1. can handle large data volumes and number of transactions
2. **Reliable/Resilient**
	1. Reliability is a measure of the probability that a system will fail in a given period
	2. ensuring that the system doesn't go down
	3. eliminate every single point of failure - i.e. being **fault tolerant**
		- this is done through **redundancy/replication** of both components and data
		-  Replication means sharing information to ensure consistency between redundant resources, such as software or hardware components, to improve reliability, fault-tolerance, or accessibility
3. **Available**
	1. measure of the percentage of time that a system, service, or a machine remains operational under normal conditions
	2. i.e. no downtime, operational 100% of the time 
	4. Reliability often implies Availability, but not necessarily other way around
4. **Efficient**
	1. Latency/ Response time: delay to obtain first item
	2. Throughput/ bandwidth: no of items delivered in a time unit
5. **Manageability/Maintainability**
	1. Ease of operation and maintenance
	2. Ease of diagnosis - observability through traces and logs
	3. Easy to update - code and infrastructure updates
6. **Modularity and flexibility**
	1. to an extent - though that is not the main goal.

> See also [[Evaluation of Software Systems]]

## Tradeoffs
[[CAP Theorem]]
