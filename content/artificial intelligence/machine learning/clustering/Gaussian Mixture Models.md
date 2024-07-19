> a.k.a GMMs
> Probabilistic Clustering Model
- Clusters are the hills in the normalized density function of distribution of the feature space.
	- The distribution of the feature space can have varying densities → more points in a space makes it more dense
	- normalized density function → returns the density
- peak or mode of the hill is the cluster center.
- look at the density function as a **probability distribution function**
- fit a mixture of gaussian models is used to model this probability distribution
- can handle overlapping clusters → assigns points to clusters with some probability
- [[Generative]], as it gives a probability model of x

>See  [[Gaussian Distribution]] 

- fitting 1 gaussian distribution to  1-dimensional gaussian- 
	- ![[Pasted image 20240530180301.png]]
	- where, **ω** is the scale or evidence 
	- **μ** is the mean and **σ** is the std dev of the gaussian **η**

### High dimensional GMM
- Assume the probability distribution **P**(x) in some **D**-dimensions is made of **k** different gaussians
	- weighted sum of **k** gaussians
	- ![[Pasted image 20240530180553.png]]
	- such that 
		- ![[Pasted image 20240530180636.png]]
	- where **x** ∈ R<sup>D</sup>
- **X** belongs to gaussian **k** for which 
		- ||**X** - **μ**<sub>k</sub>|| is min and  
		- ||**X** - **μ**<sub>k</sub>|| < 2.5**σ<sub>k</sub>**
- Equivalent **Latent variable** form
	- p(**z**=k) = ω<sub>k</sub>
		- select a mixture component with probability ω
	- p(**x** | **z** = k) = η(**x** ; μ<sub>k</sub>, σ <sub>k</sub>) 
		- sample from that component’s gaussian
	- then p(**x**) is the marginal over x
	- **z** is the latent variable

## Expectation-Maximization (EM) Algorithm

- start with **k** clusters. Select some μ<sub>c</sub>, σ <sub>c</sub> and ω<sub>c</sub>  (a.k.a. π<sub>c</sub> ) for all the clusters.
- **Expectation** step:
	- for all **x** datapoints, compute soft probabilities **r**<sub>ic</sub>, the probability that **x**<sub>i</sub> belongs to cluster **c** →N x K matrix 
	- normalize to sum to one
	- ![[Pasted image 20240530202451.png]]
	- if **x**<sub>i</sub> likely belongs to cluster **c**, π<sub>c</sub> for the cluster will be high
- **Maximization** step:
	- fixing the **r**<sub>ic</sub>, recompute the cluster parameters
	- for each cluster
	- ![[Pasted image 20240530202957.png]]
- Repeat E-M steps until **convergence**
	- each step increases the **log-likelihood** P(x)
	- ![[Pasted image 20240530203109.png]]
	- convergence when log-likelihood doesn’t change much 
	- convergence guaranteed

### How to choose k?
- penalize the log-likelihood scores

### Pros
- can handle overlapping clusters

### Cons
- sensitive to initialization parameters - can converge to local optima
	- reinitialize multiple times

### Alternatives
- Stochastic EM
- Hard EM


