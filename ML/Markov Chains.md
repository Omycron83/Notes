Markov chains are a type of stochastic model describing a sequence where the next state in that sequence is stochastically determined based on the state of the previous envent(‘s).
They are characterized by the markov properly, which is usually assumed in dynamic programming and reinforcement learning.

# Markov Property:
A [[Stochastic Process]] is said to fulfill the Markov property, if INSERT FORMAL DEFINITION

In the discrete case, one can nicely reformulate this as:
$P(X_n = x_n | X_{n-1} = x_{n-1}, …, X_0 = x_0) = P(X_n = x_n | X_{n-1} = x_{n-1})$ 
I.e. a stochastic process fulfills the Markov property if the probability of the next state does not depend on the probability of the current state.
It is to note that the state space must be constant for all $i \in I$ of the index set of the stochastic process. 
A stochastic process fulfilling the Markov property is also called a Markov process.


# (First Order) Markov Chains:
A first order Markov chain refers to a markov process having either a discrete (or countable) state space or discrete index set (or both).

## Markov Chains in graph theory:
A Markov chain can be represented using a graph, where each vertex is a reachable state and each edge is a transition between two states having a certain probability (thus all outgoing edges from some vertex having a sum of 1 (unless its a terminal state)).
Example:
![[Pasted image 20230828092536.png]]

# Matrix Description:
A Markov process can be described using a transition matrix similar to a usual matrix representation in a graph. This is done by having each row represent some state, with each corresponding column entry representing the probability of reaching the state represented by that column. For the above example:


