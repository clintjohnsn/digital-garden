A modular architecture in which an application is divided into smaller, independent services that are **loosely coupled** and communicate with each other through APIs. Typically, each microservice is responsible for a specific function or feature of the application, and can be developed, deployed, and scaled independently. 

This modular architecture allows for greater flexibility, scalability, and maintainability compared to traditional monolithic applications. 

## Why microservices?

- **Scalability** 
	-  scalable at a service level - meaning the whole system need not scale for a particular service. 
	- The scalability achieved is also flexible and on-demand
- **Maintainability**
	- Easy to onboard new developers
	- allows parallel development, deployment and testing
	- service level debugging
- **Reliability**
	- fault tolerant - no single point of failure
	- resilient if designed well, can pick up where it failed
- **Availability**
	- through horizontal scaling

> See also [[Distributed Systems#Why distributed systems?]]

## Why not microservices?
- harder to design
- might be overkill for small teams
- lots of moving parts - increases system complexity for understanding and management
- typically slower than monoliths, because of [[RPC]]s/API calls over the network
- code duplication - classes/objects may be shared, More APIs & RPCs are needed,  common functionalities might need to be shared