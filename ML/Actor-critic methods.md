Actor critic methods constitute a [[Bootstrap Methods|bootstrapping]] approach to the [[REINFORCE]] with baseline algorithm. A

Here, the update term $G_t - \hat{v}(S_t, w)$ is replaced by a bootstrap by using only the one-episode return $R_{t + 1}$ in combination with the following discounted value function estimate: $\gamma \hat{v}(S_{t+1}, w)$.
This yields:

![[Pasted image 20230822162001.png]]

and has the advantage, that the weights can be updated after each step, not requiring a full trace as with [[Monte Carlo Methods]].

This can also be generalized for larger partial traces, of not just length one.
