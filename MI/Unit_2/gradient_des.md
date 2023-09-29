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


### Vanishing Gradient
- deep layers, many times come across activation function derivatives that have (0,1] range, so it'll keep getting smaller 
- sigmoid, tanh
- can use relu but dying gradient problem for 0 or neg activations
- there is exploding gradient problem which is the opposite to this (in RNN)





