Trust-region policy optimization is a [[Policy Gradient Methods|Policy Gradient Method]] that tries to achieve better stability and convergence by taking the largest step possible to improve performance while also satisfying a constraint on the difference between the old and new policy. This is done using [[KL-Divergence]]. 
This is done as being similar in parameter space (as done in [[REINFORCE]] and other 'Vanilla' [[Policy Gradient Methods]]) can be very different from being close in the resulting policies, easily collapsing performance. If one where to improve in this aspect, using very small step sizes may not be necessary.  

## Derivation:
We will derive the concept by first figuring out how the new parameter $\theta$ of our policy should be chosen in order to both perform best in comparison to our previous policy with parameters $\theta_k$ while also restricting how much it can differ:
$\theta_{k + 1} = arg \; max_\theta E_{s,t \sim \pi_{\theta_k}} [ \frac{ \pi_\theta (a | s)} {\pi_\theta^{k}  (a | s)}  (q_\pi (s,a) - v_\pi(s)) ]$

