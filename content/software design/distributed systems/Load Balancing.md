Technique used in [[Distributed Systems]] to distribute incoming network traffic or workload across multiple servers or resources. 

Load balancers can be put between
- user & server
- internal platform layers/ between microservices
- backend servers & cache
- backend servers & DB
## Why Load Balancers?
- more throughput
- less wait times/ response times
- optimize resource utilization and avoid overload
- increased **reliability**
- smart load balancers predict traffic beforehand to scale
## Algorithms
Typically, health checks are performed constantly to add/remove works to the pool

1. **Least Connection** Method
	- direct traffic to the worker with fewest active connections
	- good for persistent connections
2.  **Least Response Time** Method
	- direct traffic to the lowest average response time worker
3. **Least Bandwidth** Method
	- direct traffic to the worker currently serving least amount of traffic
4. **Round Robin** Method
	- go around workers
5. **Weighted Round Robin** Method
	- weighted on the performance capability, most capable worker is weighted more
	- more of the connections are sent to the higher weights
6. **IP Hash** Method
	- Take IP/cookie/user Id or some other identifier on the client side & hash it to determine which worker it goes to
	- this lets worker caches to be used effectively, as a client will always connect to the same worker
	- use [[Consistent Hashing]]

## Redundant Load Balancers
Keep a redundant load balancer in addition to the active one as a backup in a cluster → eliminate single point of failure at the load balancer

## Stateful Load Balancers
- unlike stateless load balancers, stateful load balancers maintain state with session information
- once a user/session is directed to a worker, subsequent requests are also directed to the same server



