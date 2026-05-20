**Reflect on the relationship between learning objectives and evaluation metrics. In
which scenarios is rating prediction preferable, and in which scenarios are ranking-based
approaches more appropriate?** 

### Core Principle 
The learning objective determines what the model optimizes for and evaluation metrics measure how well this goal is achieved. 

A rating prediction assigns a rating to each item (e.g. 4 stars) and optimizes MSE/RMSE. 
Ranking (BPR) optimizes pairwise ranking, meaning the quality of item ordering is measured (Precision, Recall, nDCG).

Models performing well on one objective can perform badly on the other. In general, item ranking is more useful for actual recommender systems. 

### When to Use What 
Rating prediction is preferable when users explicitly rate items and we need to 
estimate user satisfaction. It is not suited for implicit feedback because there is no rating given that can be predicted.
There are workarounds (e.g. setting all positive interactions to 1.0) but this is not optimal.  

Ranking-based approaches are more appropriate for implicit feedback where the absolute score is not relevant. 
They excel at comparing whether $a > b$, allowing the model to find good recommendations by learning item orderings directly. 
On the other hand, they are suboptimal for explicit feedback, because they usually ignore the rating information available, which 
regression based models can leverage. 