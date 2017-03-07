# Assignment-8.2

1.Explain the core changes made in Hadoop 2.x. 

Ans.The core changes made in Hadoop 2.x are
a.Introduction of HDFS Federation
b.YARN for cluster resource management
c.Nodes limitation

a.HDFS Federation
HDFS is the Hadoop file system and comprises two major components: namespaces and blocks storage service. The namespace service manages operations on files and directories, such as creating and modifying files and directories. The block storage service implements data node cluster management, block operations and replication
In Hadoop 1, a single Namenode managed the entire namespace for a Hadoop cluster. With HDFS federation, multiple Namenode servers manage namespaces and this allows for horizontal scaling, performance improvements, and multiple namespaces.The implementation of HDFS federation allows existing Namenode configurations to run without changes. For Hadoop administrators, moving to HDFS federation requires formatting Namenodes, updating to use the latest Hadoop cluster software, and adding additional Namenodes to the cluster.
HDFS federation brings important measures of scalability and reliability to Hadoop. 

b.YARN(Yet another resource negotiator)
YARN is a resource manager that was created by separating the processing engine and resource management capabilities of MapReduce as it was implemented in Hadoop 1. YARN is often called the operating system of Hadoop because it is responsible for managing and monitoring workloads, maintaining a multi-tenant environment, implementing security controls, and managing high availability features of Hadoop.Job monitoring is taken care by Application master. 
YARN supports multiple processing models in addition to MapReduce. One of the most significant benefits of this is that we are no longer limited to working the often I/O intensive, high latency MapReduce framework. This advance means Hadoop users should be familiar with the pros and cons of the new processing models and understand when to apply them to particular use cases.

c.Nodes Limitation
Hadoop 1.x was suited for maximum of 4000 nodes and 40000 tasks.Hadoop 2.x can scale up to 10000 nodes and 100000 tasks. 



2.Explain the difference between MapReduce 1 and MapReduce 2 / Yarn.

Ans. In mapreduce 1 hadoop centralized all tasks to the job tracker.It allocates resources and scheduling the jobs across the cluster.In YARN,Hadoop decentralized this to ease the work load on the job tracker.Resource manager has the responsibility to allocate resources to the particular nodes and Node manager’s responsibility is to schedule jobs on the application master.YARN allows parallel execution and application master manages and execute the job.This approach can ease many job tracker problems and improves to scale up ability and optimize the job performance.YARN also allows to create multiple applications to scale up on the distributed environment.


