---
title: K Nearest Neighours
slno: 7
subject: mi
unit: 1

---

# K - Nearest Neighbours

It is an example of lazy learning, where the processing is postponed until a new data point arrives and must be classified. 

In this algorithm, instances are represented as points in a Cartesian nD space. 
The distance from this point to the nearest existing point $dist(x_1,x_2)$ is used to calculate nearest neighbours. This can be done for discrete or continuous values. 

For discrete valued sets, this returns the most common value among the training dataset, nearest to $x_q$ . For real valued data, kNN returns the mean distance value of the k nearest neighbours.

There are different ways of calculating the nearest neighbours.  
$$Euclidean\ d(x,y) = \sqrt{\sum\limits_{i=1}^{m}(x_{i}- y_i)^2}$$
$$Manhattan\ d(x,y) = \sqrt{\sum\limits_{i=1}^{m}|x_i-y_i|}$$

Once the distances are calculated the distances are sorted and among the k nearest neighbours, the new instance is classified to the class that has the most common points.

#### Choosing K
The value of k has to be decided before classification. It is recommended to keep it an odd number to reduce the chance of ties. 
As far as the value of k is concerned, choosing a low value for k leads to low bias and high variance. This leads to overfitting.
Choosing a large value for k leads to low variance high bias. This leads to underfitting.
A balance must be found to bring both variance and bias to an acceptable value. 

A good way to estimate a good value of k is to plot the error rate vs k value for different values of k. There will be one point where the error stops decreasing and begins to rise again, which is known as the **elbow point**. The point at the elbow is the one with least error.

![[Pasted image 20230828154348.png]]


## Weighted kNN
This is a variation of the kNN algorithm where the points closer to the new instance is given more weightage than farther points. This solves a problem where there is one close point and many farther points that can incorrectly influence the model to classify it in the class of the farther points.
$$ W_{i} = \dfrac{1}{distance(X_q,X_i)^m}$$
where m is how much you want to penalize the points that are far away.
the vote is taken based on $\sum{W_i}$ per class.




