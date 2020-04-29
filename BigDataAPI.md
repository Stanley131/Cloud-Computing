# Guidelines
1. The Big Data Problem 
2. Hardware for Big data 
3. Distributing for Big Data
4. Handling Failure and Slow Machines 
5. Map Reduce and Complex Jobs 
6. Apache Spark

### 1. The Big Data Problem and motivation 
1. Example: compute a large file score   
    - copy the data or download the data to the machine 

2. To handle large comptation  
    -  1GB/hour 
    - 100GB? 100h?
    
3. Where the rubber meets the road?
    - Concurrency is difficuly to reason about

4. Big Data Motivation 
    - Google Processes 20PB a day 
    - partition work 
    - Compute by many individual mahchines 
    - combine result 
    - As a programmer, we just need to write a program. 
    - Memory cost is getting cheap.
5. Hardware got Big Data 
    - Lots of hard drive, CPU, and a lot of memory 
### 3.  Distributing for Big Data
1. RDDs: Resilient Distributed Datasets 
    - Write programs in terms of operations on distributed datasets 
    - partitioned colllections of objects spread across a cluster, stored in memory or on disk
    - RDDs built and manipulated through a diverse set of parallel transformations 
    - RDDs automatically rebuilt on amchoen failure 
2. Spark Tools 
    - Spark SQL, Spark Streaming, MLib (Machine Learning), Graph graph <= Apache Spark
    - graph database 
3. Spark and Map Reduce Differences
    - hadoop map redeuce, Spark 
    - Storage: disk only, in-memory or on disk
    - operations: Map and Reduce, Map, Reduce, Join, Sample, etc...
    - Execution model: Batch, Batch interactive, streaming
    - Programmine enviroment: Java, Scala, Java, R, and Python
 4. History 
    - 2002 MapReduce @Google ...
. What's the point?
    - It's all about the right level of abstraction.
### 4. How it works?
 1. architecture 
    - A Spark program is two programs: a driver program and a workers program 
    - Wroker programs run on cluster nodes or in local threads 
    - RDDs are distributed across workers 
    - Driver -> Cluster Manager -> Workers 
 2. RDDs 
    - The primary abstraction in Spark 
          - Immutable once constructed 
          - Track lineage information to efficiently recompute lost data 
          - enable operations on collections of elements in parallel 
    - Construct RDDs 
          - by paralllelizing existing Python collections 
          - By transferring existing RDDs 
          - from files in HDFS ot any other storage system
3. Some Transformations 
    - map(func)
    - filter(func)
    - distinct(numTasks)
    - flatMap(func)
4. Small annoymous functions: use lambda functions 
    - example 
        - rdd = sc.parallelize([1,2,3,4])
        - rdd.map(lambda x: x *2)
        - rdd.filter(lambda x: x % 2 == 0)
        - rdd = sc.parallelize([1,2,3,4, 4])
        - rdd.distinct() ==> [1,2,3,4]
        - rdd.take()
        - rdd.collect()
        - comments = lines.filter(iScomment)
        - lines.count(),comments.count()
        - lines.cache()
 5. Spark Program lifesycycle 
    - create RDDs from externel data or parallelize'a collection in your driver program 
    - Lazily transforms them into new RDDs 
    - cache)() some RDDs for reuse 
    - Perform actions to execute parallel computation and produce results 
 6. Spark Key-value RDDs 
    - similar to Map Reduce, Spark supports key-value pairs 
    - Each element of a pair RDD is pair tuple 
     - rdd.reduceByKey()
     - rdd.sortKey()
     - rdd.groupByKey()
 
 
 
