## Algorithm principle
Decision trees are a family of models based on recursively binarily splitting of data into multiple subset (mostly 2 to guarantee computational feasibility) based on features, where the prediction value is based on the relevant subset. 
This is usually done by ordering the datapoints by some numerically encoded feature. Then, the datapoints are assigned quantiles according to this ordering. The resulting splits are usually the mean of the feature values of the two bordering datapoints of two quantiles. 
This is done practically by traversing the tree in order to minimize some measure of impurity or maximize information gain in the subset at each split during training (binary recursive partitioning). 
... Until some criterion  is reached, at which point the leaf node is assigned a certain value based on the datapoints remaining at itself (or in that quantile). This 'fit' tree model is then defined by its splits (or its quantiles). 

Thus, the tree partitions the input space into disjoint regions and predicts a constant value in each region based on the datapoints found in it during training.

If one wants to predict another datapoint, they can then traverse the tree according to the splits and obtain a prediction by its end node. The prediction at each node is usually the mean of the datapoint that reached it during training.

Decision trees are usually fairly parsimoneous, and can geometrically be interpreted by partitioning the datapoints by hyperplanes. They are used in more sophisticated algorithms, such as [[Gradient Boosted Trees]] or [[Random Forests]] . 

### Split criteria
There are multiple common ways to reduce overfitting during training:
1. The cardinality of the subset is to small
2. The depth of the tree is to large
3. The information gained is to small
The parameters that govern the level needed for further splitting are often hyperparameters

### Example
As an example, say one wanted to predict the value of an item during shopping based on features such as the category of the item, the brand, the weight or the level of the storage shelf it is stored in. Now, one obtains a training set that encodes those features into numerical values of a number of product. It has an average of $4.56$ Euros in price and a variance of $6.23$ Euros$^2$ (we assume the predicted values to be the mean and the entropy to be the variance in this model). Thus, if one had to predict the value of an item without any splits, they'd predict the mean price of $6.23$ Euros, but wouldn't be very sure as the price varies a lot within that set. 
At first, one tries out all the possible inequalities that could be found in the feature values: for example, they might try separating the product by those who have a shelf level above 3 and those that have one below or at 3. If this is done, the subset of products which has a shelf level above 3 has a mean price of $5.54$ and a variance of $3.89$ with 39 products with it. The other subset has a mean of $3.45$ and a variance of $5.39$, with 28 products in it. Thus, splitting the training set based on this inequality, a the weighted variance was reduced from $6.23$ to $\frac{39}{67} 3.89 + \frac{28}{67} 3.45 = 3.7$, and if one where to predict the value of a product based on the mean of part of the split it would fall into, the reduced variance would make the prediction more certain. Thus, information was gained.
This, coincidentally, was the split that minized the total variance of all the possible splits. This splitting is done again recursively again until some stopping criterion is met. 

## Classification Trees

## Regression Trees
