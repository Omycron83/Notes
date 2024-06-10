Bayesian hyperparameter optimization tries to combine the advantages of an 'intelligent' exploration of the search space with the efficiency and reproducibility gained by an algorithmized approach.

In bayesian hyperparameter tuning, the minimum of a function (here the function mapping a vector or point specific of **hyperparameters** $R^n \rightarrow R$ to the real-valued **cross-validation** loss) is found by evaluating points gathered (i.e. observations of hyperparameter combinations tested) on a distribution over functions that are supposed to surrogate that function (usually by using [[Gaussian Processes]]) and then using the knowledge gathered at that point to, using [[Bayes Theorem]], get a better estimate of reasonable surrogate functions. 

For example, if a point is sampled with some combination of hyperparameters, yielding a cross-validation score of $0.5$, it is known that the surrogate function must have a value of $0.5$ at that point. It is also known that, around that point, the function is likely to be somewhere close to that value as well. 

The advantage comes not only through these spatial correlations supplied through the surrogate functions (aspect such as continuity that are not considered in the other methods) but also with the ability to reasonably choose the next point to sample from the cross-validation function: using an acquisition function, one can optimize a trade-off between exploration and exploitation: 
if, after a large number of points sampled, some value is significantly lower than the others, it makes sense to sample close to that point, as the minimum is most likely to be found in its region. 

However, if only few points were explored and some regions haven't largely been explored at all, it makes more sense to next choose a point in those unexplored regions, as there is a possibility of the optimum being there. This tradeoff is optimized using the surrogate function through some constrained objective function constructed by some specific optimization algorithm chosen.

Through the combination of the aforementioned approaches, this technique has been empirically shown to be greately more efficient than random search (up to ca. 121 times as efficient when carefully finetuned, ca. 16.5 times as efficient with the method we used.)

*Sources:* 
-  A Tutorial on Bayesian Optimization of Expensive Cost Functions (2010), Brochu et al 
([arxiv.org/pdf/1012.2599.pdf](https://arxiv.org/pdf/1012.2599.pdf))
- Bayesian Optimization is Superior to Random Search for Machine Learning Hyperparameter Tuning: Analysis of the Black-Box Optimization Challenge 2020, Turner et al  (https://arxiv.org/abs/2104.10201)

