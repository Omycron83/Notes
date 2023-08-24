Gradient boosted trees are an ensemble learning technique that uses [[Decision Trees]] as a base optimizer, which are then fit to the residuals to further minimize the loss function.

## Algorithm 
This is done by iteratively constructing an [[Ensemble Learning|ensemble]] function  $F_{m + 1}(x_i) =  F_m (x_i) + h_m (x_i) = \hat{y_i}$ as a predictor. Thus, if one wanted to better the prediction of the predecessor $F_m$, they should choose $h_m(x_i) = \hat{y_i} - F_m(x_i)$ . This would thus minimize the absolute error of the prediction.
However, we often want to minimize a certain differentiable loss function, such as the [[Mean Squared Error|MSE]]:

$min \; L_{MSE}(y_i, F_m(x_i)) = L_{MSE}(h_m(x_i), 0)$ 

Minimizing this is not as trivial. 

