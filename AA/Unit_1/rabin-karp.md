# Rabin Karp
This is a hashing based algorithm. It involves 
- Calculating the has value of the pattern text. 
- Then compute the hash value of a sliding window of the text, the size of the pattern. 
- Compare the hash value of the window with the has value of the pattern. 
- If they are not equal move the window.
Widely used for multiple pattern searches.

To compute hash value for str[] with $|\Sigma|$ = n and pattern size m
```
hash <=0
for i=0; i<m; i++
	hash <= b*hash + str[i]
	
```
This requires $\Theta(n)$

To update hash value after sliding window of size m
`hash(i)` is the hash value of the window starting at position `i`

```
hash(i+1) <= hash(i)*n - str[i]*n^m + str[i+m]
```

**Large Pattern strings** are hard to compute as the resulting hash number does not fit in a single `long` or `long long` number. 
We must store the hash value as a modulus of a prime number.  So there can be cases when the hash value is the same but the string need not match, but if the hash value is not the same, we know that the string did not match. 
When two different strings have the same hash value its is called a **spurious hit**.
So if the hash value is same, we must also validate character-by-character.

[[finite-state-automata|Finite State Automata]]