
# Aspects of ML

**Concept:** Representation of real or theoretical object.

**Attributes:** Properties that define a concept.

If our agent is able to observe *n* attributes, there are $2^n$ combinations of binary attributes. A concept can be defined as a combination of any of these attribute sets.
So the total number of concepts that can be distinguished is $2^{2^n}$. All concepts within this is called the concept space.

By representing a concept as a conjunction of attributes we can reduce our concept space by a significant amount.

#### Inductive Bias
Representation of concepts as conjunction of properties.
Every attribute has 4 states { $1, 0,\phi, ?$ }

Rejection Case($\phi$): Attribute doesn't make sense. Reject no matter what  
Don't Care($?$): Attribute doesn't matter. Accept no matter what.

No of concepts = $4*4*4*4 ... *4 =$         $4^n$ 
But all rejection cases are the same so we can combine them to make once concept.
So semantically it is $3*3*3* ... *3 +1 =$     **$3^n+1$** 

[[find-s|Find S]]
