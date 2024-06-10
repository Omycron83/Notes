Trust-region policy optimization is a [[Policy Gradient Methods|Policy Gradient Method]] that tries to achieve better stability and convergence by taking the largest step possible to improve performance while also satisfying a constraint on the difference between the old and new policy. This is done using [[KL-Divergence]]. 
This is done as being similar in parameter space (as done in [[REINFORCE]] and other 'Vanilla' [[Policy Gradient Methods]]) can be very different from being close in the resulting policies, easily collapsing performance. If one where to improve in this aspect, using very small step sizes may not be necessary.  

## Derivation:
We will derive the concept by first figuring out how the new parameter $\theta$ of our policy should be chosen in order to both perform best in comparison to our previous policy with parameters $\theta_k$ while also restricting how much it can differ using a max. KL-Divergence of $\delta$ :

$\theta_{k + 1} = arg \; max_\theta \; E_{s,t \sim \pi_{\theta_k}} [ \frac{ \pi_\theta (a | s)} {\pi_\theta^{k}  (a | s)}  (q_\pi (s,a) - v_\pi(s)) ]$ s.t. $E_{s \sim \pi_\theta^k} [ D_{KL} (\pi_\theta(\cdot | s), \pi_{\theta^k}(\cdot | s) ) ] \le \delta$


Unfortunately, now, this can't be optimzed using gradient ascent methods anymore, due to the $KL$-constraint.

One can then Taylor-expand both terms w.r.t. $\theta$ around $\theta_k$ to leading order, which approximates this practically insolvable problem to:

$\theta_{k + 1} = g^T (\theta - \theta_k)$ s.t. $\frac{1}{2} (\theta - \theta_k)^T H (\theta - \theta_k) \le \delta$ 

This approximation has an analytical solution of

$\theta_{k + 1} = \theta_k + \sqrt{ \frac{2 \delta}{g^T H^{-1} g} } H^{-1} g$

However, only solving this would introduce a large error associated with the accuracy of the approximation. This can be partially mitigated through backtracking line search:

$\theta_{k + 1} = \theta_k + a^j \sqrt{ \frac{2 \delta}{g^T H^{-1} g} } H^{-1} g$

where $a^j \in ]0; 1[$ is the backtracking coefficient, and $j$ is the smallest natural number such that $\pi_{\theta_{k + 1}}$  still satisfies the convergence maximum.

Finally, in order to efficiently determine the matrix inverse $H^{-1}$, one can use the conjugate gradient theorem and instead calculate $Hx = \Delta_\theta ( (\Delta_\theta  \frac{1}{2} (\theta - \theta_k)^T H (\theta - \theta_k))^T x)$ 

The final algorithm:

![[Pasted image 20230822213943.png]]
