# Purpose of Database

## Problem - Solution of File Processing Systems

| FPS Problem                                                                 | DBMS Solution                                                                                          |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Data Redundancy & Inconsistency                                             | Information stored in centralized location, and changes can be made at a single spot                   |
| Difficulty in accessing Data                                                | Central Information store, fast searching and filtering through querying                               |
| Data Isolation ( Data scattered across different files in various formats ) | Centralized system, uniform and standardized way to access data through querying                       |
| Integrity Problems  (Constraints)                                           | Can enforce rules in schema by specifying integrity constraints                                        |
| Atomicity Problems ( Can have many steps in a transaction )                 | Ensures Transactions are treated as one indivisible unit of work, automatic rollback incase of failure |
| Concurrent Access Anomalies                                                 | Transaction for atomicity, Locking to prevent conflicting changes                                      |
| Security  (Unauthorized access)                                             | Admin can define access controls and permissions.                                                      |

## Characteristics of Database Systems

- **Self Describing** - Database system not only contains DB but also metadata ( DB structure and constraints)
- **Insulation** - Insulation between programs and data, structure of data files stored separately from access programs
- **Multiple Views** - Supports multiple views of data. View is subset of data that could be derived
- **Sharing of Data** - Allows multiple access in controlled manner so result of changes are correct

## Advantages of Database Systems

- No redundancy
- Sharing of data
- Restricting unauthorized access
- Persistent storage for program objects
- Storage structures and search techniques for query processing
- Backup and Recovery
- Multiple interfaces for different classes of users
- Representing complex relationships between data
- Integrity Constraints are enforced
- Potential for enforcing standards
- Reduced application development time
- Flexibility to change data structures
- Availability of current information

**Next section** - [View of Data](view-of-data.md)