The Kullback-Leibler divergence, also called relative entropy, is a measure of distance between one probability distributions $P$ to another distribution $Q$ denoted $D_{KL}(P || Q)$. 
Its not a [[Metric Spaces|metric]] as it is neither symmetric nor satisfies the triangle inequality, and is instead, as the name suggests, a type of statistical divergence.

Usually, $P$ represents some observation or measured probability distribution while $Q$ represents a theory or model of $P$. 

## Definition:
For two discrete probability distributions $Q, P$, the KL-Divergence between the two is defined as $D_{KL}(P  || Q) = \sum_{x \in X} P(x) log(\frac{P(X)}{Q(X)})$ , where $P(X)$ or $Q(X) = 0$ is assumed to be zero.
