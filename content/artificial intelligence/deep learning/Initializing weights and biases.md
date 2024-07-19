Initialization is important to make sure that the network is not in a saturated state at the beginning of optimization
> ![[Saturation]]
It is important to stress that the randomness in the initializations plays an important role in symmetry breaking. All the units in a given layer typically are symmetric to begin with. If all the weights are initialized identically, then there will be nothing to differentiate them during training.

For [[Sigmoid or Logistic Activation]], can use 0 or a random value around 0. 
For d weights (w<sub>1</sub> ... w<sub>d</sub>), initialize  from a Gaussian distribution with mean 0 and variance = 1/d assuming that inputs x<sub>i</sub> satisfy E[x<sup>l</sup>] ~ 1. Bias terms can be set to 0 or some small value around 0

For [[ReLU activation]], should use a small positive constant