- NLX Inc, 
- CEO, Co-Founder 
- Andrei, Papa.. 

### Deal with large scale applications 
	- small number => big number 
		- scale out 
		- NLP consume too much memory 
### Challeneges with monolithic Systems 
	- Code Complexity and maintanilty 
	- deployment becomes the bottleneck 
	- Fear to change
	- lack of ownership 
	- failure dependencies 
	
### Microserverice to the rescue 
	- small, simple protocol, loosely-coupled, 
	- speed, innnovation,  quality 
	
### Serverless Components 
	- No servers to manage
	- Scability out of the box 
	- minimize codebase size 
	- pay per usage 
	- extremely low cost 
	- ** aws: Lamda, API Gateway, Congito, IAM**
### API design 
	- think before build 
	- drive a good chunk of the architecture 
	- data structure design 
	- make everthing more efficient 
	- Note: documentation is time consuming 
	- NOTE: **Swagger**
### Swagger 
	- standardized, open source, panda friendly
	- can generate different code 

### API Gateway + API Gateway + Lambda 
	- Front-end documentation, awesome
	- The most important role the API gateway plays is ensuring reliable processing of every API call.
	- IAM (identity access management)
	- Step Functions
	- build a library as along 
	- layers: 
	
### IAM 
	- Always use "roles", not access keys in our command line 
	
### API gateway bonus: SDH Generation 
	- cognito exchanges your session to temp IAM with limited access 
	
### Scaling the Frontend 
	- Host your website on S3 
	- cheap 
	- durability 
	- front-end data driven 
### Checkout 
	- Asynchronous checkout 
	- SQS: Amazon Simple Queue Service
	- SNS: Amazon Simple Notification Service (SNS)
	- SES: Amazon Simple Email Service (SES)

### LF2 
	- Alexa is online, baby. 
	

	
	
