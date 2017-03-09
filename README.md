Session8
Assignment 4
1.	Explain the difference between FIFO and Capacity scheduler.
i.	Capacity scheduler:
In the Capacity Scheduler separate dedicated queue allows the small job to start as soon as it is submitted, although this is at the cost of overall cluster utilization since the queue capacity is reserved for jobs in that queue.The large job finishes later than when using the FIFO Scheduler.
ii.	FIFO Scheduler:
But in FIFO Scheduler every application should wait for its queue as the applications will start according to the order they are entered. But all the resources present will be used by the application while running.
2.	Explain the difference between FIFO and Fair scheduler.
i.	FIFO scheduler:
The FIFO Scheduler has the merit of being simple to understand and not needing any configuration, but it’s not suitable for shared clusters because large applications will use all the resources in a cluster, so each application has to wait its turn.
ii.	Fair scheduler:
In the Fair Scheduler there is no need to reserve a set amount of capacity, since it will dynamically balance resources between all running jobs.
3.	Explain the difference between Capacity and Fair scheduler.
i.	Fair Scheduler:
Fair Scheduler is a method of assigning resources to jobs such that all jobs get, on average an equal share of resources over time. When there is a single job running, that job uses the entire cluster.
ii.	Capacity Scheduler:
The Capacity Scheduler is designed to allow sharing a large cluster while giving each organization a minimum capacity guarantee. This provides elasticity for the organizations in a cost-effective manner.
4.	What are the limitations of Hadoop 1.x and how they were overcome in Hadoop 2.x.
a.	Limitations of Hadoop 1.x:
1)	Only one NameNode is possible to configure i.e. If NameNode fails entire cluster goes down, that is why NameNode is called as Single Point of Failure (SPOF).
2)	Secondary NameNode was just to take hourly backup of MetaData from NameNode.
3)	It is only suitable for Batch Processing of Huge amount of Data, which is already in Hadoop System but not for Real-time Data Processing.
4)	It supports only up to 4000 Nodes per Cluster.
5)	It has a single component: JobTracker, which is a single point of failure.
6)	It supports only one Name Node and One Namespace per Cluster. 
b.	Benefits of Hadoop 2.x over Hadoop 1.x:
1)	HDFS Federation – horizontal scalability of NameNode.
2)	NameNode High Availability – NameNode is no longer a Single Point of Failure.
3)	YARN – ability to process Terabytes and Petabytes of data available in HDFS using Non-MapReduce applications such as MPI, GIRAPH.
4)	Resource Manager – splits up the two major functionalities of overburdened JobTracker (resource management and job scheduling/monitoring) into two separate daemons: a global Resource Manager and per-application ApplicationMaster.
5)	There are additional features such as Capacity Scheduler (Enable Multi-tenancy support in Hadoop), Data Snapshot, Support for Windows, NFS access, enabling increased Hadoop adoption in the Industry to solve Big Data problems.
