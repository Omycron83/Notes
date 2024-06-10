Temporal difference methods are a class of reinforcement learning algorithms that use [[Bootstrap Methods|bootstrapping]] in form of an updated for a function utilizing the actual value at that time step as well as an estimate for the following time steps. Most are based on the temporal difference error discribed below.

# Temporal Difference Error
The temporal difference error is the error between the current estimate of the value function $V^\pi (s_t)$ and the actual value, which is estimated by [[Bootstrap Methods|bootstrapping]] the value function: $r_t + \gamma V^\pi(s_{t+1})$. Thus, temporal difference methods update the target by $r_t + \gamma V^\pi(s_{t+1}) - V^\pi (s_t)$.
