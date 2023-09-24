Transformers are a [[Neural Network]] variant mainly utilizing attention, encoding and embedding as well as context memory to improve pattern recognition when dealing with sequential or high dimensional data. This is done by selectively focusing only on a part of the information.  

# Architecture:
## Inputs:
Contrary to [[RNN|RNNs]], the transformer architecture requires a fixed-size input, which in practice gives a maximum sequence length. We will denote this length as $d_{sequence}$.
Different sequence lengths are usually padded to this maximum, and the added dimensionality then mitigated by the other components.  
### Input Embedding:
When working with multiple inputs in a sequence, which transformers are optimized for, one can then simply convert the corresponding vectors into a matrix by ‘stacking them’, i.e. using them as its column vectors. 
The size of each vector is referred to as $d_{model}$. 
Thus, each sequence input is a $d_{sequence} \times d_{model}$ [[Matrizen|matrix]].

Input embedding refers to the practice of converting an arbitrary input into a real-valued vector that can then be mathematically operated on. It is often desirable to keep relationships between words, i.e. have the 'close-ness' in reality be reflected in the distance in the embedding space. This is not necessarily the case when dealing with numerical inputs.
#### One-hot-embedding
One-hot-encoding refers to the practice of creating a vector with one entry equal to one and all other entries equal to zero. The name stems from electrical engineering, where one … is ‘hot’ and the others ’cold’. 

Each entry then refers to one specific input, i.e. if there are 100 registered words, each word can be represented by a $100$-tuple or vector which is one-hot at the specific word location inside of that vector. 
### Positional Encoding:
The vector representation of the input does, contrary to [[RNN|RNNs]], not contain positional information anymore, which is necessary when working with input sequences. Thus, we need to infuse positional encoding again to the input.

This is done by constructing a positional-encoding vector containing information about the position of the sequence member, which is then added to the embedded sequence member vector. 
Thus, a position-dependent signal is added to each embedding and thus positional encoding infused, which avoids destroying the embedded information (empirically) while not increasing dimensionality (as would happen with concatenation). 

It turns out that linearly adding the positional values (i.e. adding $(0, ..., 0), (1, ..., 1)$ etc. ) faces problems with 'variable-length' sequences. This leads to the following requirements for a positional-encoding mechanism:
- The model should easily be able to learn to attend by relative positions for any fixed offset
- It should be injective, i.e. output a unique encoding for each time step
- The distance between any two time steps should be consistent across varying lengths
- It should generalize to longer sequences without any effort
- Its values should be bounded
- It must be deterministic
#### Sin-Encoding:
The mechanism introduced by Vitya et al satisfies the above equations:
Let $p_t$ denote the positional encoding vector corresponding to the position $t$ in the given sequence.

Then $f: N \rightarrow R^{d_{model}}, t \mapsto p_t^{(i)} = sin(\frac{t}{10000^{2k / d_{model}}})$ if $i = 2k$, $cos(\frac{t}{10000^{2k / d_{model}}})$ else
satisfies this equation. This forms a geometric progression from $2\pi$ to $10000 \cdot 2\pi$ on the wavelength, with vectors of the form
$\begin{pmatrix} sin(\frac{t}{10000^{2\cdot 0 / d}}) \\  cos(\frac{t}{10000^{2\cdot 0 / d}}) \\ ... \\ sin(\frac{t}{10000^{2 \cdot d / 2 / d} }) \\ cos(\frac{t}{10000^{2 \cdot d / 2 / d}})\end{pmatrix} = \begin{pmatrix} sin(\frac{t}{1}) \\  cos(\frac{t}{1}) \\ ... \\ sin(\frac{t}{10000}) \\ cos(\frac{t}{10000})\end{pmatrix}$

representable as ![[Pasted image 20230924151254.png]]

Proof:
	While the other assertions are easy to see, the first assertion requires more comprehensive consideration. We essentially have to show that there exists a linear transformation $M \in R^{2 \times 2}$ (which is the basis of the neural network) that is able to transform $M \cdot \begin{pmatrix} sin(\frac{t}{10000^{2k / d_{model}}}) \\ cos(\frac{t}{10000^{2k / d_{model}}}) \end{pmatrix} = \begin{pmatrix} sin(\frac{t + \phi}{10000^{2k / d_{model}}}) \\ cos(\frac{t + \phi}{10000^{2k / d_{model}}}) \end{pmatrix}$ for every sine-cosine pair *irrespective* of $t$.
	This can be done by parameterizing $M = \begin{pmatrix}u_1 & v_1 \\ u_2 & v_2\end{pmatrix}$
	And then, by the additive theorem, substituting $\begin{pmatrix} sin(\frac{t + \phi}{10000^{2k / d_{model}}}) \\ cos(\frac{t + \phi}{10000^{2k / d_{model}}}) \end{pmatrix}= \begin{pmatrix} sin(t...)cos(\phi...) + cos(t...)sin(\phi...) \\ cos(t...)cos(\phi...) - sin(t...)sin(\phi ...) \end{pmatrix}$
	yields a system of linear equations with the solution
	$u_1 = cos(\phi...), v_1 = sin(\phi...), u_2 = -sin(\phi...), v_2 = cos(\phi...)$ 
	Thus proving that the model is able to capture relative positions for a fixed offset $\phi$.

