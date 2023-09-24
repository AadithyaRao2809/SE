# Regression

Statistical method to understand the relationship between independent variables **(x)**
and features or dependent variables **(y)**. 
The value of y will depend on the independent variables (X1, X2, X3 ...)


#### Linear Regression
It is a type of regression where we try to find a linear relation between the independent and the dependent variables. 

There are many types of linear regression. Simple linear regression involves only one independent and one dependent variable. Multiple linear regression has many independent variables and one dependent variable. 

#### Logistic Regression
A supervised machine learning algorithm, mainly used for binary classification where the objective is to find the probability that an instance belongs to one of two classes.
Logistic Regression predicts the output of a categorical variable.

$p = \dfrac{Outcomes\ of\ Interest}{All\ Possible\ Outcomes}$

$Odds= \dfrac{Probability\ of\ an\ event\ occurring}{Probabilty\ of\ an\ event\ not\ occuring}$

odds ratio is the ratio of the odds of two events.
Eg. One coin has 0.6 odds of heads and another coin has 0.2 odds of heads. The odds ratio is 3, which means you are three times as likely to get heads on the first coin than the second one. 

**Logit function** log-odds of the event   
$Logit(p) = ln(odds) = ln(\dfrac{p}{1-p})\ =\ ln(p)-ln(1-p)$ 
$Logit^{-1}(p)= \dfrac{1}{1+e^{-z}}$ where z is the linear combination of the input variables.
$z = \beta_{0}+\beta_{1}X_{1}+\beta_{2}X_{2}\ +\ ...\beta_{p}X_p$

Inverse Logit function is nothing but the sigmoid fn.

When a threshold is set on the predicted probability, it becomes a classifier. When the probability is below the threshold, it is classified as 0 and when the probability is above threshold, it is classified as 1. 


#### Loss function in Logistic Regression
Binary cross entropy is used in logistic regression. BCE is given by
$L(y,\hat{y}) = - [y\ log(\hat{y})\ +\ (1-y)\ log(1-\hat{y})]$
We need to find $\frac{\partial L}{\partial m}$ and $\frac{\partial L}{\partial b}$ as they are required for gradient descent. 


[k-nearest-neighbours](k-nearest-neighbours.md)