### Abstract 
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
