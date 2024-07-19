used in data visualization, data compression and [[Feature Extraction]]
### Aim
- Find a linear orthonormal projection to maximize data [[Variance]] in the new [[vector space]] ([[linear transformation]])
- find a new basis of maximum variance; basis named principal components (PCs) and their importance decided by variance
- A new low-dimensional representation achieved by projecting data points onto few (< original ) PCs

### Math
#### [[PCA math]]
![[PCA math]]
As any real-valued covariance matrix (leading to PCA) is semi-definite positive and symmetric, its eigenvectors (PCs) are always orthogonal each other. 

PCA can only provides only up to d′ PCs (d′ ≤ d) where d′ is the rank of a covariance matrix used for PCA.
### [[Dual PCA]]
![[Dual PCA]]

## [[Proportion of Variance]]

![[Proportion of Variance]]

- can be used to find optimum intrinsic dimensionality
- also works for the **dual PCA** although there are only up to N non-zero eigenvalues and at least d − N zero values.
## Limitations
- **non-orthogonality**
	- Data distribution may not satisfy the PCA assumption: orthogonal dimensions,
	- **Independent Component Analysis**: captures the maximum variance in non-orthogonal dimensions
- **inconsistency to discrimination**
	- in classification, axis of maximum variance in PCA may be inconsistent with that of the largest discrimination
	- **Linear Discriminative Analysis (LDA)** : Finds out the axis of the largest discrimination by considering the label information
- **non-linearity**
	- non linear manifolds

### [[PCA Extensions]]
