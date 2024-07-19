a.k.a **RNN**

family of neural networks for processing sequential data.

> e.g. in NLP, modelling the next word given the observed history -> Recurrent Neural Networks compress the entire history in a fixed length vector, enabling long range correlations to be captured.

RNN is a a feed forward network where the hidden layer is a function of both the input x and the previous hidden layer h, with output layers attached to every hidden layer.

The unrolled recurrent network is a directed acyclic computation graph.

## [[Backpropagation Through Time (BPTT)]]

## Issues with RNNs
- Lack of parallelizability: Forward and backward passes have O(sequence length) unparallelizable operations. Enter [[Transformers]]
