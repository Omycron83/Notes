Usually, in the experience-replay mechanism used in i.e. DQN-Methods, transitions (or traces) are stored in some datastructure and then uniformly sampled to facilitate training on them. 
This removes temporal correlation between recent and past experiences, making one able to learn efficiently from experiences.

This, however, is inefficient as the relevance of samples may drastically change with the current policy: some samples may be more or less suprising, redundant or relevant than others and thus provide different amounts of information in the training of the neural network.

That can however be fixed by using a prioritised experience-replay mechanism which prioritizes transition with high temporal difference error, the priority of each transition being the "largeness" of its TD-Error . In order to reduce a loss of diversity, stochastic prioritization is used, and in order to reduce bias, importance sampling is used. 

Sampling is done using a sampling probability, which is calculated by:
$P(i) = \frac{p_i^\alpha}{\sum_k p_k^\alpha}$ , i.e. by dividing the exponentiated priority of the sample $i$ by the total sum of exponentiated priorities, where $\alpha$ determines the amount of importance priority plays: if $\alpha$ is close to 0, it plays little to no importance while it plays an exponentially higher importance with an increasing $\alpha$. 


![[Pasted image 20230812044531.png]]