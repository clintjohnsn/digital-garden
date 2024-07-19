- composed of perceptions
- can theoretically compute any function
- why not boolean circuits?
	- differentiable end to end

## [[Perceptron]]
![[Perceptron]]
if the activation is sigmoid, then this perceptron is basically just Logistic Regression

### One Layer Net
activation function on a **linear**(**affine** in general) **transformation**
There are many possible [[Activation Functions]]

A one layer net with **ReLU** activation would be
N ∶ R<sup>n</sup> → R<sup>p</sup> 
x ↦ max{0,Wx + b} ∶= N(x)

## Multi-layer Perceptron (MLP)
- multiple layer neural network, could be any kind of artificial neurons, not just perceptrons
  ![[Pasted image 20240114214106.png]]

## Feedforward neural Networks
stack of multiple MLPs with multiple hidden layers

![[Pasted image 20240114214940.png]]
-  **depth** = no of transformations = no of layers(counting both and input and output as layers) - 1 = 4
- max number of nodes in a layer is called the **width** = 5
- no of parameters = N<sup>l</sup> * (N<sup>l-1</sup> +1) + N<sup>l-1</sup> * (N<sup>l-2</sup> +1) + ...
	- +1 accounting for bias terms, assume a bias term in every unit

deep neural nets are just functions 
![[Pasted image 20240124145738.png]]

### Population Risk and Empirical Risk

For a distribution **D**, a finite set of samples from it **S**,

**Population Risk (L<sub>D</sub>)** : Measures The Expected Prediction Error of N Over All Data. Empirical population risk will be over the test samples.

**Empirical Risk (L<sub>S</sub>)**: Measures The Expected Prediction Error of N Over The **Seen Training Data**

![[Pasted image 20240124152528.png]]

## Backpropagation
![[Backpropagation]]

## [[Issues with training neural networks]]

## Neural Networks as universal approximators

In theory, one hidden layer is enough: 2 layer neural networks are universal approximators (they are capable of approximating any continuous function to any desired degree of accuracy