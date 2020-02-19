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
### ELB set up using Command line tool
  - elb-create-lb production 
    -- availability-zones us-east-lb 
    -- listener "prodctioHTTP, lb-port=80, instance-port=80"
  - elb-configure-healthcheck production \
    -- taget "HTTP:80"
    -- intervval 30 
    -- timeout 2 
    -- healthy--threshold 6 
    -- unhealthy-threshold 2 
  - elb-register-instances-with-lb production \
    -- instances i-23223
  - Note: a good system design should be simple 
### What is misssing ?  AutoScale
  - four keys:  
    - authoscale groups - holds instance  (a container)
      - a group can have multiple instances 
    - Launch configurations - that determins which instance is launched 
    - Alarms - that determines when instance is launched 
      - Certain resources or conditions to determine this (example CPU utilization <70%)
      - Clock Watch watches this 
    - policy: specify that instances will be launched or terminated
      - When alarms ocur => add or reduce instances (Launch configurations)
    
### Policies 
  - scale up or scale down
  - evalution pierod: take multiple periods and find average 
  - 
  
  
  
  
  
  
  
  
  
