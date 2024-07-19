- Used to calculate distances or similarity between vectors 
- **p-norm**
	- ![[Pasted image 20240528175038.png]]
- For vectors
	- [[L1 Norm]]
	- [[L2 Norm]]

### Comparisions
- **Robustness**
	- resistance to outliers
	-  L1 > L2
		- the L2 norm squares values, so it increases the cost of outliers exponentially
- **Stability**
	- resistance to horizontal adjustments.
	- L2 > L1
- **Computational Difficulty**
	- L2 > L1
	- L2 has a closed form solution
	-  L1 does not have a closed form solution because it is a non-differenciable piecewise function, as it involves an absolute value. For this reason, L1 is computationally more expensive, as we can't solve it in terms of matrix math
- **Sparsity**
	- L1 > L2

### Matrices
- [[Frobenius Norm]] for matrices