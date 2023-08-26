A neural network is a parameter function for function approximation that, according to the [[Universal Approximation Theorem]], can theoretically approximate any function to any degree of accuracy, depending on the architecture. It sequentially applies linear mappings and non-linear activation functions to the function arguments in a process called [[Neural Network#Forward-propagation |Forward-Propagation]] , where the linear weights are to be learned. They are then typically adjusted through gradient- or hessian-based methods through non-convex optimization methods in a process called [[Neural Network#Backwards-Propagation|Backwards-Propagation]] in order to minimize some objective function, usually a distance function between the desired and current outputs of the model.
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
Here, $f_{n+1}$ is the non-linear activation function of the $n + 1$-Layer and $\theta_{n + 1}$ the matrix for the linear mapping between the two vector spaces of the vectors representing the layer values. 
(This means that, if we want to )

## Backwards-Propagation

## Regularization and Hyperparameter-Tuning