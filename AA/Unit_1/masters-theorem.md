# Master's Theorem

Any recurrence relation can be represented as  $T(n) = aT(\frac{n}{b})+f(n)$ 
where 
- $T(n)$ is monotonic. Eg. T(n) cannot be sin(n)
- $f(n)$ is of the form   $n^{k}\log^pn$. 

#### $if\ a > b^k$
$$T(n) \in \Theta(n^{\log_ba})$$ 

#### $if\ a = b^k$
$$
\begin{equation}
  T(n) =
    \begin{cases}
      \Theta(n^{log_{b}a}\ log^{p+1}n) & \text{if p>-1}\\
      \Theta(n^{log_{b}a}\ log\ logn) & \text{if p=-1}\\
      \Theta(n^{log_{b}a}) & \text{if p<-1}\\
    \end{cases}       
\end{equation}
$$
 
 
####  $if\ a < b^k$
$$
\begin{equation}
  T(n) =
    \begin{cases}
      \Theta(n^{k}log^pn) & \text{if p $\geq$ 0}\\
      \Theta(n^{k}) & \text{if p<0}\\
    \end{cases}       
\end{equation}
$$


[[string-matching|String Matching]]