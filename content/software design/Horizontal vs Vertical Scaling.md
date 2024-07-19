### Horizontal Scaling
- typically, [[Load Balancing]] is required
- more resilient and **reliable**
- typically requires more network calls ([[RPC]]s)
- Data **inconsistency** is possible
- unlimited scaling

### Vertical Scaling
- single point of failure
- faster inter process communication because of lesser [[RPC]]s 
- data **consistency** is maintained
- there are hardware limits to scaling

> Usually, a combination of both are used IRL