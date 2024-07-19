## Algorithm
- select **k** clusters
- initialize a random **k** points as cluster means
	- randomize, or
	- **k** uniformly distributed within the range of distribution, or
	- perform k-means on a subset of data and use the result as the initial means
- assign each point to the nearest mean
- recompute the mean of each cluster
- repeat till **convergence** 
	- when the means stop moving, or 
	- change in means < some threshold

### How to pick K?
1. **Elbow method**: Plot the cost (sum of squared distances from each point to its cluster centroid) for different values of **k**. The optimal **k** is the "elbow" point where the cost starts decreasing linearly
2. **Silhouette Analysis**: measures how well it fits into its assigned cluster compared to other clusters
3. **Calinski-Harabasz Index**:  ratio of the between-cluster dispersion and the within-cluster dispersion. Scales better, as each pair distance is not needed.
4. **Davies-Bouldin Index**: measures the average similarity between each cluster and its most similar one. Scales better, as each pair distance is not needed.
5. **Dunn Index**:  calculates the ratio of the smallest inter-cluster distance to the largest intra-cluster distance

### Cons
- need to pick k
- sensitive to initialization
- sensitive to outliers

### Scale
- [[MiniBatchKMeans]]