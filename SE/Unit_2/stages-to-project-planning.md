# Stages to Project Planning

## Understanding expected Deliverables
- customer expectations
- market forces (new tech, competition)
- high level decisions (make, buy or reuse)
- Supported by Feasibility study and Requirements elicitation

## **Planning the Process**
- Choice of lifecycle - depends on degree of uncertainty (certainity->legacy)
- Models, Standards(technical, interoperability, quality, regulatory), guidelines, procedures(config, quality plan, change management)

## **Organizing Project**
- Structure - in terms of people, team, responsibilities (hierarchical, flat, functional, matrix, line org)
- Partners - downstream(marketing document, manage, support) and upstream(innovation, building and install)
- Determine deliverables - make, buy, reuse

## **Work Breakdown**
break into smaller deliverables, small enough to work with. Tree structure(tasks into phases). track milestone, checkpoint. Entry exit criteria for each. Lowest granularity is work packages
### Estimation 
Effort and time. 
Efficient control. 
Common Estimates LoC, Delphi Expirience based(expert judgment, comparative study), emperical analysis

#### CoCoMo Estimate
Categorized based on type of project
- **Organic** small team, problem well understood, team has basic experienced.
- **Embedded** Large team, complex problem statement, well experienced team
- **Semi-Detached** between organic and embedded.

Estimated with constants based on size
$Effort\ E = a(KLOC)^b$
$Time\ T=c(E)^d$
No. of people = Effort/Time

| Software Project | a   | b    | c   | d    |
| ---------------- | --- | ---- | --- | ---- |
| Organic          | 2.4 | 1.05 | 2.5 | 0.38 |
| Semi Detatched   | 3.0 | 1.12 | 2.5 | 0.35 |
| Embedded         | 3.6 | 1.20 | 2.5 | 0.32 |

Types of CoCoMo -  Basic, Intermediate, Detailed

## Scheduling and allocating Resources 
based on the WBS and Estimate 
### Calendar
plan activities 
### Activities 
- concerned individuals build schedule.
- Identification and allocation of resources)
- rework estimates- provision based on competencies

### Validate 
upstream downstream dependencies

### Organize
Concurrent - people optimization
Sequential - dependency management

### Graphic tools
Gantt chart - time estimate, calenderisation
![Pasted image 20230921120550.png](Pasted%20image%2020230921120550.png)

### Scheduling risk
Identify scheduling risk 
come up with mitigation plan

### Minimize Task Dependency
Improves concurrency. avoids delays

### Factoring Working Conditions
Holidays, leaves, working hours

### Multiple Iterations
of scheduling
due to changing requirements, schedule, people, cost.

[[risk-management|Risk Management]]


