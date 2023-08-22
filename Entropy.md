Entropy is a measure of information or 'suprise' inherent to the potential values of a random variable. 
This means that, if a highly likely event occurs, the entropy of the random variable is low, as it carries low information. If contrary, an event with low likelyhood occurs, the entropy is high.

For example, knowing that a certain number **isn't** the winning number in a lottery carries low information. However, knowing that **it is** the winning number carries a lot of information.
The possible outcome of getting any one side of a die is also of higher entropy than the outcome of getting any one side of a coin, as the probability of the former occuring is much higher.
## Derivation
This means that the entropy of any one event $E$ should be inversely correlated to the probability of an event, and, if the probability of the event is one, it should have an entropy of zero.
It should thus be monotonically decreasing, and should also satisfy $I(p_1 \cdot p_2) = I(p_1) + I(p_2)$ as the information given from two random events is the sum of the information learned from them.

A term satisfying this is: $I(E) = log(\frac{1}{P(E)}) = -log(P(E))$, where $P$ is the probability distribution and $I$ is the amount of informational content.
Usually 2 is chosen as a base for the logarithm (due to measuring it in 'bit'), however, a change of basis is always just a scalar away. 

## Definition:
Let $X$ be a random variable, having a sample-space of $L$ and a distribution of $P: L \rightarrow [0; 1]$ with $P(x) := P[X = x]$. Then, Shannon defines the Entropy $H: P \rightarrow R^+$ of the variable as: 
$H(X) = E[ I(X)  ] = E[ -log(P(X))]$ 
One can then explicitly write the expected value as:
$H(X) = - \sum_{x \in P} p(x) log(p(x))$ 
As  $log(0)$ is undefined, we assume that the upper limit is taken in the case of $p(x) = 0$. 

However, there are a number of other ways to define entropy mathematically.

## Conditional entropy
Assuming one has two variables $X, Y$ from sample spaces $L, G$, then the conditional entropy 
$H(X | Y)$ can be defined as:
$H(X|Y) = - \sum_{x,y \in L, G} p_{X, Y} (x, y) log( \frac{p_{X, Y} (x,y)}{p(x, y)} )$ 
It can be understood as the remaining 