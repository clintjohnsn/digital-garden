>Continuous Bag of Words

- predicting the word given its context
- context => surrounding words
	- **m** words before and after the word **w<sub>t</sub>**
- no hidden layers
- context is averaged

### Objective function
Let wt-1,...,wt-m, wt+1,...,wt+m be the context
- **y** = average(context)
- Pr(w<sub>t</sub> |context) = softmax(W**y**)

![[Pasted image 20240523191625.png]]