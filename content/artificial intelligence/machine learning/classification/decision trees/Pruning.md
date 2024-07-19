Prevent overfitting in decision trees

## Pre-pruning
or **forward pruning**
	- stop during tree creation if information gain is not sufficient
	- some prefixed tree depth
[[Horizon effect]]


## post-pruning
-  prune after the tree is created 
- use validation set to evaluate predication accuracy, if pruned copy of the tree does not perform worse than original tree, keep the pruned copy

- Top down
	- start at root, drop entire subtrees, might drop relevant sub trees
	- [[Pessimistic Error Pruning (PEP) ]]
- Bottom up
	- start at last nodes, does not drop relevant sub trees
	- [[Reduced Error Pruning (REP)]], [[Minimum Cost Complexity Pruning (MCCP)]], or [[Minimum Error Pruning (MEP)]]
