### Batch Gradient Descent

- Run all points at once, (dot prod of matrices) get predictions , we know actual, calc cost for each and sum it up
- So every epoch, w, b updates once.
- batch is faster running
- smooth curve, as it is averaging->asking every point
 ![](../../Attachments/gradient_des-20230924.png)
 - cant vectorize large batches of data, would not fit in memory

### Stochastic

- Shuffle data
- calc prediction->loss->update w, b
- stochastic converges faster though
- due to jaggedness, it can avoid local minima and find global
- even though it converges faster, it may not be exact

### Mini Batch
- Mix of both, set a batch size and do


*fun fact: batch sizes are generally in multiples of 2 due to memory optimizations.*


### Problems
- local minima
- saddle point(flat for long slow training)
- High curvature(Large Bulge harder to traverse)


### SGD With Momentum
- avoids high curvature
- flat areas
- local minimas
![](../../Attachments/gradient_des-20230929.png)
![](../../Attachments/gradient_des-20230929-10.png)
- $\beta$  is decaying factor if its .9 then current is .9 of prev which is .9 of its prev
-  prev influence=$\frac{1}{1-\beta}$
-  $\beta=1$ is like no friction pendulum

It's faster,but its unstable before settling down,oscillates around miniman

### Nesterov Accelerated gradient
![](../../Attachments/gradient_des-20230929-9.png)
- Smaller bounces around minima
- but lesser momentum than sgd with momentum
### AdaGrad
`Adaptive gradient`

- if you haven't normalized, scale is different use AdaGrad
- sparse input(for different w, low loss as it is sparse,so it will elongate,so its flat along one axis and you aren't moving there)
- 
![[../../Attachments/gradient_des20230929.excalidraw.svg]]
%%[[../../Attachments/gradient_des20230929.excalidraw.md|🖋 Edit in Excalidraw]], and the [[../../Attachments/gradient_des20230929.excalidraw.dark.svg|dark exported image]]%%

*Solution*
![](../../Attachments/gradient_des-20230929-4.png)
- Different learning rates
- If sum of previous gradients are large->reduce learning rate
- If small->increase

*Problems*
- as you approach minima,sum of previous gradients are large,so learning rate much lesser cannot converge at minima,expecially for the non sparse weight,as sum of previous gradients is large
- use in regression not neural nets


### RMSprop
`root mean square prop`
fixes the problems adagrad had
![](../../Attachments/gradient_des-20230929-6.png)
![](../../Attachments/gradient_des-20230929-11.png)
Weightage to recent epochs

**It is a very powerful technique**

### Adam
![](../../Attachments/gradient_des-20230929-7.png)
![](../../Attachments/gradient_des-20230929-8.png)
 
### Vanishing Gradient
- deep layers, many times come across activation function derivatives that have (0,1] range, so it'll keep getting smaller 
- sigmoid, tanh
- can use relu but dying gradient problem for 0 or neg activations
- there is exploding gradient problem which is the opposite to this (in RNN)
- Proper weight initialization![](../../Attachments/gradient_des-20230929-12.png)





