> a.k.a. Sequential Monte Carlo Methods

- Non parametric Bayesian filter
	- Represent arbitrary probability distributions 
	- more complex pdf
	- Represent state distribution non-parametrically
- Recursive non-linear discrete time estimation
	- can be used for non-linear motion
- Use n particles to represent distribution over hidden states
	- use sampling to propagate densities over time
	- e.g. across frames in a video sequence
- At each time step, represent posterior P(Xt |Yt ) with weighted sample set
- Previous time step’s sample set P(Xt-1|Yt-1) is passed to next time step as the effective prior
- **Transition**
	- sample next state for each particle
- **Evidence**
	- weight samples based on evidence
- **Resample**
	- generate a new distribution of particles

### Pros
- non linear systems
- Efficient: particles tend to focus on regions with high probability

### Cons
- Want as few particles as possible for efficiency, but need to cover state space sufficiently well
- interactions between multiple objects require special treatment
	- Multimodal densities possible
	- Not handled well in the particle filtering framework