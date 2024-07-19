
in a deep neural network, doing the backpropagation involves multiplying several derivatives of activation functions together - for some activation functions, this makes the gradient ≈ 0

eg [[Sigmoid or Logistic Activation]] - the derivative of sigmoid <= 0.25 so every time we are guaranteed to multiply with at max 0.25

opposite of [[Exploding Gradient Problem]]

can be solved by [[ReLU activation]]