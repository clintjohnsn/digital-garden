Software design can be worked out either from top down approach (customer/user requirements/features → code → data) or from bottom up approach  (data → code → features).

# Process
## High Level Design
1. Define Requirements from user’s perspective
	1. product managers create **PRD** (Product Requirement Document) based on user feedback, data, market gaps
	2. Pick up the most important requirements
2. From the product requirements, extract features/abstract concepts and map them to **data definitions**, which then turn into **objects** in your database
3. define **APIs** through which data can be manipulated 
	1. consider [[Network Protocols]]
4. Consider **engineering requirements**
	1. availability, reliability, extensibility, fault tolerance, etc
	2. [[Estimation of scale]]
5. Testing the design
	1. test flow through scenarios
	2. identify bottlenecks

## Low Level Design
1. Consider 
	1. memory optimizations
	2. User behaviour
	3. API calling
	4. Concurrency
	5. Latency
	6. Throughput
2. Perform Data modeling - use case diagram leading to class diagrams/ER diagrams
3. write pseudocode

### Use Case Diagram
1. Define all the actors - users, stakeholders, operators, third party integrations, etc
2. Define requirements in terms of actions the actors can take
3. Convert the actions to objects → APIs and what services handle what
	1. The objects become the basis for class diagrams

### Class Diagram
1. Every class needs
	1. States
		- data that an object needs to perform behaviours
	2. Behaviour
