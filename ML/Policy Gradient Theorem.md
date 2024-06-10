### Theorem: 
Given an optimization function $J(\theta)$, a policy $\pi(a | s, \theta)$ as well as the action value function $q_\pi(s, a)$ and the [[Stationarity|stationary]] distribution $\mu(s)$, the gradient of the objective function is proportional to:
$\Delta J(\theta) \propto \sum_s \mu(s) \sum_a \Delta \pi(a | s, \theta) q_\pi (s, a) = E_{\pi}[\Delta \pi(s | a, \theta) q_\pi(s, a)]$ 
and exactly equal to 
$\Delta J(\theta) = E_\pi[\frac{\Delta \pi(s | a, \theta)}{\pi(s | a, \theta)} q_\pi(s, a)] = E_\pi[\Delta ln(\pi(s|a, \theta)) q_\pi(s, a)]$ 
This also holds for the continuous and discounted use case. 
### Proof:
