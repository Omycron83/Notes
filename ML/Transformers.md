Transformers are a [[Neural Network]] variant mainly utilizing attention, encoding and embedding as well as context memory to improve pattern recognition when dealing with sequential or high dimensional data. This is done by selectively focusing only on a part of the information.  

# Architecture:
Fundamentally, all transformers architectures are based on dealing with sequence modelling problems. 
Contrary to [[RNN|RNNs]], the transformer architecture requires a fixed-size input, which in practice gives a maximum sequence length. Different sequence lengths are usually padded to this maximum.  


However, as [[RNN#^991e61|with RNNs]], different types of problems require different types of architectures. One open question is whether or not 
# Encoder:

# Decoder:

# History
The central attention mechanism was first used in [[RNN|RNNs]] in order to combat the problem of information loss in long sequences. It weighs the previous states according to **learned** measure of relevance. This has first been implemented by Bahdanau et al (2014). It was then combined with embedding and self-attention to get rid of the RNN-component altogether, which then formed the original transformer in Vitya et al (2017), after decomposable attention had been proven successful in 2016 when used in combination with a feedforward network. Convergence problems with the architecture where then mitigated by Xiong et al (2020) using layer normalization before multiheaded attention.
# Intuition:
They achieve their success in part due to their parallelizability in sequence modelling tasks compared to previous state-of-the-art algorithms, which enables large scaling and model sizes.
[[RNN]]s, [[LSTM]]s and [[GRU]]s only effectively have access to a certain reference window of previous datapoints in time or outputs previously generated, where LSTMs and GRUs improve on RNNs by elongating that window.
Transformers on the other hand can theoretically use all the previous datapoints and outputs, which it can do effectively by learning and then only focusing on the information currently relevant, which is done through **attention**.

# The Vitya-Transformer:
In general, inputs (usually words) are initially converted into real valued vectors using a lookup table in a process called **input embedding**.
To those vectors, positional information (encoded through a vector of a function taking the position as an input) is then injected by adding it to the embedding in a process called **positional encoding**.
Then, this positional encoding is fed into an **encoder layer** that maps a sequence to an abstract continuous representation which is supposed to hold the learned information of the entire sequence. This contains a multi-headed attention mechanism as well as a regular [[Neural Network]]. There are residual connections between each of the submodules followed by a layer normalization.
Here, in the multi-headed attention submodule, self-attention is used, where the model learns to associate between the positional encodings. This is done by feeding them into three 
# Input Embedding:
Input embedding refers to the practice of converting an arbitrary input into a real-valued vector that can then be mathematically operated on.
## One-hot-encoding
One-hot-encoding refers to the practice of creating a vector with one entry equal to one and all other entries equal to zero. The name stems from electrical engineering, where one … is ‘hot’ and the others ’cold’. 
Each entry then refers to one specific input, i.e. if there are 100 registered words, each word can be represented by a $100$-tuple or vector which is one-hot at the specific word location inside of that vector. 
When working with multiple inputs in a sequence, which transformers are optimized for, one can then simply convert multiple vectors into a matrix by ‘stacking them’, i.e. using them as its column vectors. 
# Attention Mechanisms:
Attention mechanisms are a family of mechanism in transformer models that learn to make predictions by selectively attending to a given set of data. The amount of attention is usually quantified by a certain, learned weight and then formed by a weighted average.
## Self-Attention:
Self attention is a type of attention mechanism that uses observation on a set of datapoints to make predictions about that same set. It is permutation-invariant, i.e. is an operation on sets.
There are multiple forms of self attention out there, with the one originally used being scaled dot-product attention.
### Scaled dot-product attention:
Scaled dot-product attention uses 

# Training:
Typically, unsupervised pretraining is done before moving onto supervised "fine-tuning", as the amount of required labeled training data is often not nearly sufficient for the amount of parameters trained. However, unlabeled data is often available on a large scale.


*Sources:*
https://lilianweng.github.io/posts/2023-01-27-the-transformer-family-v2/
https://e2eml.school/transformers.html
https://www.youtube.com/watch?v=4Bdc55j80l8
https://jinglescode.github.io/2020/05/27/illustrated-guide-transformer/