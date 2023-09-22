Recurrent neural networks are a [[Neural Network]] variant used in either sequence-to-input, input-to-sequence or sequence-to-sequence tasks. 
This enables one to deal with variables size sequences and retain general invariance while still sharing information between sequence members.

# Architecture:
RNNs, as a basis, take in input sequence members ordered into *points in time* $1, ..., t$. Each point in time has its own input $x^{<1>}, ..., x1^{<t>}$, and some states (depending on the architecture) have a target label $y^{<t>}$ that is conditioned on. (Going forward, I will denote points in time using superscripts).

This conditioning is based on ordinary feedforward networks.
However, in order to be able to process variable length sequences as well as to retain  invariance to the position in time $t$, the model parameters are then shared between all points in time. 

Information containing relationships between points in time is then transferred from one point in time to another (either from $t \rightarrow t + 1$ : unidirectionally, $t + 1 \rightarrow t$ : reverse unidirectionally, or both : bidirectional. We assume unidirectionally going forward) using a hidden state matrix $a^{<t>}$ (also called activation), which acts as a layer in itself. 

This layer takes as an input not only the previous layer of this point in time $x^{<t>}$, but also the hidden state matrix of the previous layer $a^{<t - 1>}$, with distincts weights respectively, such that $a^{<t>} = f(W_{aa} a^{<t - 1>} + W_{ax}x^{<t>} + b_a)$, where $a^{<t>}, a^{<t - 1>} \in R^{m \times n}$ and $x \in R^{m \times g}$, thus $W_{aa} \in R^{n \times n}$, $W_{ax} \in R^{g \times n}$ and $b \in R$.
One can see how this can be simplified by column-stacking $W_{aa}$ and $W_{ax}$ as well as $a^{<t-1>}$ and $x^{<t>}$, creating one input and one weight matrix.
As usually done, the bias can be included into the matrix representation by adding a column of $1$'s to the input while adding a corresponding 

