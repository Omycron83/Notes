Recurrent neural networks are a [[Neural Network]] variant used in sequence processing tasks. This enables one to deal with variables size sequences (without increasing complexity) and retain invariance while still sharing information between sequence members. 
However, the state representation limits the amount of information sharable between points in time, especially going far back in time and having to process each step in time sequentially leads to poor parallelizability and thus long computing times.
This and the vanishing gradient problem led to the invention of the [[GRU]] and the [[LSTM]].
# Architecture:
RNNs, as a basis, take in input sequence members ordered into *points in time* $1, ..., t$. Each point in time has its own input $x^{<1>}, ..., x1^{<t>}$, and some states (depending on the architecture) have a target label $y^{<t>}$ that is conditioned on. (Going forward, I will denote points in time using superscripts).

This conditioning is based on ordinary feedforward networks.
However, in order to be able to process variable length sequences without as well as to retain  invariance to the position in time $t$, the model parameters are then shared between all points in time. 

Information containing relationships between points in time is then transferred from one point in time to another using a hidden state matrix $a^{<t>}$ (also called activation), which acts as a layer in itself. 

This layer takes as an input not only the previous layer of this point in time $x^{<t>}$, but also the hidden state matrix of the previous layer $a^{<t - 1>}$, with distincts weights respectively, such that $a^{<t>} = f(W_{aa} a^{<t - 1>} + W_{ax}x^{<t>} + b_a)$, where $a^{<t>}, a^{<t - 1>} \in R^{m \times n}$ and $x \in R^{m \times g}$, thus $W_{aa} \in R^{n \times n}$, $W_{ax} \in R^{g \times n}$ and $b \in R$. Conventionally, $a^{<0>}$ is initialized as the zero matrix.

![[Pasted image 20230922172626.png]]

One can see how this can be simplified by row-stacking $W_{aa}$ and $W_{ax}$ as well as column-stacking $a^{<t-1>}$ and $x^{<t>}$, creating one input and one weight matrix with dimension $m \times n + g$ and $n + g \times n$, respectively.
As usually done, the bias can be included into the matrix representation by adding a column of $1$'s to the new input matrix while adding a corresponding row to the weight matrix, making the dimensions $m \times n + g + 1$ and $n + g + 1 \times n$, respectively. 

## Types of RNNs

^991e61

### One-to-One:
Is just a regular [[Neural Network]]:
![[Pasted image 20230922173248.png]]
Example: Image recognition
### One-to-Many:
$T_x = 1, T_y > 0$, i.e. we start with one input, and then build a sequence out of it:
![[Pasted image 20230922173402.png]]
Example: Music generation

### Many-to-One:
$T_x > 1, T_y = 1$, i.e. we predict only at the last timestep of the sequence:
![[Pasted image 20230922173504.png]]
Example: Sentiment classification

### Many-to-Many:
Two cases:

1. $T_x = T_y$, i.e. we predict at each point in time:
![[Pasted image 20230922173623.png]]
Example: Name entity recognition

2. $T_x \neq T_y$, i.e. we sometimes predict, sometimes we don't:
![[Pasted image 20230922173722.png]]
Example: Machine translation



# Training:
The loss function of a sequence of time steps in a RNN is defined as
$L(\hat{y}, y) = \sum_{t = 1}^{T_y} L(\hat{y}^{<t>}, y^{<t>})$, i.e. the loss is the (unweighted) sum of the losses at points in time.

This loss can then be minimized through BPTT (Backpropagation Through Time). 

At timestep $T$, the derivative of the loss $L$ w.r.t. a weight matrix $W$ can be expressed as $\frac{\delta L^(T)}{\delta W} = \sum_{t = 1}^T \frac{\delta L^(t)}{\delta W}$.



# Variants:

### Bidirectional RNNs
In a bidirectional RNN, the hidden state representations are passed both from the start and the end of each sequence:
![[Pasted image 20230922180528.png]]

### Deep RNNs
There is no reason to exclude multiple hidden state representation layers:
![[Pasted image 20230922180620.png]]
If we assume to roughly discover different patterns at each layer, this may yield special interpretations.

### Gradient Clipping:
In order to alleviate the exploding gradient problem, one can cap the maximum value for the gradient:
![[Pasted image 20230922181858.png]]

### Gates:
^9221f9
In order to alleviate the vanishing gradient problem, specific gates with a well-defined purpose can be employed. They are usually denoted $\Gamma$ and are of the form $\Gamma = \sigma(Wx^{<t>} + U a^{<t -1>} + b)$, where $W, U$ and $b$ are gate-specific.

