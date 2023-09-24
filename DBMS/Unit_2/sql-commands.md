# SQL Commands

### Datatypes in SQL

**Numeric Datatypes**
`INT` or `INTERGER` standard size int
`SMALLINT` machine dependent subset of int

**Character String Types**
`CHAR(n)` fixed length str
`VARCHAR(n)` variable length with limit n


**Bit String Datatype**
`BIT(n)` Fixed length
`BIT VARYING(n)` variable length

**Date data type**
`DATE` - format YYYY-MM-DD
`DATETIME` - format: YYYY-MM-DD HH:MI:SS
`TIMESTAMP` - format: YYYY-MM-DD HH:MI:SS (Optional `WITH TIME ZONE` qualifier)
`YEAR` - format YYYY or YY

**Large Object Types**
When there is a need to include large objects like documents or other file types such as videos and photos, we use LOBs.

`CLOB` Character LOBs used to store large amount of character data, i.e. plain text files.
`BLOB` Used to store any kind of file in binary format. Like images, audio, video.

### Data Definition Commands

`CREATE` creates objects in the DB
`ALTER` modifies the structure of the DB
`DROP` deletes a part of the structure from the DB
`TRUNCATE` removes rows from the DB and the space allocated to it.

### Specifying Constraints in SQL
`PRIMARY KEY`  specifies an attribute to be a primary key
`UNIQUE` specifies an attribute to not have any duplicate values. Also known as creating secondary or candidate keys.
`FOREIGN KEY` specifies a key as being a foreign key, followed by `REFERENCES` to indicate which table the foreign key is referencing.
`DEFAULT` used to specify a default value to an attribute.
`NOT NULL` Specifies that the attribute is not nullable.
`CHECK` used to provide a constraint on the value in the form of a condition.
`ON DELETE` and `ON UPDATE` are steps to be taken when a delete or update is performed.
`CASCADE` propagate the action from parent table to child.

View Commands are used to create a virtual table. We select a part of our DB table to be  the view
`CRETE VIEW <view_name> AS <query>` where `<query>` is any valid SQL query.:

[dml-commands](dml-commands.md)