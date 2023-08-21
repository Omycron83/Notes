
## Algorithm principle
Decision trees are a family of models based on the rule-based splitting of data into multiple categories based on features while traversing the tree in order to minimize some measure of impurity in the data available at each split during training. This is done until some criterion (often a max. of splits or min. of impurity) is reached, at which point the leaf node is assigned a certain value based on the datapoints remaining at itself. This 'fit' tree model is then defined by its splits. 

If one wants to predict another datapoint, they can then traverse the tree according to the splits and obtain a prediction by its end node.


Decision trees are usually fairly parsimoneous, and can geometrically be interpreted by partitioning the datapoints by hyperplanes.

## Classification Trees

## Regression Trees
