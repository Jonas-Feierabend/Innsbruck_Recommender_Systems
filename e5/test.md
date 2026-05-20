Here we have extracted the user as well as the item features and have reduced the dimensions with PCA. 
A PCA (Principal Component Analysis) is a mathematical process to reduce dimension. It looks for the best dimensions which 
offer the biggest varianze between the items. 

**Interpretation**   
With the PCA we have reduced the dimensions from 50 (this was the features hyperparameter) to two dimensions. This may or may not align with reality. 
If there are two dimensions which are very important (e.g. "is this film rated >4 stars"), then the result of the PCA can align with reality quite well. 
In our case, we could somehow draw a circle around all green and red dots, but this would incorporate probably 1/3 of all films. Meaning this doesn't really show which films are actually interesting to the user. 
Furthermore, if we selected the 10 films with the lowest Euclidean distance to the red star, we probably wouldn't find a single movie the system actually wants to recommend to the user. 


We can also see from the components that they explain 4.67% and 3.45% of the variance. This means that we can only "see about 8% of the variance", which can be vaguely interpreted as seeing only 1/10 of the deciding factors. This is similar to only looking at an actor in a supporting role and based solely on him or her, recommending the film to a user. Because of this massive information loss, this 2D plot should be interpreted very cautiously because it is not a reliable tool to verify individual recommendations. 


