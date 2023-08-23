Transformers are a [[Neural Network]] variant mainly utilizing attention, encoding and embedding as well as context memory to better pattern recognition when dealing with sequential or high dimensional data by selectively focusing on information. 

They achieve their success in part due to their parallelizability in sequence modelling tasks compared to previous state-of-the-art algorithms, which enables large scaling and model sizes.
RNNs, LSTMs and GRUs only effectively have access to a certain window of datapoints previous in time or outputs previously generated, where LSTMs and GRUs improve o RNNs by elongating that window.
Transformers on the t

It was originally introduced in the paper "Attention is all you need" in 2017 using an encoder-decoder architecture for language translation, but since shown remarkable results in Computer Vision, Large Language Models or Reinforcement Learning.
# Attention mechanisms:
Attention mechanisms are a family of mechanism in transformer models that learn to make predictions by selectively attending to a given set of data. The amount of attention is usually quantified by a certain, learned weight and then formed by a weighted average.

## Self-Attention:
Self attention is a type of attention mechanism that uses observation on a set of datapoints to make predictions about that same set. It is permutation-invariant, i.e. is an operation on sets.
There are multiple forms of self attention out there, with the one originally used being scaled dot-product attention.

### Scaled dot-product attention:
Scaled dot-product attention uses 



*Source:* https://lilianweng.github.io/posts/2023-01-27-the-transformer-family-v2/