
used to perform [[Feature Extraction]] and **data interpretation**, esp. for  two relevant random vectors 

Find optimal [[linear projection]]s for two relevant random vectors to maximize their correlation in the new low dimensional space.
> see [[Correlation & Covariance]]

For 2 domains (2 domains of variables collected on the same samples), find (low dimensional) projections using (one or more) **canonical variates** (basis) such that the two projections are (maximum) correlated and in the same space.

identify and measure the correlation among two sets of random variables (random vectors), which leads to a new (common) representation capturing the maximum correlation between two random vectors

[[Data Centralization]] must be done prior.

**Correlation** -> plays a role of **normalization** to make the correlation invariant with respect to rescaling a and b (canonical variates)
## Math
[[CCA math]]
![[CCA math]]

## Algorithm

![[Pasted image 20240122202830.png]]
### [[Proportion of Variance]]
![[Proportion of Variance]]
PoV(k) works up to min(p, q)
can be used to find optimum intrinsic dimensionality

## [[CCA Extensions]]
