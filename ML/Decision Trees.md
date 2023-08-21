
## Algorithm principle
Decision trees are a family of models based on recursively binarily splitting of data into multiple subset based on the subset features, where the prediction value is based on the relevant subset. 
This is done in by traversing the tree in order to minimize some measure of impurity or information gain in the subset at each split during training (binary recursive partitioning). 
This is done until some criterion  is reached, at which point the leaf node is assigned a certain value based on the datapoints remaining at itself. This 'fit' tree model is then defined by its splits. 

If one wants to predict another datapoint, they can then traverse the tree according to the splits and obtain a prediction by its end node. The prediction at each node is usually the mean of the datapoint that reached it during training.


Decision trees are usually fairly parsimoneous, and can geometrically be interpreted by partitioning the datapoints by hyperplanes.

### Split criteria
There are multiple common ways to reduce overfitting during training:
1. The cardinality of the subset is to small
2. The depth of the tree is to large
3. The information gained is to small
The parameters that govern the level needed for further splitting are often hyperparameters


## Classification Trees

## Regression Trees
