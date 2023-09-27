	# Finite State Automata
Finite State Automata (FSA) used as to make string matching efficient. Building the FSA is a part of the preprocessing.  

The idea is to build an FSA where
- every state is a character in the pattern
- each character send the automaton to a new state.
- If the characters in the pattern match, it goes into an accepting state.
- Else, the FA will return to a suitable state, such that the returned state gives us maximum advantage.
Time to build FA is large if $|\Sigma|$ is large
matching time O(n)

FSA for `ababaca`
![](../../Attachments/finite-state-automata-20230927-2.png)

[[knuth-morris-pratt|Knuth Morris Pratt]]