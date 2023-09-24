![[Pasted image 20230922193457.png]]
#### Differences:
- Complexity
- Processing logic
- Neuroplasticity

#### Geometric Intuition

![[Pasted image 20230922194538.png]]

In 3D
$ax + by + cz + d \geq 0$
Equation of a plane, in 4D we get a hyperplane.

**Works only with linear or sort of linear data**


#### How to train
![](Pasted%20image%2020230922224148.png)
![](Pasted%20image%2020230922224353.png)
![](Pasted%20image%2020230922224609.png)
![](Pasted%20image%2020230923181128.png)
#### Problems with perceptron trick
![](Pasted%20image%2020230922230904.png)
1) Which line is better?
2) Problem with convergence, if you don't select random points properly, line wont move

**Use loss functions**
1) using distance formula is complex, instead substitute point in line, we get a $quantity \propto distance$
$$
L=\frac{1}{n} \sum_{i=1}^{n} max(0,-y_i f(x_i))
$$

for correct predictions, $y_i$ and $f(x_i)$ (prediction) have same sign, so the above returns 0 error 
![](Pasted%20image%2020230923020231.png)
![](Pasted%20image%2020230923020422.png)
![](Pasted%20image%2020230923020541.png)

| Loss function | Activation | Output |
| ------------- | ---------- | ------ |
|    Hinge Loss           |Step            |  perceptron-binary|
|log loss(binary cross)|sigmoid|logistic regression|
|categorical cross|softmax|softmax regression|
|mse|linear|linear regression|


#### Problems with Perceptron

Fails with non linear data



[index](MI/Unit_2/index.md)






