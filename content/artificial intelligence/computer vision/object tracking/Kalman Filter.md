- parametric Bayesian filter
-  algorithm for estimating the values of measured variables over time, given continuous measurements of those variables and the amount of uncertainty in those measurements
- estimate using past (possibly noisy) observations and present (and possibly noisy) observations
### Assumptions
- noisy sensor
	- noise can be modelled using [[Gaussian Distribution]] PDF
- initial prior knowledge (state) is also a [[Gaussian Distribution]] PDF

## Algorithm
#### 1. Predict Step
predict the current state given the previous state and the time that has passed since
- **state**
	- prediction variable gaussian distribution
		- mean vector (of the prediction variable) and 
		- covariance of prediction variables (uncertainity or noise in prediction variables) 
	- e.g. mean and covariance of position and velocity of an object
- **state-transition matrix** (**F**): relates the previous state to the current one
- **prediction equations**
	- **μ**<sub>p</sub> = **F** **μ**<sub>t</sub>
		- **μ**<sub>p</sub> = predicted mean vector
		- **μ**<sub>t</sub> = mean vector at t
	- predicted covariance matrix
		- ![[Pasted image 20240602221835.png]]
		- **Q**: **process noise**
			- encapsulates uncertainty created by the time that has passed since we last updated the state,
#### 2. Update Step
- combine the predicted state with an incoming measurement
- input two possible states and outputs a new state
-  [[Bayesian inference]]
- ![[Pasted image 20240602224108.png]]
	- x = actual position
	- m = measured position
	- **prior**: predicted state
	- **prior** and **likelihood** are assumed to be [[Gaussian Distribution]]s
	- Normalization i.e measurement probability distribution → empirically calculated
- Posterior probability (updated state) calculated is also a [[Gaussian Distribution]]
- ![[Pasted image 20240602225406.png]]
-  **H** → linear transformation that takes us from the state space to the measured space
-  **Kalman gain**
	- factor by which we incorporate the new sensor information into the updated state
	- Error<sub>estimate</sub> / (Error<sub>estimate</sub> + Error<sub>measured</sub>  )
	- ( 0, 1)
		- 0 → estimate error =0 → estimate is perfect
		- 1 → measure error =0 → measure is perfect, estimate is imperfect
## 1-D case

> [Reference](https://towardsdatascience.com/what-i-was-missing-while-using-the-kalman-filter-for-object-tracking-8e4c29f6b795) 

- object tracking in 1-dimension
- assume constant velocity in 1-dimension
- let state = x, v → position, velocity
- ![[Pasted image 20240602220423.png]]
- initially there is no covariance between the velocity and position.
- **Predict step** equations
	- mean vector prediction
	- ![[Pasted image 20240602221117.png]]
	- **F** picked based on constant velocity assumption
	- Solving for covariance
	- ![[Pasted image 20240602222120.png]]
	- introduces off-diagonal elements in the covariance matrix
- **Update Step** equations
	- ![[Pasted image 20240602225752.png]]
	- ![[Pasted image 20240602225855.png]]
	- ![[Pasted image 20240602230212.png]]
	- ![[Pasted image 20240602230137.png]]

### Pros
- updates are simple and efficient

### Cons
- unimodal distribution
- class of motions restricted by linear model