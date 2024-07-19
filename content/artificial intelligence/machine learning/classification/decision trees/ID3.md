# Iterative Dichotomizer 3

- tries to create a shallow tree
- greedy
- recursive depth first

### Algorithm
- choose best feature using [[Information Gain Ratio]] or some other metric, dont pick this feature again.
- partition dataset using selected feature (all possible branches)
- repeat until break condition

### Break condition
 - homogenous or pure set -> mark as classfication
 - no information gain if split
 - run out of features to split on