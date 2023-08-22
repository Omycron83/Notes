Proximal policy optimization tries to implement the general idea used in [[TRPO|Trust Region Policy Optimization]] in a more efficient way by, instead of enforcing a certain maximum $KL$-Divergence, one just clips the ratio between the two policies $r(\theta) = \frac{\pi_\theta (a | s)} {\pi_\theta^{k})$ in a value $[1 - \epsilon, 1 + \epsilon]$, where $\epsilon$ is another hyperparameter. Thus, the weight objective becomes:

$\theta_{k + 1} = E [min(   (q_\pi (s,a) - v_\pi(s)) , (q_\pi (s,a) - v_\pi(s))  )]


*Source:* https://lilianweng.github.io/posts/2018-04-08-policy-gradient/