Based on https://arxiv.org/abs/1511.05952
Usually, in the experience-replay mechanism used in i.e.  [[DDQN - Architecture|DQN-Methods]], transitions (or traces) are stored in some datastructure and then uniformly sampled to facilitate training on them. 
This removes temporal correlation between recent and past experiences, making one able to learn efficiently from experiences.

This, however, is inefficient as the relevance of samples may drastically change with the current policy: some samples may be more or less suprising, redundant or relevant than others and thus provide different amounts of information in the training of the neural network.

That can however be fixed by using a prioritised experience-replay mechanism which prioritizes transition with high temporal difference error, the priority of each transition being the "largeness" of its TD-Error. In order to reduce a loss of diversity, stochastic prioritization is used, and in order to reduce bias, importance sampling is used. 

However, there are two options that can be used as a priority measure: either the absolute error (plus some small constant so that there is always a probability of being sampled) $|\delta| + \epsilon$ or the inverse rank of its error when sorted by decreasing error: $\frac{1}{rank(\delta)}$ .  
Empirically, a the latter method has been proven more robust to outliers, making it the distribution of choice from hereon out.

Sampling is done using a sampling probability, which is calculated by:
$P(i) = \frac{p_i^\alpha}{\sum_k p_k^\alpha}$ , i.e. by dividing the exponentiated priority of the sample $i$ by the total sum of exponentiated priorities, where $\alpha$ determines the amount of importance priority plays: if $\alpha$ is close to 0, it plays little to no importance while it plays an exponentially higher importance with an increasing $\alpha$, making it a hyperparameter.

In order to decrease the bias stemming from the difference in the transition distribution fed to the network and the transition distribution actually expected, one can correct the weight of the sampled transitions by multiplying it by an importance-sampling weight, which divides both by the amount of transitions as well as the sampling probability, and then exponentiates by another hyperparameter $\beta$, which controlls how much is corrected (where $0$ means no correction, $1$ means fully compensating):
$w_i = (\frac{1}{N} \cdot \frac{1}{P(i)})^\beta$ . For stability reasons, it also makes sense to normalize the weights, i.e. dividing them by the maximum weight in order to only scale impacts upwards, not downwards.

Now, only the implementation of this sampling remains. 
There are multiple ways this could be done efficiently, but the one chosen is approximating the cdf by a piecewise linear function with $k$ segments of equal probability, where the section boundaries can be computed as long as $N$ and $\alpha$ stay the same. At runtime, we sample a segment and then sample uniformly among the transitions within it. 
If one uses a minibatch-based algorithms, they can put $k =$ size of minibatch and then sample one transition out of each segment, so that the minibatch is balanced out in a way so that there is always one transition with large, medium and small error included. 


The full algorithm in pseudocode:

![[Pasted image 20230812044531.png]]