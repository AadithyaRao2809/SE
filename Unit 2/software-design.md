### Software Design Principles

- Behavior of components and it's interaction with users
- Using appropriate algos and data structs for interfaces

### Techniques that enable design
- **Abstraction**
- **Modularity,  Cohesion and Coupling**
	degree or the extent to which the larger module can be decomposed

***Cohesion is the measure of degree of relationship between elements of a module.** **Coupling is the measure of degree of relationship between different modules**.*
###### Types of Cohesion
- **Coincidental cohesion**
    elements are grouped into modules in a haphazard way
- **Logical cohesion**
    These routines do not call one another and they do not pass information to each other. Their function is just very similar.
-  **Temporal cohesion** 
    The various elements of it are independent but they are activated at about the same point in time.
-  **Procedural cohesion**
	consists of a number of elements that have to be executed in some given order.
- **Communicational cohesion**
	elements of a module operate on the same (external) data
-  **Sequential cohesion**
    where the output of one element serves as input to the next element.
-  **Functional cohesion**
    all elements contribute to one single function of that module

###### Types of Coupling

- **Content**: One component directly impacts another.
- **Common**: Two components share data (Globals).
- **External**: Components communicate through an external medium such as a common file.
- **Control**: One component controls the other by passing control information.
- **Stamp**: Complex data structures are passed between components.
- **Data**: Only one simple data passed amongst components.

