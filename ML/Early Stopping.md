Early stopping is a machine learning technique used to potentiall reduce overfitting by stopping the training on a training set as soon as validation error starts to increase significantly.
This stems from the theory that, when training a model, the 'obvious', population-specific patterns are discovered first, while '[[Overfitting]]', i.e. the discovery of sample-specific patterns happens later in the training process, where a lack of required learning of the affirmentioned patterns leads to the discovery of the latter patterns. 
It is especially useful when working with [[Neural Network|a neural networks architecture]].
If that were the case, there would be an optimal point in time where most of the general, but few of the specific patterns are discovered:

![[Pasted image 20230822153344.png]]

Usually, the manifestation of this is supposed to show when the error on a validation set starts to increase from the hightend variance, while previously having decreased as bias was reduced.
Thus, practical implementations usually rely on the validation error to identify the point of early stopping. 
In 1997, the paper 'Early Stopping - but when?' (https://page.mi.fu-berlin.de/prechelt/Biblio/stop_tricks1997.pdf) tested multiple ways this could be done. Afterwards, they were ranked based on training time, efficiency (the amount of redundant calculations as the optimum had already been discovered), effectiveness (the quality of the network performance), and robustness (the sensitivity of the affirmentioned criteria based on learning problem) when applied to neural networks.
Accoding to the findings, one of the best tradeoffs was achieved in the $UP_3$ - criterion.
Here, the validation error was measured every 5 epochs and the training process thus partitioned into strips of 5 epochs. The training was stopped if the validation error increased over each of three successive strips (i.e. 4 samples of the validation error). At this point, the model parameters with the best validation score were used. 
