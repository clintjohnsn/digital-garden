**homeomorphic** property of [[Manifold]] allows for an approximation of proper [[geodesic distance]] via the use of [[euclidean space]] locally. 

> see [[homeomorphism]]

**ISOMAP** : apply [[Classical MDS (cMDS)]] to the **geodesic distance matrix**, which is approximated by a sequence of steps (Euclidean) on relevant groups of neighboring points

### Geodesic distance matrix
Data set is represented as weighted graph where data points are treated as nodes and weights on edges are approximated geodesic distances
## Algorithm

1. **Construct neighborhood graph**: Determine neighbors based on Euclidean distances. Set edge length equal to δ(i,j)
	- **ϵ-ISOMAP** : 
		- [[ϵ-neighborhood]]
		- connect each point to all points within a fixed radius ϵ.  
	- **K-ISOMAP**: 
		- [[k-nearest neighbors algorithm (k-NN)]]
		- connect each point to all of its **K** nearest neighbors
1. Approximate the geodesic distances for non-neighbors by estimating their **shortest-path distance** in the weighted graph. 
	- [[Dijkstra Algorithm]] 
		- For k = 1, · · ·,N, replace all entries δG(i, j) by min {δG(i, j), δG(i, k) + δG(k, j)}
2. Convert the geodesic distance matrix into the [[Gram matrix]]
3. Apply [[Classical MDS (cMDS)]]

> K and ϵ become hyperparameters.
> If **cMDS** is used, then [[Proportion of Variance]] can be used to find optimum intrinsic dimensionality
### Manifold Interpolations
Can be used in manifold interpolations - Linear interpolations in low dimensional ISOMAP feature space and Nonlinear interpolations in high dimensional space

## Limitations
- sufficient data points - manifold must be smooth
- Work only on **convex Euclidean manifolds** to recover the intrinsic geometry, 
	- e.g. for 2-D manifolds coming from any physical transformations such as folding, twisting and curving a sheet of paper without tears, holes, or self-intersections
	- see [[Convex set]]
- same limitations and extensions as [[Multi dimensional Scaling (MDS)]] or [[Classical MDS (cMDS)]]
	- ![[MDS Extensions#Out of sample extension]]
## [[ISOMAP Extensions]]