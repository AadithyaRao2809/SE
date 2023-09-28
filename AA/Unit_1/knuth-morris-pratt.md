# Knuth Morris Pratt
T is a string matching algorithm that optimizes the naive string matching algorithm by creating an lps table, where it stores the longest prefix that is also the suffix of a substring of the pattern. 

 In this algorithm, the index of the text is never backtracked, but the pattern string will.
#### Creation of lps table
- We first create a table the size of the pattern string.
- then for every index find the index of prefix that is same as the suffix.
- If no such string, enter 0


Eg. Pattern sting `ababaca`

| str      | lps |
| -------- | --- |
| a        | 0   |
| ab       | 0   |
| aba      | 1   |
| abab     | 2   |
| ababa   | 3   |
| ababac   | 0   |
| ababaca  | 1   |

**Final lps Table**

| a   | b   | a   | b   | a   | c   | a   |
| --- | --- | --- | --- | --- | --- | --- |
| 0   | 0   | 1   | 2   | 3   | 0   | 1   | 

##### The Matching

- We start with an index `i` at the start of the string and an index `j` at the start of the pattern.  
- On a successful character match, we increment both `i`and  `j`.
- If there is a mismatch and `j` is at 0, we increment only `i` . 
- On Mismatch if `j` is not 0, we set `j` to `lps[j-1]`, and continue the string matching. 
- If `i` reaches the size of the string, patter is not found, if `j` reaches size of pattern, pattern is found at index `i`.