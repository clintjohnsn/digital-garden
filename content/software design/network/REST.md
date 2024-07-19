_representational state transfer_ (REST) architectural style

- independent of programming languages on client and server

## Design Principles
- uniform interface
	- All API requests for the same resource should look the same
- client-server decoupling
- statelessness
	- each request needs to include all the information necessary for processing it
	- no server side sessions
- cacheability
	- When possible, resources should be cacheable on the client or server side.
- layered system architecture
	- don’t assume that the client, and server applications connect directly to each other
	- need to be designed so that neither the client nor the server can tell whether it communicates with the end application or an intermediary.