This is actually similar to binary encoding: if one wants to binarily encode numbers, the least significant bit (the last one) is alternated on every number, the second-lowest bit is rotating on every two numbers etc. The sinusoidal functions are actually equivalent to alternating these bits, but can effectively be used in combination with the typically used floating point numbers. Decreasing their frequencies like we are doing with the geometric progression enables us to 'address not only the first few, but also the last bits'.
![[Pasted image 20230924142803.png|320]] ![[Pasted image 20230924142815.png|320]]


## Encoder:
The goal of the encoder is to output a set of encoded vectors for each sequence member. As discussed above, it takes in a fixed-length vector.

The entire encoder is made up from multiple encoder structures, which are all identical in nature, though they do not share weights:

Each encoders input is first processed by a self-attention layer, and its results are then fed into a feed-forward-layer, which is applied to each position independently. The outputs of that layer are then fed into the next encoder etc.

![[Pasted image 20230924154026.png]]
Thus, while the self-attention layer includes dependencies between the 'paths' of each input at some point in time, the feed-forward-layer does not, allowing for parallelization. This is one of the key properties of the transformer.

Additionally, after each sub-layer, there is a residual connection between the inputs and the outputs of the two mechanisms (self-attention and feedforward-layer) that is then used in an addition and layer-normalization step:
![[Pasted image 20230924190341.png]]

Here, layer normalization refers to the process of 
## Decoder:
The goal of the decoder is to generate the next sequence member in the output sequence. For this, it takes in the previously generated output sequence as well as the encoded vectors of the encoder. 

## Attention Mechanisms:
Attention mechanisms are a family of mechanism in transformer models that learn to make predictions by selectively attending to a given set of data. The amount of attention is usually quantified by a certain, learned weight and then formed by a weighted average.
### Self-Attention:
Self attention is a family of type of attention mechanisms that uses observation on a set of datapoints to make predictions about that same set (usually some importance-score of each element for some value). It is permutation-invariant, i.e. is an operation on sets. 
#### Scaled dot-product attention:
##### Process:
In scaled dot-product attention, for each encoded vector in a sequence, three vectors are created for every encoded vector $w_t$ at some point in time $t$: a query vector $q_t$, a key vector $k_t$ and a value vector $v_t$, all of the same size $d_k$, which form different abstractions of the vector. 

They are obtained by multiplying each vector my the corresponding, learned weight matrix $W^Q$, $W^K$ and $W^V \in R^{d_n \times d_k}$ .

Using these abstractions, a score for the importance of each point in the sequence for the value of this point in the sequence can be calculated by scoring each datapoint of the sequence against this datapoint (even the datapoint itself). This score is obtained by taking the **dot-product** of the query and key vector $q_t \cdot k_t^T$. 

Then, the scores for each point in the sequence are divided by $\sqrt{d_k}$ in order to guarantee more stable gradients. 

Afterwards, the normalized scores for each point in the sequence are passed through the softmax-function, which obtains sharper weights summing to one.
The softmax score then determines how impactful each sequence member is for this sequence member. Clearly, the sequence member itself will probably have one of the highest scores, but other scores may be high as well.

This softmax score is then multiplied by the values vectors $v_t$, forming a weighted representation. This is then summed up to gain an importance-weighted average $z_t$ for this point in the sequence, which can be passed on. 

Example for determining the score of the word 'thinking' in the sequence 'thinking machines':
![[Pasted image 20230924164750.png]]
##### Matrix Representation:
This individual process can easily be represented using matrices. 

We note that the input to each self-attention layer is a $X \in R^{d_{sequence} \times d_n}$ matrix, where each row represents the encoded representation for some sequence member.

Thus, the corresponding query, key and value **matrices** can be obtained by multiplying $Q = X \cdot W^Q, K = X \cdot W^K, V = X \cdot W^V$. Each of the matrices has size $R^{d_{sequence} \times d_k}$, and represents the query/key/value score (column) for each sequence member (row).

The score of each word can then be obtained by multiplying $Q \cdot K^T$, which produces a $d_{sequence} \times d_{sequence}$ Matrix. This represents the score/weight for each sequence member (row) of each sequence member (column).  

As previously stated, each entry is then scaled and each row then put through the softmax-function (so that each row, i.e. the score for each each sequence member sums up to one).

