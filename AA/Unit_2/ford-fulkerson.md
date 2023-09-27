# Ford Fulkerson Method

This is called a method and not an algorithm. It can be implemented in many different ways with different runtimes, but imply the same basic methodology.

The idea is to iteratively increase the flow by finding an augmenting path in the residual network. 

A Flow represents a path from source to the sink where the value of the flow is the edge with the least capacity(weight).

**To find the flow path**
1. find an augmenting path
2. compute the capacity of the bottleneck
3. augment each edge and total flow

Augmenting a path involves either pushing forward in a non full vertex or a backward edge from a non empty vertex.
