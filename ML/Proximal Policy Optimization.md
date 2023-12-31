Proximal policy optimization tries to implement the general idea used in [[TRPO|Trust Region Policy Optimization]] in a more efficient way by, instead of enforcing a certain maximum $KL$-Divergence, one just clips the ratio between the two policies $r(\theta) = \frac{\pi_\theta (a | s)} {\pi_\theta^{k}(a | s)}$ to a value $[1 - \epsilon, 1 + \epsilon]$, where $\epsilon$ is another hyperparameter. Thus, the weight objective becomes:

$\theta_{k + 1} = arg \; max_\theta E [min( r(\theta)   (q_\pi (s,a) - v_\pi(s)) , clip (r(\theta), 1 - \epsilon, 1 + \epsilon) (q_\pi (s,a) - v_\pi(s))  )]$

Which can be optimized using gradient ascent methods, similar to the [[REINFORCE]]-Algorithm.

Where $clip (r(\theta), 1 - \epsilon, 1 + \epsilon)$ clips the ration to be no more than $1 + \epsilon$ and no less than $1 - \epsilon$.
It then takes the minimum between the original value and the clipped value.

The final algorithm:
![[Pasted image 20230823005049.png]]

*Source:* https://lilianweng.github.io/posts/2018-04-08-policy-gradient/