Recurrent neural networks are a [[Neural Network]] variant used in either sequence-to-input, input-to-sequence or sequence-to-sequence tasks. 
This enables one to deal with variables size sequences and retain general invariance while still sharing information between sequence members.

# 
This is done by adding a recurrent layer in between regular feed-forward-layers, and then dividing inputs into unequal *points in time*. Thus, an often natural order of states is constructed. 
Each point in time has its own input $x_t$, and some states have a target label $y_t$ that is conditioned on. 
Parameters are then shared between the points in time, such that if there was no other connection between them
Information can then be consistently transfered between the states by the use of a  , 

![[Pasted image 20230922164203.png]]