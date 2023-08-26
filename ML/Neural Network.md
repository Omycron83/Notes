A neural network is a parameter function for function approximation that, according to the [[Universal Approximation Theorem]], can theoretically approximate any function to any degree of accuracy, depending on the architecture. 
It sequentially applies linear mappings and non-linear activation functions to the function arguments in a process called [[Neural Network#Forward-propagation |Forward-Propagation]] , where the linear weights are to be learned. 
They are then typically adjusted through gradient- or hessian-based methods through non-convex optimization methods in a process called [[Neural Network#Backwards-Propagation|Backwards-Propagation]] in order to minimize some objective function, usually a distance function between the desired and current outputs of the model.
## Architecture:
A standard feed-forward neural network consists of three main parts:
1. An input layer, where Inputs get fed in
2. A number of hidden layers with a variable number of neurons
3. An output layer, where projected labels are produced

Where the number of hidden layers as well as their neuron count largely determine the model complexity.
## Forward-propagation:
In forward propagation, the output can be produced from the input in the following sequence:
$L_{n + 1} =  f_{n + 1} (L_{n} \cdot \theta_{n + 1})$ 
where $L_0$ is the input layer and $L_o$ the output layer, with $o - 1$ hidden layers in between.
Here, $f_{n+1}$ is the non-linear activation function of the $n + 1$-Layer and $\theta_{n + 1}$ the weight matrix for the linear mapping between the two vector spaces of the vectors representing the layer values. 
(This means that, if we want to map between a layer of $l$ and a layer of $g$ neurons, we need a $\theta \in R^{l \times g}$ .)

Here, we assume the input to be a matrix of datapoints of size $m \times n$  with $m$ datapoints each consisting of $n$ features. Thus, each layer is an $m \times g$ matrix, where $g$ is the number of neurons in that layer.

Additionally, it is to note that, usually, an additional bias term is usually used instead of a usual [[Lineare Abbildungen|Linear Mapping]]. This can be implemented by adding a column of $1$'s to each neuron layer and adjusting the size of the weight [[Matrizen|matrices]] accordingly. 
However, this has notable consequences in backwards propagation as well as regularization.

After reaching $L_o$, the loss function $L(L_o, \hat{y})$ is evaluated between the predicted output layer values $L_o$ and the actual target values $\hat{y}$. 
It measures the distance between the two and is thus to be minimized, which is done using certain optimizers as well as backpropagation.     
## Backwards-Propagation
In backpropagtion, the gradient w.r.t. each weight matrix $\theta_n$  

## Optimizers
## Regularization and Hyperparameter-Tuning