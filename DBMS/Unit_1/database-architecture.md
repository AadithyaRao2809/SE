# Database Architecture

#### Centralized databases
- Single shared database
- Easy Consistency
- Limited scalability

#### Client Server
- Server executes queries on behalf of many clients.

![](../../Attatchments/database-architecture-20230924-14.png)

#### Parallel databases
- Design to run on a cluster of machines
- better scalability
- Many cores and many disks

![](../../Attatchments/database-architecture-20230924-15.png)

#### Distributed databases
- Data spread across geographically separated machines.
- Facilitates large scale data management
- Schema heterogeneity
![](../../Attatchments/database-architecture-20230924-16.png)

#### Two Tier Architecture
- Client applications directly access database

![](../../Attatchments/database-architecture-20230924-17.png)

#### Three Tier Architecture
- Client application cannot directly access the db.
- Client invokes server application which can access the db and return the data.

![](../../Attatchments/database-architecture-20230924-18.png)