Afterwards, this matrix is then multiplied by the value matrix $V$ to the final score matrix, so that each row (representing the weight of each sequence member of the column for the corresponding sequence member) is multiplied by each column (representing the corresponding feature values for each sequence member) yielding the weighted 'impact' values in the corresponding sequence point row in the corresponding feature value column. 
This matrix of size $d_{sequence} \times d_k$ is then fed into the subsequent feedforward layer.

Visualization:
![[Pasted image 20230924165950.png]]
##### Matrices as lookup-tables:
One may ask for the motivation of the matrices $Q, K$ and $V$ and the implicit theory behind them. This can be explained using [[Markov Chains]]: 
we can view our sequence as a markov chain, as in that the different sequence points represent states and the way they lead to each other are the conditional probability between them. The probability of the point in the sequence (given another point in the sequence) times the value can then be interpreted as the expected value given that there was the other point in the sequence. 

And as we know, a markov chain can be expressed using a matrix, which we yielded here by multiplying the query and key matrices and which we then multiplied by the value matrix after enabling the probabilistic interpretation using the softmax function:
![[Pasted image 20230924181055.png]]

The multiplication of the query and key matrices can then further be viewed as mask lookup: [[Masks]] are a way to exclude unnecessary features 

#### Multi-head attention:
Instead of only performing one variant of self-attention, i.e. learning one representation of each vector as one combination of features, one can yield multiple representation subspaces by using multiple sets of Query/Key/Value weight matrices denoted $W_i^Q, W_i^K, W_i^V$, that are all independently randomly initialized and subsequently learned. These are called **attention heads**.

As an example, if we had eight different weight-matrix-sets, we would yield eight different z-matrices:
![[Pasted image 20230924181831.png]]

However, the next feedforward layer assumes a $d_{sequence} \times d_k$ input matrix. This can be alleviated by interpreting each representation of $Z_i$ as a different set of features for each sequence member. Thus, we can concatenate the matrices $d_{sequence} \times d_k$ matrices to one $d_{sequence} \times n \cdot d_k$ matrix:
![[Pasted image 20230924182337.png]]

In order to yield a matrix with $d_k$ columns again, one can then multiply this concatenated matrix by another learned weight matrix $W^O \in R^{n \cdot d_k \times d_k}$ to yield the final representation matrix $Z$. In total:
![[Pasted image 20230924185423.png]]

## Backpropagation:
Now that 'forward-propagation' has been discussed, 
# History
The central attention mechanism was first used in [[RNN|RNNs]] in order to combat the problem of information loss in long sequences. It weighs the previous states according to **learned** measure of relevance. This has first been implemented by Bahdanau et al (2014). It was then combined with embedding and self-attention to get rid of the RNN-component altogether, which then formed the original transformer in Vaswani et al (2017), after decomposable attention had been proven successful in 2016 when used in combination with a feedforward network. Convergence problems with the architecture where then mitigated by Xiong et al (2020) using layer normalization before multiheaded attention.
# Intuition:
They achieve their success in part due to their parallelizability in sequence modelling tasks compared to previous state-of-the-art algorithms, which enables large scaling and model sizes.
[[RNN]]s, [[LSTM]]s and [[GRU]]s only effectively have access to a certain reference window of previous datapoints in time or outputs previously generated, where LSTMs and GRUs improve on RNNs by elongating that window.
Transformers on the other hand can theoretically use all the previous datapoints and outputs, which it can do effectively by learning and then only focusing on the information currently relevant, which is done through **attention**.

# The Vaswani-Transformer:
In general, inputs (usually words) are initially converted into real valued vectors using a lookup table in a process called **input embedding**.
To those vectors, positional information (encoded through a vector of a function taking the position as an input) is then injected by adding it to the embedding in a process called **positional encoding**.
Then, this positional encoding is fed into an **encoder layer** that maps a sequence to an abstract continuous representation which is supposed to hold the learned information of the entire sequence. This contains a multi-headed attention mechanism as well as a regular [[Neural Network]]. There are residual connections between each of the submodules followed by a layer normalization.
Here, in the multi-headed attention submodule, self-attention is used, where the model learns to associate between the positional encodings. This is done by feeding them into three 

# Training:
Typically, unsupervised pretraining is done before moving onto supervised "fine-tuning", as the amount of required labeled training data is often not nearly sufficient for the amount of parameters trained. On the contrary, unlabeled data is often available on a large scale.


*Sources:*
https://lilianweng.github.io/posts/2023-01-27-the-transformer-family-v2/
https://e2eml.school/transformers.html
https://www.youtube.com/watch?v=4Bdc55j80l8
https://jinglescode.github.io/2020/05/27/illustrated-guide-transformer/
https://datascience.stackexchange.com/questions/51065/what-is-the-positional-encoding-in-the-transformer-model
https://kazemnejad.com/blog/transformer_architecture_positional_encoding/
