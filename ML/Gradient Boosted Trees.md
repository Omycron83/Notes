Gradient boosted trees are an ensemble learning technique that uses [[Decision Trees]] as a weak learner, which are then fit to the residuals to further minimize the loss function.

## Algorithm 
This is done by iteratively constructing an [[Ensemble Learning|ensemble]] function  $F_{m}(x_i)$ consisting of weak learners $h_m, …, h_1$ from a family of algorithms $H$ as a predictor, which is calculated as a weighted sum of them: $F_m(x) = \sum_i^m \gamma_m h_m(x)$ . 
This is done, as with most supervised learning algorithms, by minimizing some differentiable loss function $L$ such as the [[Mean Squared Error|MSE]].

Specifically, a constant value $F_0 = \gamma_0$ is chosen initially as a ‘bias’, which is done by choosing the best expected approximation $F_0(x) = arg \; min_\gamma \sum_1^n L(y_i, \gamma_0)$.
From then on, this approximation is expanded in a greedy fashion, always choosing the next model in a way to minimize the expected error at this point in time:
$F_g(x) = \sum_i^{g - 1} \gamma_i h_i (x) + (arg \; min_{h \in H}[ \sum_1^n L(y_i, F_{g - 1} + \gamma_g h_g) ])(x)$  

This is not computationally feasible in an analytical way. 
However, using gradient descent (or *steepest descent*), one can use the negative direction of steepest descent as an approximation, thus choosing:
$F_g(x) = F_{g - 1}(x)  

![[PNG-Bild.png]]