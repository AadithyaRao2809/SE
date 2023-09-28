# Software Architecture
#### Architectural design & Characteristics
- decomposition and organization(software -> components)
- blueprint for project, includes **perspectives from all stakeholders**. 
- blueprint also allows separation of concern.
- can be used to negotiate project details(functional and quality goals).
- manifests the early design decision.
- supports reuse, helps in WBS and structures the development.
- changes in architecture are expensive in later stages of SDLC.
-  realizes use cases across scenarios.
- complex system -> **distinct, independent, manageable parts**
- **Quality Driven, recurring styles and conceptual integrity(following same style of development across all components, like nomenclature)**


### Architect
- distinct role in project
- coding standards tools and 
Makes high level design choices and tech standards. 
![[../../Attatchments/software-architecture-20230924.png]] 

### Architectural Views, Styles and Patterns
**Views** Different Perspectives of stakeholders
**Styles** how subsystems are organized.
**Pattern** Observing and including known solutions to **structuring and functioning** of subsystems

Architect >> Programmer


### Architectural Conflicts
Large Grained component - complex, large, self contained. Good performance low maintainability
Redundant data - improves availability, makes security and data integrity harder.
Localizing safety related features - better security, but involves extensive communication.

Architect has to take a choice on which is better. depends on use case.

### Design Issues
Designer takes the inputs given by the architect and decides the best of the alternatives. 
Designer resolves design issues.

#### Backlog
Contains list of all undone features. 
Context from architect, requirements from customer and constraints from sponsor
![[../../Attatchments/software-architecture-20230924-1.png]]
Ideally, components should have high cohesion low coupling

**Decompose Based on**
- layering(Network stack)
- distribution of computational resources(threads, or CPU GPU)
- Exposure - How is the component exposed and consumes other components
- Functionality - Grouping with problem domain and separate based on functions Eg: login module, customer module, so on
- Generality - Components which can be used in other places as well
- Volatility - Identify parts which may change and keep them together (UI)
- Configuration - Look at target for features needing to support different configurations

### Architectural View
View - Something that focuses on explaining one aspect of the product, while not divulging much about the other aspects
elements -> relationships
##### Module view
has code units. includes classes, functions
code based, dont represent runtime structure
useful to know what each part of the code does.


![[../../Attatchments/software-architecture-20230924-2.png]]


##### Component and Connector View
- runtime entities called components.
- Objects (not classes), a collection of objects, and a process are
- examples of components.
- While executing, components need to interact with others to support the
- system services. Connectors provide means for this interaction

##### Allocation View
- Deciding on hardware, file-system and people
- Deployment structure: software assigned to hardware and communication paths
- How software is mapped onto file structures in systems development
- Work assignment structure - Who is doing what and the knowledge needed

##### Krutchen's (4+1 View)
Previous views are interrelated. 
**Shows diffrerent to different entities.**
- Use case view: exposing requirements or scenarios
- Design view: exposes vocabulary of problem and solution space
- Process view: dynamic aspects of runtime behaviour
- Implementation view: realisation of the system; UML diagrams
- Deployment view: focus on system engineering

![[../../Attatchments/software-architecture-20230924-3.png]]
### Architectural Styles
characterized by the features that make it notable
1. Vocabulary – A set of design elements.
2. Design rules – A set of design constraints.
3. Semantic interpretation - Well-defined meaning of the connected design elements.
4. Analysis - Analysis that can be performed on systems built in that style.

### Architectural Pattern
- general, reusable solution to a commonly occurring problem in software architecture within a given context.
- characterized by the features that make it notable.
- The main difference is that a pattern can be seen as a solution to a problem, while a style is more general and does not require a problem to solve for its appearance.

![[../../Attatchments/software-architecture-20230924-4.png]]

### Importance of Styles and Patterns
- **Benefits reuse** of design and code comps, ease of understanding architecture, increased interoperability
- **Represents earliest design decisions**- Hardest to modify ,difficult to get right, comm b/w stakeholders
- **First design artifact**
- **Key to systematic reuse**


[[unit-2|Unit 2]]

