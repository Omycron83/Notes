Proximal policy optimization tries to implement the general idea used in [[TRPO|Trust Region Policy Optimization]] in a more efficient way by, instead of enforcing a certain maximum $KL$-Divergence, one just clips the ratio between the two policies $r(\theta) = \frac{\pi_\theta (a | s)} {\pi_\theta^{k}(a | s)}$ to a value $[1 - \epsilon, 1 + \epsilon]$, where $\epsilon$ is another hyperparameter. 

Thus, if $r > 1$, the action is more likely in the current than the old policy. However, if $r$ is $\in [0; 1]$, the action is less likely. Thus, this is an easy divergence measure.

Thus, the weight objective becomes:
$\theta_{k + 1} = arg \; max_\theta E [min( r(\theta) A(s, a)   , clip (r(\theta), 1 - \epsilon, 1 + \epsilon) A(s, a)   )] = argmax_\theta L^{clip} (\theta)$
Where $clip (r(\theta), 1 - \epsilon, 1 + \epsilon)$ clips the ration to be no more than $1 + \epsilon$ and no less than $1 - \epsilon$. It then takes the minimum between the original value and the clipped value.

With e.g. $A(s, a) = (q_\pi (s,a) - v_\pi(s))$
(Assuming we use the action-value- and the value-function to form the advantage.)
Which can be optimized using gradient ascent methods, similar to the [[REINFORCE]]-Algorithm.

The final algorithm:
![[Pasted image 20230823005049.png]]

In practice, this got expanded to:
![[Pasted image 20240210125721.png]]
in the paper
https://arxiv.org/pdf/1707.06347.pdf



*Source:* https://lilianweng.github.io/posts/2018-04-08-policy-gradient/
https://huggingface.co/blog/deep-rl-ppo#the-intuition-behind-ppo
