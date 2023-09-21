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
![[Pasted image 20230921175650.png]] 

### Architectural Views, Styles and Patters
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
![[Pasted image 20230921183036.png]]
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
#### Module view
has code units. includes classes, functions
code based, dont represent runtime structure
useful to know what each part of the code does.


![[Pasted image 20230921184510.png]]


#### Component and Connector View
runtime entities called components.
Objects (not classes), a collection of objects, and a process are
examples of components.
While executing, components need to interact with others to support the
system services. Connectors provide means for this interaction