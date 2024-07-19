The objective function being minimized when training neural networks is not a [[Convex Function]] of the parameters. 

**Strictly convex functions** have only 1 global minima. Since all units in a layer are symmetric, given a solution, the weights can just be moved around -> hence the network is invariant to permutations ->  multiple local minima exists -> Not a convex function

Since  this is a non-convex optimization problem, plateauing does not necessarily mean being close to optimality. Changing the **learning rate** in such cases can be used as a way to see if the training procedure can escape the local minimum