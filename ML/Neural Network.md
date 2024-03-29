A neural network is a parameter function for function approximation that, according to the [[Universal Approximation Theorem]], can theoretically approximate any function to any degree of accuracy, depending on the architecture. 
## Architecture:
A standard feed-forward neural network consists of three main parts:
1. An input layer, where Inputs get fed in
2. A number of hidden layers with a variable number of neurons
3. An output layer, where projected labels are produced

Where the number of hidden layers as well as their respective neuron count largely determine the model complexity.

It sequentially applies [[Lineare Abbildungen|linear mappings]] and non-linear activation functions to the function arguments in a process called [[Neural Network#Forward-propagation |Forward-Propagation]] , where the linear weights are to be learned. 
They are then typically adjusted through gradient- or hessian-based methods through non-convex optimization methods in a process called [[Neural Network#Backwards-Propagation|Backwards-Propagation]] in order to minimize some objective function, usually a distance function between the desired and current outputs of the model.

### Weight Initialization:
The goal of a neural network is to find the optimal weight matrices to minimize the loss function. This, however, begs the question of how to initialize the weights initally. 
The intuitive approach, i.e. initializing all entries to some constant value, doesn't work as there exists a symmetry between neurons: in backpropagation, each neuron has the same inputs, and their value is thus **only** differentiated by the entries in the weight matrix. Therefore, with the same weights, all neurons in each layer would have the same output. And this would not change with backpropagation. 

Thus, the weights ought to be initialized randomly. Usually, values sampled uniformly from $[0; 1]$ are fine in practice. However, there are optimal ways with regards to convergence to initialized weights depending on the activation function applied at this layer.

#### Kaiming / He-Initialization
This initialization method has been proven optimal for the ReLU-Activation function. This avoids changing the magnitude of input signals exponentially, thus preventing the vanishing or exploding gradient problem.

##### Initialization Scheme:
$w_l \sim N(0, 2/n_l)$ 
This can be implemented in practice by 
np.random.normal(0.0, np.sqrt(2 / F_in))

#### Xavier Initialization
This initialization method has been proven optimal for the Sigmoid-Activation function.

##### Initialization Scheme:
$w_l = N(0, n_l + n_o)$
This can be implemented in practice by
np.random.normal(0.0, np.sqrt(2 / (F_in + F_out) ) )


### Activation Functions:
There are a number of widely used activation functions, which also all have an optimal weight initialization procedure:

#### Sigmoid:
The sigmoid function

##### Notes On Implementation:

##### Derivative:


### Output Functions:

### Loss Functions:


### Forward-propagation:
In forward propagation, the output can be produced from the input in the following sequence:
$L_{n + 1} =  f_{n + 1} (L_{n} \cdot \theta_{n + 1})$ 
where $L_0$ is the input layer and $L_o$ the output layer, with $o - 1$ hidden layers in between.
Here, $f_{n+1}$ is the non-linear activation function of the $n + 1$-Layer and $\theta_{n + 1}$ the weight matrix for the linear mapping between the two vector spaces of the [[Vektorraum|vectors]] representing the layer values. 
(This means that, if we want to map between a layer of $l$ and a layer of $g$ neurons, we need a $\theta \in R^{l \times g}$ , where the an entry $\theta_{i, j}$ is the weight of the neuron $i$ for the neuron $j$.)
One can see that, by sequentially transforming the input from layer to layer, it is 'propagated forward' to the output layer, thus the name.

Here, we assume the input to be a matrix of datapoints of size $m \times n$  with $m$ datapoints each consisting of $n$ features. Thus, each layer is an $m \times g$ matrix, where $g$ is the number of neurons in that layer.

Additionally, it is to note that, usually, an additional bias term is usually used instead of a usual [[Lineare Abbildungen|Linear Mapping]]. This can be implemented by adding a column of $1$'s to each neuron layer and adjusting the size of the weight [[Matrizen|matrices]] accordingly. 
However, this has notable consequences in backwards propagation as well as regularization.

After reaching $L_o$, the loss function $L(L_o, \hat{y})$ is evaluated between the predicted output layer values $L_o$ and the actual target values $\hat{y}$. 
It measures the distance between the two and is thus to be minimized, which is done using certain optimizers as well as backpropagation.     
### Backwards-Propagation
In backpropagtion, the gradient w.r.t. each weight matrix $\theta_n$, $\nabla_{\theta_n} L$ is to be determined so it can then be used in various optimizers. 

Note that, mathematically speaking, a neural network is nothing but a chain of parameterized functions (that follow a certain form, but that can be disregarded for now).
Thus, $L(L_o, \hat{y}) = L(  f(l(L_{o - 1})) , \hat{y}) = L(  f(l(g(h(L_{o - 2})))) , \hat{y})...$
Where $l,h$ would be the linear mappings and $f, g$ the activation functions applied between each layer.
Thus, determining $\nabla_{\theta_n} L(L_o, \hat{y})$ requires us to 'pass the gradient' back to layer $n$ by using the chain rule:
$\nabla_{\theta_n} L(L_o, \hat{y}) = \frac{\delta L(L_o, \hat{y})}{\delta \theta_n} =  \frac{\delta L(L_o, \hat{y})}{\delta L_o} \frac{\delta L_o}{\delta\theta_n} = \frac{\delta L(L_o, \hat{y})}{\delta L_o} \frac{\delta L_o}{\delta l(L_{o - 1})} \frac{\delta l(L_{o - 1})}{\delta \theta_n} = \frac{\delta L(L_o, \hat{y})}{\delta L_o} \frac{\delta L_o}{\delta l(L_{o - 1})} \frac{\delta l(L_{o - 1})}{\delta L_{o - 1}} \frac{\delta L_{o - 1}}{\delta \theta_n}$ 
$= ... = \frac{\delta L(L_o, \hat{y})}{\delta L_o} \frac{L_o}{l(L_{o - 1})} \frac{l(L_{o - 1})}{\delta L_{o - 1}} \frac{\delta L_{o - 1}}{\delta h(L_{o - 2})} ... \frac{\delta L_{n}}{\delta \theta_n}$ 

One realizes that the gradient calculation is largely the similar for multiple layers, as the only difference between two successive layers is that one directly calculates $\frac{\delta L_n}{\delta \theta_n}$  while the other one continuous the gradient calculation to calculate $\frac{\delta L_{n- 1}}{\delta \theta_{n- 1}}$. 
Thus, we can 'pass the gradient back' in one iteration and then use the appropriate values at each step to calculate the different weight gradients in just one step.

This act of once passing back the gradients back similarly to passing the input values forward is called **backwards propagation**. 

If one uses some elementary calculus and knowledge of linear algebra, they can see that the gradient w.r.t. the layer $n$ (**not** the next layers weights) can be calculated by the gradient w.r.t. the layer $n + 1$ by the series: NEEDS FIX:
$\nabla L_{n} =  (\nabla L_{n + 1} \cdot \theta_n^T ) * f'(L_{n-1})$  
where $*$ is the [[Hadamard-Operator]].
#### Autograd
An implementation of the computation above works fairly well 

## Training:
However, one cannot simply train the neural network by only applying backpropagation, as that only yields the gradient values. However, those can be used by a variety of gradient- and hessian-based optimizers:
## Regularization and Hyperparameters:

