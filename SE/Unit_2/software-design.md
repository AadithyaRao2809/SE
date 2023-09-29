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
parallel execution of more than one program; deadlocks/race conditions 
- Event handling: messages sent between objects
- Distribution of component
- Distributed apps are supported by middleware
- Consider communication breakdown

#### Non functional requirement
may have system-wide impact • Error, exception handling, fault tolerance

- Mistake diverts program execution or create incorrect result/action
- Exception could lead to termination
- Ensure that Faults do not need lead to errors which lead to system

failures

- Approaches: fault avoidance, fault detection and removal
- Interaction and presentation
- React to user input effectively and efficiently
- Data persistence
- Storage of information between execution


### Differences between architecture and design
![[../../Attachments/software-design-20230929.png]]

### Design Methods
*support in decomposing components, representing
system requirements as components*

#### Data Flow Diagram
Illustrate the flow of data within a system
**<u>Two step process</u>**
- **Structured analysis**: logical design; data flow diagrams
- **Structured design**: transform logical design into program structure;
	structure charts, based on coupling and cohesion.

**4 levels**
- **lvl 0** : Highest level dfd that shows input and output to different groups of users,no internal details
- **lvl 1**: Breaks down major lvl 0 processes into sub processes and represents it separately
- **lvl 2**: Further breakdown of subprocesses
- **lvl 3**:  Most detailed, used by complex systems

##### Components of a DFD
![[../../Attachments/software-design-20230929-1.png]]

##### Minispec
process in DFDs become sufficiently straight forward and
doesn’t warrant further decompositions
##### Data dictionary entries
Logical decomposed state is precise description of structure of data
1. data dictionary called centralized metadata repository
2. A data dictionary is a collection of descriptions of the data objects or items in a data model for the benefit of programmers and others who need to refer to them

##### Structure Chart
Derived from dfd,breaks entire system to lowest func modules ,and describes them.
![[../../Attachments/software-design-20230929-2.png]]



### Design Patterns
#### Procedural patterns
- Analyze problem prior to and during construction
![[../../Attachments/software-design-20230929-3.png]]
#### Object-oriented pattern: Gang of Four solutions
- Creational patterns that focus on creation of objects (Singleton, builder)
- Structural patterns that deal with composition (Adapter, Bridge)
- Behavioural pattern that describe interaction (Command, interpreter)
- Distribution patterns that deal with the interface for distributed systems
##### Singleton pattern
- **Intent**: only **one instance of class is created**; global access point to the object
- **Motivation**: one object to coordinate actions across the system
- One class responsible to instantiate itself
- **Global point** of access to the instance
- Eg: centralized management of global resources


### Anti Patterns
- Describes situations a developer should avoid
- In agile approaches, refactoring is applied when an anti-pattern is introduced

### Contrasting structural approach vs object oriented approach



![[../../Attachments/software-design-20230929-4.png]]
![[../../Attachments/software-design-20230929-5.png]]

[[unit-2|Unit 2]]





