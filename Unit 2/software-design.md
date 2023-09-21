# Software Design Principles

- Behavior of components and it's interaction with users
- Using appropriate algos and data structs for interfaces

### Techniques that enable design
#### Abstraction
#### Modularity
#### Cohesion and Coupling
degree or the extent to which the larger module can be decomposed


***Cohesion is the measure of degree of relationship between elements of a module.** **Coupling is the measure of degree of relationship between different modules**.*
##### Types of Cohesion
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

##### Types of Coupling

- **Content**: One component directly impacts another.
- **Common**: Two components share data (Globals).
- **External**: Components communicate through an external medium such as a common file.
- **Control**: One component controls the other by passing control information.
- **Stamp**: Complex data structures are passed between components.
- **Data**: Only one simple data passed amongst components.


#### Information Hiding
Need to know; each module has a secret
Done via
• Encapsulation: hides data and only allows access via specific functions
• Separation of interface and implementation: define a public interface
but separate details of how it is realized
Enables independence

##### Limiting Complexity
Ensuring minimal Complexity for better maintainability
Higher value => higher complexity => higher effort => worse design
Kinds of module complexity • Intra-modular: complexity of single module; based on size (LOC) • Inter-modular: between module
- Based on size and structure
- Eg: local flow, global flow and so on

##### Hierarchical Complexity
Views whole structure as a hierarchy

### Key Issues

#### Concurrency
parallel execution of more than one program; deadlocks/race conditions • Event handling: messages sent between objects • Distribution of components

- Distributed apps are supported by middleware
- Consider communication breakdown

#### Non functional requirement
may have system-wide impact • Error, exception handling, fault tolerance

- Mistake diverts program execution or create incorrect result/action
- Exception could lead to termination
- Ensure that Faults do not need lead to errors which lead to system

failures

- Approaches: fault avoidance, fault detection and removal
• Interaction and presentation
- React to user input effectively and efficiently
• Data persistence
- Storage of information between execution


### Differences between architecture and design
![[Pasted image 20230921204252.png]]

### Design Methods
*support in decomposing components, representing
system requirements as components*

#### Data Flow Design
 **<u>Two step process</u>**
- **Structured analysis**: logical design; data flow diagrams
- **Structured design**: transform logical design into program structure;
	structure charts

