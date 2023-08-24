Gradient boosted trees are an ensemble learning technique that uses [[Decision Trees]] as a weak learner, which are then fit to the residuals to further minimize the loss function.

## Algorithm 
This is done by iteratively constructing an [[Ensemble Learning|ensemble]] function  $F_{m}(x_i)$ consisting of weak learners $h_m, …, h_1$ as a predictor. The prediction is iteratively improved by using gradient descent 
However, we often want to minimize a certain differentiable loss function, such as the [[Mean Squared Error|MSE]]:


![[PNG-Bild.png]]