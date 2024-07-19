[[think globally, fit locally]]

**Stage 1**: learn reconstructing one data point with its neighboring points via linear parametric model.
find Neighbors via-
-  [[ϵ-neighborhood]] : connect each point to all points within a fixed radius ϵ.  
- [[k-nearest neighbors algorithm (k-NN)]] : connect each point to all of its K nearest neighbours

**Stage 2**: learn embedding coordinates by reconstructing one data point with its neighboring points linearly in low-dimensional representational space with those parameters learned in Stage 1

> K and ϵ become hyperparameters

![[Pasted image 20240124051222.png]]
## Limitation
- data points have to be sampled from the manifold uniformly
- Sensitive to noisy sampling and the hyperparameter, K or ϵ
- Unlike [[Isometric Feature Mapping (ISOMAP)]], LLE does not make any assumption on manifolds being convex but may not be able to recover complex non-convex manifold. [[Convex set]]
- Unlike ISOMAP, no robust way to decide the intrinsic dimension of embedding space -  **[[Proportion of Variance]]** does not work
-  ![[MDS Extensions#Out of sample extension]]
### [[LLE Extensions]]