Recurrent neural networks are a [[Neural Network]] variant used in either sequence-to-input, input-to-sequence or sequence-to-sequence tasks. 
This enables one to deal with variables size sequences and retain general invariance while still sharing information between sequence members.

# Architecture:
RNNs, as a basis, take in input sequence members ordered into *points in time* $1, ..., t$. Each point in time has its own input $x^{<1>}, ..., x1^{<t>}$, and some states (depending on the architecture) have a target label $y_t$ that is conditioned on. 

This conditioning is based on ordinary feedforward networks.
However, in order to be able to process variable length sequences as well as to retain  invariance to the position in time $t$, the model parameters are then shared between all points in time. 

Information containing relationships between points in time is then transferred from one point in time to another (either from $t -> t + 1$ : unidirectionally, $t + 1 -> t$ : reverse unidirectionally, or both : bidirectional. We assume unidirectionally going forward) using a hidden state matrix $a_t$ (also called activation), which acts as a layer in itself. 

This layer takes as an input not only the previous layer of this point in time $x_t$, but also the hidden state matrix of the previous layer $a_{t - 1}$. 