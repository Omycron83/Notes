In Policy gradient method, the reward is to be optimized by finding an optimal parameterized policy $\pi^*(a | s, \theta)$, where $\theta$ is some parameter vector and $\pi^* = Pr\{A_t = a | S_t = s, \theta_t = \theta\}$ .
Often, an estimate of the value function $\hat{v}(s , w)$ with parameter $w$ is also used, in which case the method is called an actor-critic method ($\pi$ being the actor, $v$ the critic).

The advantage of those kinds of models are usually: 
- Smooth and natural exploration through the stochastic nature -> Stronger convergence guarantees
- Able to learn stochastic policies
- Not needing to fully understand the environment, but only to learn how to act

It is generally optimized by gradient ascent: $\theta_{t + 1} = theta_t + \alpha \cdot \Delta \hat{J}(\theta_t)$ , where $\hat{J}$ is some performance measure w.r.t. the policy parameters.
And usually, in the episodic case, we can define $J(\theta) = v_{\pi_\theta}(s_0)$.

For this to be possible, we need the policy to be differentiable, $\Delta \pi$ w.r.t. $\theta$ needs to exist. 
Furthermore, the policy should, in order to ensure exploration, not be deterministic, i.e. $\pi(a | s, t) \in ]0; 1[$ 
This can usually be insured by using the softmax function at the end of the policy-evaluation.

Now, we can obtain the general gradient through the [[Policy Gradient Theorem]].

