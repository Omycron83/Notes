Gradient boosted trees are an ensemble learning technique that uses [[Decision Trees]] as a weak learner, which are then fit to the residuals to further minimize the loss function.

## Algorithm 
This is done by iteratively constructing an [[Ensemble Learning|ensemble]] function  $F_{m}(x_i)$ consisting of weak learners $h_m, …, h_1$ as a predictor, which is calculated as a weighted sum of them: $F_m(x) = \sum_i^m y_m h_m(x)$ . 
This is done, as with most supervised learning algorithms, by minimizing some differentiable loss function $J$ such as the [[Mean Squared Error|MSE]].



![[PNG-Bild.png]]