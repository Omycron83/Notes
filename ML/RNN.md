Recurrent neural networks are a [[Neural Network]] variant used in either sequence-to-input, input-to-sequence or sequence-to-sequence tasks. 
This enables one to deal with variables size sequences and retain general invariance while still sharing information between sequence members.

# Architecture:
RNNs, as a basis, take in input sequence members ordered into *points in time* $1, ..., t$. Each point in time has its own input $x^{<1>}, ..., x1^{<t>}$, and some states (depending on the architecture) have a target label $y_t$ that is conditioned on. 

This conditioning is based on ordinary feedforward networks.

In order to be able to process variable length sequences as well as to retain  invariance to the position in time $t$, the model parameters are then shared between all points in time. 

Parameters are then shared between the points in time, such that if there was no other connection between them
Information can then be consistently transfered between the states by the use of a  , 