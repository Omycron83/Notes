Gradient boosted trees are an ensemble learning technique that uses [[Decision Trees]] as a base optimizer, which are then fit to the residuals to further minimize the loss function.

## Algorithm 
This is done iteratively by constructing an [[Ensemble Learning|ensemble]] function  $F_{m + 1}(x_i) =  F_m (x_i) + h_m (x_i) = \hat{y_i}$ as a predictor. Thus, if one wanted to further the ability 