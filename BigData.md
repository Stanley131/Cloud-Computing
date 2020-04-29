# Guidelines
1. Hadoop/MapReduce , Spark 


## 1. Big Data System Architecture 
1. Data Processing 
    - sparking streaming , GraphX, MLBase, BlinkDB, Shark, HIVE, PIG, Spark, HADOOP...
2. Data Management
    - Tachyon, HDFS, HBASE 
3. Resource Management 
    - Mesos, Yarn
    
### 2. HDFS Architecture 
1. When an input file is added to HDFS 
    - file is split into smaller blocks of fixed size 
    - each block is replicated 
    - each replicated block is store on different host 
2. Block size is configureable. Default is 128/256MB 
3. Replication lebel is configurable, default is 3. 
    - replication is necessary for scaling and high avaliablity 
4. In case a host crashes or is removed 
    - all blocks on that host are automatically replicated to other hosts 
5. In case a host is added 
    - Blocks will be relanced so that some blocks from other hosts will be placed on the new host. 
6. master node(namenode daemon) -> data daemon
### MapReduce MR 
1. MR Framework Components 
    - JOB tracker 
            - centeral component responsible for managing job lifecycles 
            - One Job tracker per MR framework instance 
            - Accepts job submissions, queries 
            - Enqueues jobs and schedules individual tasks 
            - Communicates with task trackers to deploy and run tasks 
            - Attempts to assign tasks to support Data lcoality 
       
    - Task tracker  
            - one task tracker per host 
            - runs and manages individual tasks 
            - communicates progress of task tracker to job tracker 
2. Everything esle 
    - handles scheduling 
    - handles data distrution 
    - handles synchronization 
    - handles errors and faults 
    -
