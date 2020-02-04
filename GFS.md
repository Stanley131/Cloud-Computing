### 1. Abstract 
  - a scalable distributed file system for large distributed data-intensive applications. 
  - Component failures are norm, containing hundreds and thounsands of machines built from 
    inexpensive commodidity.  
  - The quality and quatity of the components virtually guarantee that some are not functional 
  - constant monitoering, error detection, fault tolenrence, and automatic recovery must be intergral
    to the system. 
  - I/O operation and block sizes have to be revisited. 
  - Third, most files are mutated. 
  - Fourth, co-designing the applications and the file system API benefits the overall system by increasing 
    our flexibility. 
     - example: atomic appending operation so that multiple clients can append concurrently to a file. 
     - GFS clusters are currently deployed for different purposes.
     - A storage node is a machine that is connected to a Backup server and one or more devices used in
        Backup's backup, archive, and HSM operations.
### 2. Assumptions 
  - high substained bandwith is more important than low latency 
  - not standard POSIX 
  - GFS has snapshot and record append operations. record append allows multiple clients to append data to 
    the same files to be invaluable in building large distributed applications. 
  - GFS cluster = master + mutiple chunkservers 
  - Chunkservers store chunk on local disks as Linux files and read or write chunk data on local disks
    as linux files 
  - 3 replicas 
  - Master: control meta data, access control information 
  - Single master: simplifies design 
  - Chunk Size: 64MB, 
  - Lazy space allocation avoids wasting space due to internal fragmentation. 
  - master metadata: chunk namespace, mapping from files to chunks, the location of all replicas 
  - This periodic scanning is used to implement chunk garbage collection, replication in the 
    presence of chunkserver, chunk migration. 
  - Operation log: central to OS to keep concurrency, log is small, checkpoint 
  - read/write/
  - data integrity 
  
  
