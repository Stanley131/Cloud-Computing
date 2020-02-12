### Understanding and leveraging On-demand Infrastructure
  - config status 
  - data status 
  - create your AMI to have a snapshot of machine 

### Example Working With on-demand Dynamic Resources 
  - vritual disk 1 and 
  - EBS: (Elastic Block Store)
  - mount VMI on on EBS 
  - Steps: 
    - create a EBS Volume 
    - Attach to EC2 instance 
    - Create a file system: mkfs -t ext3 /dev/sdh   (patition) 
    - Create a directory /ebs and mount the EBS volume: mount /dev/sdh /ebs

### Cloud Watch 
  - monitor
  
### Elastic 
  - it depends 
  - Meeting the need 
  - Vertical scaling: 
    - con: downtime could be higher 
    - 
  - Horizontal scaling: 
    - logic should be stateless 
  
  - Define Elastic metrics by monitoring 
  
### Create a elastic Infras 
  - Monitoring: to detect change for resource capacity
    - Define ALERTs so that you know when you are running out of capacity
  - Request additional resources
  - Ability to add these resources dynamically: Need some form of load balancing
  - Modify configurations so that new resources are now consumed
  - Design a simple controller code to enable most of these steps
 
### Amazon Elastic Load Balancer && Autoscale for building generic elastic infrastructure
  - 
  - 
  - 
  - 
  - 
  - 
  - 
  
