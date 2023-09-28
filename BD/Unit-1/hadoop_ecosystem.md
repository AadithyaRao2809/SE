## Hadoop Ecosystem
• Pig-scripting tool
• HIVE-SQL like query tool
• SQOOP-RDBMS tool
• Flume-Tool to capture weblog data
• OOZIE-Workflow Manager
• HBASE-Distributed Columnar database


### Oozie

Recommendation system needs to precompute, online too expensive

`Apache Oozie is a workflow scheduler system to manage Apache Hadoop jobs. It allows users to define, manage, schedule, and execute complex Hadoop workloads via web services. Oozie is tightly integrated with the Hadoop stack, supporting various Hadoop jobs like Hive, Pig, Sqoop, as well as system-specific jobs like Java and Shell.`

#### What is an workflow
• The sequence of steps is called a Workflow
• Workflows are common in data centers
• Users would like to
	• Specify the steps
	• Specify when the steps are to be run
	• Maybe periodically
• Run the Workflow
• What to do in case of error

Apache Oozie **schedules**, **runs** and **manages** different types of jobs in a Hadoop distributed environment.

`dependencies between the jobs`->`specified by the user` ->`Directed Acyclic Graphs`->`consumes this information and schedules these in the correct order as specified in the workflow along with a specified frequency`

It is an open Source Java Tomcat Web-Application
- It **receives requests from a client**, **triggers workflow actions** by using **Hadoop execution engine** to actually execute the task. It provides a **unique callback HTTP URL** to the task which then **notifies that URL** when it is complete.
- Oozie can also detect completion of tasks by **polling** the task for completion and then returns the result to the client.
- Oozie leverages the **existing Hadoop machinery** for **load balancing**, **fail-over**, etc


#### Oozie workflow

- Oozie workflow consists of **Action nodes** and **Control flow nodes**.
- An **action node** represents a workflow task, e.g., moving files into HDFS, running a MapReduce, Pig or Hive jobs, importing data using Sqoop or running a shell script of a program written in Java.
- A **control-flow node** controls the workflow execution between actions by allowing constructs like conditional logic wherein different branches may be followed depending on the result of earlier action node.

##### Control Node
- Start Node, designates the start of the workflow job.
- End Node, signals end of the job.
- Error Node designates the occurrence of an error and corresponding error message to be printed.
- Fork(Start parallel tasks)
- Join(Merge parallel tasks)
- Decision(switch case)

##### Action Node
When action node finishes, next task in workflow will start


At the end of execution of a workflow ,HTTP callback to update client with workflow status
Action node can trigger callback too

![](../../Attachments/hadoop_ecosystem-20230928.png)


