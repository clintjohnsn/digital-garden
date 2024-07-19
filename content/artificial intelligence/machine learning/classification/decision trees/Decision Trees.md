build predictive models using the most informative features

interior nodes -> query on some descriptive feature of the dataset
leaf nodes -> decision/predicted classification/predicted value

shallow trees >>
- prevent [[Overfitting]]

informative features split the dataset into more homogenous or pure sets.


## Measures of purity
- entropy & information gain
- information gain ratio
- gini index
- variance

### [[Entropy]]

![[Entropy]]
### [[Information Gain]]

[[Kullback–Leibler divergence]]


![[Information Gain]]
### [[Information Gain Ratio]]
Information Gain has a preference for features with many values

Information Gain Ratio divides information gain with the amount of information used to determine the value of the feature
![[Information Gain Ratio]]

### [[Gini Index]]

![[Gini Index]]

### Variance
![[Variance]]

- Used for regression trees

![[Variance for Regression Trees]]

### Continuous Descriptive features

- preprocessing like binning
- turn into Boolean features using some threshold value
	- < threshold value and >= threshold value
	- sort the dataset according to the continuous feature
	- adjacent instances with different y are possible threshold values 
		- threshold value -> lies between the continuous feature value of the two instances {((x2 - x1)/2) + x1}
	- optimal threshold - compute information gain (or other measure) for each split and select the split with highest information gain

### Algorithm
- [[ID3]]
- [[CART]]
both are greedy algos, they don't check whether the best possible splits at a high level lead to lowest possible impurity at lower levels.

## [[Overfitting]]
The likelihood of over-fitting occurring increases as a tree gets deeper because the resulting classifications are based on smaller and smaller subsets as the dataset is partitioned after each feature test in the path.

- [[Pruning]]

## [[Ensemble Decision Trees]]
