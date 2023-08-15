### Theorem: 
Given an optimization function $J(\theta)$, a policy $\pi(a | s)$ as well as the action value function $q_\pi(s, a)$ and the stationary distribution $\mu(s)$, the gradient of the objective function is proportional to:
$\Delta J(\theta) \propto \sum_s \mu(s) \sum_a \Delta \pi(a | s) q_\pi (s, a)$ 

### Proof:
