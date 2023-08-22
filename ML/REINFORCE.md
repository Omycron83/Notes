The REINFORCE-Algorithm is an algorithm directly following the [[Policy Gradient Methods |general Idea of Policy Gradient Methods]]. It is special in that the update done at the point in time $t$ only depends on $A_t$, i.e. only on the action actually taken on the timestep $t$ , and is, due to using $G_t$, i.e. the actual reward occured in that episode a, a monte-carlo algorithm.

### Derivation:
We take the proportionality obtained by the [[Policy Gradient Theorem]], and realise that, for an expectation under $\pi$ , we need to normalize under $\pi$ :
Thus, we use $\Delta J(\theta) \propto E_\pi  [\, \sum_a  q_\pi (S_t, a) \Delta \pi(a | S_t, \theta) \, ]$ and then multiply and divide by $\pi(a | S_t, \theta)$ :
$\Leftrightarrow \Delta J(\theta) = E_\pi [\, \sum_a  \pi(a | S_t, \theta) q_\pi (S_t, a) \frac{\Delta \pi(a | S_t, \theta)}{\pi(a | S_t, \theta)}  \,]$ Now, we can replace a with $A_t \sim \pi$ :
$\Leftrightarrow \Delta J(\theta) = E_\pi [\, q_\pi (S_t, A_t) \frac{\Delta \pi(A_t | S_t, \theta)}{\pi(A_t | S_t, \theta)}  \,]$ Now, we know that $q_\pi (S_t, A_t) = E_\pi [ G_t | S_t, A_t ]$ 
$\Leftrightarrow \Delta J(\theta) = E_\pi [ \,  G_t \frac{\Delta \pi(A_t | S_t, \theta)}{\pi(A_t | S_t, \theta)}  \,]$  Where $G_t$ is just the return expected from thereon forward

Thus, the gradient-ascent update rule yields:
$\Leftrightarrow \theta_{t + 1} = \theta_t + \alpha G_t \frac{\Delta \pi(A_t | S_t, \theta)}{\pi(A_t | S_t, \theta)}$
And, because we know $\Delta ln(x) = \frac{\Delta x}{x}$ :
$\Leftrightarrow \theta_{t + 1} = \theta_t + \alpha G_t \Delta ln(\pi(A_t | S_t \theta)$

Thus, we get the algorithm:
![[Pasted image 20230815010633.png]]

This can be optimized using some optimizer, for example directly through gradient descent.
### Reinforce with baseline:
The policy gradient theorem can be altered to also include an arbitrary baseline estimator $b(s)$:
$\Delta J(\theta) \propto \sum_s \mu(s) \sum_a (q_\pi (s, a) - b(s)) \Delta \pi(a | s, \theta)$
This can be an arbitrary function, as long as it doesn't depend on $a$ , as the subtracted quantity is then zero:
$\sum_a b(s) \Delta \pi(a | s, \theta) = b(s) \sum_a  \Delta \pi(a | s, \theta) = b(s) \Delta \sum_a  \pi(a | s, \theta) = b(s) \Delta 1 = b(s) 0 = 0$

Analog to our previous update rule, we can now generalize this. It often makes sense, for convergence reasons, to use an estimator 