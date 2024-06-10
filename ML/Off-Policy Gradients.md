If one uses [[Policy Gradient Methods|policy gradient methods]] following the [[REINFORCE]]-principle especially in combination with a function approximator such as a neural network, online or on-policy learning is extremely inefficient as practical consideration often force the policy to only change slowly, as seen in [[TRPO]] and [[Proximal Policy Optimization]]. 

For that, one has to remember that $argmax_\theta J(\theta) = E_{\tau \sim p_\theta (\tau)} [r(\tau)]$ is our goal, i.e. to maximize expected return encountered in transitions whos policy are parameterized by $\theta$. Now, lets assume one instead has $\tau \sim \bar{p}(\tau)$ Transitions encountered by a different policy. Then:
$J(\theta) = E_{\tau \sim \bar{p}(\tau)} [\frac{p_\theta (\tau)}{\bar{p}(\tau)} r(\tau)]$, as 
![[Pasted image 20240209232554.png]]

and due to 
$p_\theta(\tau) = p(s_1) \Pi_{t = 1}^T \pi_\theta (a_t | s_t) p(s_{t + 1}|s_t, a_t)$
(per Definition, as the probability of the episode $\tau$ happening is equal to the starting probability multiplied by the probablity of the according action and resulting probability at each step.)

Now, when also doing this with $\bar{p}(\tau)$, all but the products of the policies cancel out, leaving: $\frac{p_\theta(\tau)}{\bar{p}(\tau)} = \frac{\Pi_{t = 1}^T \pi_\theta (a_t | s_t)}{\Pi_{t = 1}^T \bar{\pi}(a_t | s_t)}$.


Source: https://rail.eecs.berkeley.edu/deeprlcourse/static/slides/lec-5.pdf
