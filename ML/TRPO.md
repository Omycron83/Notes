Trust-region policy optimization is a [[Policy Gradient Methods|Policy Gradient Method]] that tries to achieve better stability and convergence by taking the largest step possible to improve performance while also satisfying a constraint on the difference between the old and new policy. This is done using [[KL-Divergence]]. 
This is done as being similar in parameter space (as done in [[REINFORCE]] and other 'Vanilla' [[Policy Gradient Methods]]) can be very different from being close in the resulting policies, easily collapsing performance. If one where to improve in this aspect, using very small step sizes may not be necessary.  

## Derivation:
We will derive the concept by first figuring out how the new parameter $\theta$ of our policy should be chosen given that we 