# Relational Operators
It is a representation of a database query in algebraic form.

## **Unary Operators**
### Selection ($\sigma$)
Return rows of the table that match the condition given.
Eg. $\sigma_{salary\geq 85000}(instructors)$ returns a table with the rows where instructors have a salary of above 85,000.

### Projection ($\Pi$)
Outputs the specified columns of a table
Eg. $\Pi_{id,salalry}(istructor)$ returns a table containing id and salary of all instructors.

### Rename ($\rho$)
Renames the columns of a table
Eg. $\rho_{salary\rightarrow pay}(Employee)$ changes the salary column to pay in the employee table.
$\rho_{s(b1,b2,b3..) \rightarrow r}$ changes the attributes to $b1,b2,b3 ...$
### Assignment Operator ($\leftarrow$)
Assigns the result of a relational algebra to a variable.
Eg. Physics $\leftarrow$ $\sigma_{dep\_name='physics'}(Instructor)$


## **Binary Operators**

### Cartesian Product($\times$)
Creates a new entry for every combination of the entries in the two tables.
Eg. A Student table with 20 rows and a teacher table with 10 rows will lead to student $\times$ teacher having 200 rows.

### Join ($\Join$)
Outputs the pairs of row from the two input relations. This basically combines the select and Cartesian product operation into one.

Eg. $instructor \Join_{instructor.id=teacher.id} teaches$ makes a table where it combines the instructor and teaches table for the rows where instructor id is same as the teacher id.   $r \bowtie_{\theta}s = \sigma_{\theta}(r \times s)$

### **Set Operations** 
- Union ($\cup$)
- Intersection ($\cap$)
- Set Difference ($-$)


### **Boolean Operators**
- Conjunction ($\wedge$)
- Disjunction ($\vee$)
- Negation ($\neg$)

## Aggregate functions
Functions that perform operations on a set and return a single value
- AVERAGE 
- MINIMUM
- MAXIMUM
- SUM 
- COUNT 

[SQL Commands](sql-commands.md)