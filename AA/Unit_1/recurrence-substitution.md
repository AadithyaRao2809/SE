# Soln. of Recurrence Relations - Substitution

A method where we guess the bound for an algorithm and use mathematical induction to prove our guess.
this method can tell us if the bound is correct or not, but it cant tell us if it is the tight bound or not.

We assume an algorithm $T(n) \in O(g(n))$ time complexity, given by a relationship
$T(n) = a* T(n/b) +f(n)$

Assume $T(N) \in O(g(n))$ is true $\forall\  m<n$

Let m = n/b
we can say that  $T(m) \leq cg(m)$
using this if we can prove that $T(n) \leq cg(n)$
we can imply that $T(n) \in O(g(n))$

<hr>

Eg.  $T(n) = 2T(\frac{n}{2})+n$
Lets assume that $T(n) \in O(n\log n)$
Let m = n/2
$\quad T(m)\leq (cm)\ log(m)$
$= T(n/2)\leq (cn/2)\ log(n/2)$

$T(n)\ \ \ = 2T(n/2)+n$
$\qquad \quad \leq 2\ c(n/2) \ log(n/2)+n$
$\qquad \quad \leq cn \log(n/2)$
$\qquad \quad \leq cn(log\ n - log\ 2)+n$
$\qquad \quad \leq cn(log\ n - 1)+n$
$\qquad \quad \leq cn\ log\ n -cn +n$
$\qquad \quad \leq cn\ log\ n - n(c-1)$
$\qquad \quad \leq cn\ log\ n\quad \forall\ c>1$ 
this implies that $T(n) \in O(n\log n)$


[[recurrence-tree|Recurrence Tree]]

