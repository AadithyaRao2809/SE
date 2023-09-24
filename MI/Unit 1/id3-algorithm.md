# ID3 Algorithm for Decision Trees

Decision trees are a non supervised learning algorithm. They are mainly used for classification, and make use of a tree structure to determine the effect of attributes on the outcome.

The goal of a decision tree is to have the least possible height while being accurate at classifying the data. which means we should be able to reach a conclusion with as little steps as possible.

To build a decision tree with the lowest possible height, we must get a way to figure out which attributes is important. For Classification **Gini Impurity** is used as a heuristic.

This is where the ID3(Iterative Dichotomizer 3) algorithm is used.
- Entropy: indicator of non homogeneity
- Information gain: Entropy before the split - Entropy after the split (should be as high as possible)


First get the number of positive outcomes in the dataset $(m)$ and the number of negative outcomes int the dataset$(n)$ and use it to calculate the entropy

$$
 E(S) = \dfrac{-m}{m+n}\ log_2\left({\frac{m}{m+n}}\right)+ \dfrac{-n}{m+n}\ log_2\left({\frac{n}{m+n}}\right)


$$
*Note: Entropy for a given attribute $E(S,a)$ is the number of positive and negative outcomes for a particular value of an attribute*

Next find the average information of each attribute
$$
I(S,a) = \dfrac{\sum p_{i}+n_{i}}{p+n} *E(S,a)
$$
where $p_i$ and $n_i$ are the positive and negative outcomes of the $i^{th}$ value of attribute $a$ 

We can finally use this to get the Information Gain of a particular attribute
$$
G(S,a) = E(S) - I(S,a)
$$

We use the attribute with the highest information gain the most important decision. This process has to be then repeated for all the attributes in all the sub-trees as one decision may lead to one attribute as more important than the other sub-trees.  


### Problems with Decision trees
The most prevalent issue with decision trees is that is prone to overfitting. It also has issues when the data is continuous. It also cannot handle missing values and attributes with different costs.

#### Overfitting 
It is when the model becomes too specific to the training set. This becomes worse when the data has noise, is too small, or is biased.  

**Formal Definition** Consider error of hypothesis $h$ over training data $error_{t}(h)$ and error over the entire dataset $error_D(h)$ then the hypothesis $h$ overfits the data if there is an alternate hypothesis $h'$ such that
$\qquad error_t(h)<error_t(h')$
and
$\qquad error_D(h)>error_D(h')$


A way to avoid overfitting is to prune the tree to ensure it doesn't become too long.

#### Pruning
Removing the lower levels of the decision which is believed to resemble the inaccuracies in the test data. This can be done by
- **Reduced Error Pruning**
- **Rule Post Pruning**

### Dealing with Continuous Data
If the attributes are continuous values, taking each value is not an option. So the decisions that need to be taken will be with respect to threshold values. 

[Decision Boundaries](decision-boundaries)
