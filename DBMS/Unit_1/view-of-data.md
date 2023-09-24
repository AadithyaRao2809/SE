# View of Data

-  **Data Models** - Refers to a collection of conceptual tools for describing the data, relationships, semantics and constraints
- **Data Abstraction** - Hiding complexity of data structure to represent only the data to users


## <u> Data Models </u>

### Relational Model

- Collection of Tables / Relations to show data and relationships between the data
- Multiple columns with unique names
- Record based model - Fixed format records of several types
- Tables contain records of particular type
- Each **Row** represents one piece of information
- **Columns** correspond to attributes
- Most widely used data model

![](Pasted%20image%2020230923194933.png)


### Entity - Relationship Model

- Uses entities and relationships
- **Entity** - Thing or object in the real world that is indistinguishable from other objects
- ER model is widely used in database design
![](Pasted%20image%2020230923203143.png)

### Semi - Structured Data Model

- Individual data items of the same types may have different attributes
- JSON and XML widely used
- No separation between data and schema
- Can represent information of some data sources that cannot be constrained by schema

### Object - Based Data Model

- Dominant software development methodology
- Can store objects in relational tables
- Can be seen as extending the relational model with notions of encapsulation, methods and object identity


## <u>Levels of Data Abstraction</u>

- Common man cannot understand complex data structures, need arises for hiding the complexity
- This is done through several layers of data abstraction

Three different levels of data abstraction are :-
1. Physical Level
2. Logical Level
3. View Level

### Physical Level

- Lowest level of data abstraction
- Describes how data is physically stored in computer

### Logical Level

- Higher than physical, more organized and simpler view of data
- Describes what kind of data is stored + relation between different pieces of information
- Describes entire database through relatively simple structures

### View Level

- Highest level of abstraction
- Even with logical level there is some complexity due to amount of information
- Most users don't need all this information, only need to **view a specific part of database**
- Each view differs based on needs and permissions


## <u>Data Independence </u>


### Physical Data Independence

- Refers to property of being able to modify **physical schema** without modifying **logical schema**
- Ex. Changing storage size of database will not affect the logical schema
- Alteration of indices, modifying data structures used in storage, utilizing storage devices, will not modify logical level


### Logical Data Independence

- Refers to property of being able to modify **logical schema** without affecting **external schema** or the application program.
- User view does not get affected
- Ex. Insertion or Deletion of attributes, altering table structures, entities, or relationships.


## Example of Data Abstraction

Taking the example of a University Database

**Physical Level** - How student records, course info is stored in Hard Drive or memory
**Logical Level** - Define entities like department, student, course, and their attributes
**View Level** - Faculty member has access to view showing their courses, student only has view of courses they have taken

- Without physical data independence, changing storage structure could potentially break query methods, etc, would require extensive modification in higher layers

- Without logical data independence, modifying entities and relationships would result in changes that propagate through entire application, minor changes could lead to widespread disruption


## Instances and Schema

- **Instance** - Collection of information stored in the database at a particular time
- **Schema** - Overall design of the database

- Different types of schemas exist for each level, which are
1. Physical Schema - Includes details like data storage format, file organization, indexing methods Ex. B-Trees, Hash Indexes
2. Logical Schema - Focuses on structure and relationships between the tables. **Holds most significance in impacting application programs**. 
3. Subschema - Several schemas at view level describing different views




**Next section** - [database-languages](database-languages.md)


