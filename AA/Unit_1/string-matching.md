# String Matching
**Problem** To find the existence of a smaller string inside of a Bigger string

$\Sigma$ - Alphabet set
n - length of the string
m - length of the pattern

Most string matching algorithms rely on preprocessing to reduce time taken or matching.

| Algorithm             | Preprocssing Time                        | Matching Time               |
| --------------------- | ---------------------------------------- | --------------------------- |
| Naive                 | 0                                        | $O((n-m+1)m)$               |
| Rabin Karp            | $\Theta(m)$                              | $O((n-m+1))$                |
| Boyer Moore           | $O(               \| \Sigma        \| )$ | $O((n-m+1+ \| \Sigma \| ))$ |
| Finite State Automata | $O(m\|\Sigma\|)$                         | $\Theta(n)$                 |
| Knuth Morris Pratt    | $\Theta(m)$                              | $\Theta(n)$                   |

#### Naive String Matching Algorithm
This involves aligning the pattern wit the text and checking the characters one by one. If a mismatch occurs, then we shift the pattern by one and try again. 
This is not a very efficient algorithm as it checks for every position.

[[boyer-moore|Boyer Moore]]