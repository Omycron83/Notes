Eligibility traces are a way to combine both [[Temporal Difference Methods|Temporal Difference]] targets and [[Monte Carlo Methods|Monte-Carlo]] returns by unifying both updates. They use a short-term memory vector for the weight $\theta$, the eligibility trace $\theta_t$, that parallels the original weight and 

# $\lambda$-Methods
## The $\lambda$-Return
One finds that, averaging multiple [[n-Step Return|n-step-returns]] with overlapping time horizons $w_1 G_{t:t+1} + w_2 G_{t:t+2} + ... + w_n G_{t:t + n}$, $w_1 + ... + w_n = 1$, it creates a new way to interrelate the methods, and can only be applied when $G_{t:t + n}$ has been finished.

Now, the $\lambda$-return enables a very specific update by using a $\lambda \in [0, 1)$ and more specifically its $\lambda^l$ as weights, thus giving a certain preference according to 
$G_t^\lambda = (1 - \lambda) \sum_{n = 1}^\infty \lambda^{n - 1} G_{t:t + n}$ 
where $1 - \lambda$ is used to ensure that the weights sum to $1$ and all n-step returns after having reached a terminal state being assigned the conventional return $G_t$, which begs the post-termination sum being given by
$G_t^\lambda = (1-\lambda) \sum_{n = 1}^{T - t - 1} \lambda^{n - 1} G_{t:t+n} + \lambda^{T - t - 1} G_t$

![[Pasted image 20240208200553.png]]
If $\lambda = 0$, then the overall update reduces to the first component, i.e. the one-step TD update. 
If $\lambda = 1$, then the overall update reduces to its last component, i.e. the monte carlo update.
![[Pasted image 20240208200911.png]]

## The Offline $\lambda$-Return Algorithm
One can then use the usual [[semi-gradient rule]], using the $\lambda$-target according to
$w_{t + 1} = w_t + \alpha [G_t^\lambda - \hat{v}(S_t)] \nabla \hat{v}(S_t)$ mit $t = 0, ..., T - 1$.
This moves more smoothly between the two methods, leading to slightly superior performance on a 19-step random walk task:
![[Pasted image 20240208202159.png]]
One also observes that the optimal value appears to be somewhere in the middle.

However, it remains: this is offline and forward-viewing: i.e., at each point in time, we only look forward to the future steps in time and combine them in a meaningful way. This also leads to future states being processed repeatedly, making it computationally inefficient. 

## TD($\lambda$)
TD($\lambda$) improves on this by approximating the affirmentioned return, while also improving in practicallity:
- It can update the weight vector on every step of an episode instead of at the end
- The computations are equally distributed in time
- Can be implemented for continuing problems

It works by implementing a vector/matrix of the same size as the weights of the model. It acts a short-term vector, lasting less than the length of an episode while assisting in the learning process by accumulating the gradient and then fading away by $\gamma \lambda$:
$z_{-1} = 0$
$z_t = \gamma \lambda z_{t - 1} + \nabla \hat{v}(S_t)$ 
It is then said to indicate the 'eligability' of each component for undergoing learning changes for a reinforcement-step. So, when the TD-error is $\delta_t = R_{t + 1} + \gamma \hat{v}(S_t) - \hat{S_t}$,
we instead update with $\theta_{t + 1} = \theta_t + \alpha \delta_t z_t$.

This leads to the algorithm being:
![[Pasted image 20240208215731.png]]
which now is forward-looking and has the stages back in time contributing in a meaningful, but fading way.

