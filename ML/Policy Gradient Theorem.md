### Theorem: 
Given an optimization function $J(\theta)$, a policy $\pi(a | s, \theta)$ as well as the action value function $q_\pi(s, a)$ and the [[Stationarity|stationary]] distribution $\mu(s)$, the gradient of the objective function is proportional to:
$\Delta J(\theta) \propto \sum_s \mu(s) \sum_a \Delta \pi(a | s, \theta) q_\pi (s, a)$ 
This also holds for the continuous and discounted use case.
### Proof:
