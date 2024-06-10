Random Variables $X$ can either be discrete or continous, i.e. are able to take on only a finite (or countable infinite) or infinite set of values. 

The probability in taking on each of those values is determined by a **probability mass function** or **pmf** that gives us the probability of the occurence of each random variable, i.e. $Pr(X = x)$.

In working with continous variables however, a problem arises: is the pmf even remotely uniformly distributed, the probability of any random variable being taken on tends to 0. 
However, this doesn't mean that its impossible, but rather that it [[Almost Surely]] won't happen.
Therefore, events are often characterized not by any specific, but rather by an intervall of events that might be taken on. 

This is given by a **cummulative distribution function** or **cdf** where we define $P(x) := P(X \le x)$ . Thus, if we want to know the probability of the value being between a number $a$ and a number $b$ is given by $P(a) - P(b) = P(b  < X \le a)$. 
It is obvious that $P$ needs to be monotonically increasing and have an infimum of 0 and a supremum of 1. ^e4b749

We define the **probability density function** as the derivative of the **cdf**: $p(x) = \frac{d}{dx}P(x)$ .
Now, we can compute the same probability by $\int^b_a  p(x)dx = P(b) - P(a)$. ^8517ec

The **inverse cdf** function, also called the quantile function $P^{-1}(q), q \in [0; 1]$ produces the random variable $x_q$ such that $P(X \le x_q) = q$, which is called the $q$'th quantile of $P$. 