# Asymptotic Notation

### $\Theta\ -\ Notation$
$$
\begin{align}

\Theta(g(n)) = \{f(n)\ there\ exists\ +ve\ constants\ c_{1},\ c_{2},\ and\ n_{o}\ such \\
that\ 0 \leq c_{1}g(n)\ \leq f(n)\ \leq c_{2} g(n)\ for\ all\ n\geq n_{o}\ \}
\end{align}
$$

### $O-Notation$

$$
\begin{align}

\Theta(g(n)) = \{f(n)\ there\ exists\ +ve\ constants\ c_{1}\ and\ n_{o}\\ such\
that\ 0  \leq f(n)\ \leq c\ g(n)\ for\ all\ n\geq n_{o}\ \}
\end{align}
$$

### $\Omega - Notation$
$$
\begin{align}

\Theta(g(n)) = \{f(n)\ there\ exists\ +ve\ constants\ c_{1}\ and\ n_{o}\\ such\
that\ 0  \leq c\ g(n)\ \leq f(n)\ for\ all\ n\geq n_{o}\ \}
\end{align}
$$

### $o - Notation$
$$
\begin{align}

\Theta(g(n)) = \{f(n)\ there\ exists\ +ve\ constants\ c_{1}\ and\ n_{o}\\ such\
that\ 0  < f(n)\ < c\ g(n)\ for\ all\ n\geq n_{o}\ \}
\end{align}
$$

### $\omega - Notation$
$$
\begin{align}

\Theta(g(n)) = \{f(n)\ there\ exists\ +ve\ constants\ c_{1}\ and\ n_{o}\\ such\
that\ 0  < c\ g(n)\ < f(n)\ for\ all\ n\geq n_{o}\ \}
\end{align}
$$
### Limit Method

For an algorithm if  

$\lim_{n \to +\infty} \dfrac{f(x)}{g(x)} = \infty$     $f(n) \in \omega(g(n))$

$\lim_{n \to +\infty} \dfrac{f(x)}{g(x)} = 0$     $f(n) \in o(g(n))$



[[recurrence-substitution|Recurrence-Substitution Method]]
