# Rectified Linear Unit
- function and derivative are monotonic
- solves the [[Vanishing Gradient Problem]] and [[Exploding Gradient Problem]] because the derivative of the ReLU function is 0 or 1.

![[ReLU formula]]

### Dying ReLU Problem
- **dead state** of ReLU neuron -> most input ranges are negative and the output is 0
- does not recover because gradient of 0 is 0
- **Causes**
	- high learning rate -> accidently sets negative weights
	- large negative bias -> bias terms become negative
- deep ReLU network will eventually die in probability as the depth goes to infinite 
## Leaky ReLU
- avoid dying ReLU -> non zero gradient in the entire range

### [[Parametric ReLU]]
