
# Amortized Analysis


Amortized analysis is a way of getting the true average cost of an operation. Instead of looking at the cost with respect to the probability, we analyze the average cost of every operation. 
It shows that even though a singular operation might be expensive, over a large sample the average cost of each operation is small. It gives the average performance of each operation in the Worst Case.

Eg. Dynamic table is an array that doubles in size every time an item needs to be appended and it is full. If the current size of the table is not $2^n$, where n is an integer, an append operation is very inexpensive O(n). If the size of the table is a power of two, doubling the table size takes O(n) time, and then appending to that takes O(1).

There are two ways of calculating the amortized cost of a series of operations
- Aggregate Method
- Accounting Method

To understand the different methods, take the example of stack, which supports `push()` and
`pop()`, which take O(1), and `multipop()`, which takes O(n).
### Aggregate Method
In this method, the cost for n successive operations is calculated - T(f(n)). This is divided by the number of operations n to give us the amortized cost of the operations.

When we start with an empty stack, there can only be at most equal number of push and pop operations, so even though `multipop()` takes more time, it can only be performed as many times as the push() operations. So it can at most be O(n). So the amortized cost is O(1) for n operations.

### Accounting Method
A charge is assigned to each of the operations. If for a given operation, the amortized cost is lesser than the actual cost of the operation, it can be saved as **credits**. This can then be used later on when the amortized cost is greater than the actual cost. It is very important to chose amortized cost correctly to prove the bound. 

let the amortized cost of an operation be $\hat{c_i}$  and the actual cost of an operation is $c_i$ then  $\sum\limits_{i=0}^{n}\hat{c_{i}}\ \geq \sum\limits_{i=0}^{n}{c_{i}}$    is to be true for all sequences of n operations.

We know that there can be as many pops as there are pushes. We can assign the amortized cost as follows

| Operation   | Cost | Amortized <br>Cost |
| ----------- | ---- | ------------------ |
| push        | 1    | 2                  |
| pop         | 1    | 0                  |
| multipop(k) | k    | 0                  |

For every push operation one unit is used by the operation and the other unit is stored as credit. As there can never be more pushes than pop, when n elements are push, n credits are stored. This is used to perform at most n pops, so the amortized cost will be greater than or equal to actual cost.

### Potential Method
In this method, a potential function $\phi(D_i)$ is defined and used to calculate amortized cost $(\hat{C_{i}}).$  The amortized cost of the $i^{th}$ operation is 
$$
\hat{C_{i}}= C_{i}+ \phi(D_{i})- \phi({D_{i-1}})
$$

The actual cost of the operation is $C_i$ and the difference is the change in potential $\Delta \phi_i$. If $\Delta \phi_{i}>0$ means that it has been overcharged and if $\Delta \phi_{i}< 0$ it means that it has been undercharged. 

**Potential function for Stack** $\phi(d_i)$: Number of elements

- Push Operation - 1 +(n+1) -(n) = **2**
- Pop Operation - 1 + (n-1) - (n) = **0**
- Multi-pop Operation - k + (n-k) - (n) = **0**




[[masters-theorem|Master's Theorem]]