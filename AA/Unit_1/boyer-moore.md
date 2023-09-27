# Boyer Moore

Boyer-Moore string matching algorithm, creates two tables while prepossessing the data. one is the bad symbol shift and the other is the good suffix shift. Both of these are used to determine the shift amount.

**Bad Symbol Shift** is of size $|\Sigma|$ and it determines
- the distance of every character from the ending.
- for the last character, it second occurrence must be taken. 
- If a character doesn't exist, then its value should be the length of the pattern.
Eg. If the pattern is `AABCAC`  for the alphabet $\{A,B,C,D\}$ is

| char | $d_1$ |
| ---- | ----- |
| A    | 1     | 
| B    | 3     |
| C    | 2     |
| D    | 6     |

Th output from the bad symbol shift is $d_1$

**Good Suffix Shift** is of size m and it has
- the position from a suffix of size $i$ when the suffix letters  repeat
- if the suffix exists partially, at the beginning, we take the value as the distance of the start of the suffix to the start of the partial suffix.
Eg. 

| k   | pattern           | $d_2$ |
| --- | ----------------- | ----- |
| 1   | ABC**B**A<u>B</u> | 2     |
| 2   | **AB**CB<u>AB</u> | 4     |
| 3   | **AB**C<u>BAB</u> | 4     |
| 4   | **AB**<u>CBAB</u> | 4     |
| 5   | **A**<u><b>B</b>CBAB</u> |4       |


When a mismatch occurs, we look at the character that caused the mismatched and look at the good symbol shift to find $d_1$.
We then Look at how many characters matched before the mismatch and use that to calculate $d_2$.
We determine how much the patter should shift by taking $max(d_1,d_2)$. 

[[rabin-karp|Rabin Karp]]