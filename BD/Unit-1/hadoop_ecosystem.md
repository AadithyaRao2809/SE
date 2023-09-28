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
