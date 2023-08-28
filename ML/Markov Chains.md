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
A first order Markov chain refers to a markov process having either a discrete state space or discrete index set (or both), i.e. it either has a discrete space of possible states or a discrete set of points in time.
