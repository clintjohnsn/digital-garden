- iteratively create and add models to an ensemble
	- combine several weak learners into a strong learner
	- train predictors sequentially
- each new model is biased to pay more attention to instances that previous models misclassified
	- weighted dataset
- avoid [[Underfitting]]
### Weighted dataset
- each instance has associated weight > 0
- initially set to 1/n
- test model on **training data** 
	- weights of instances model gets correct decreased
	- weights of instances model gets incorrect increased
- weights -> distribution over which the dataset is sampled to create a replicated training dataset 
	- replication is proportional to weight

## Aggregation
weighted averaging