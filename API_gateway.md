## API gateway
### 1. 
  - a component separates business logic with authentications
  - ===> API gateway: entry point for API 
  - Every time when users make a request should get through API gateway 
  - Security, Authentication, and authorization 
    - authentication: identify access rights, more ahout identity 
    - authoritzation: about permissions to add, edit, ...
    - security: malicious
  - API gatway is like a guard to protect everything. 

### 2.
  - separate and consolidate cross cutting concerns across microservices 
  - Authentication, authorization, SSL termination, DDoS protection 
  - **Routing** to different URLs or places  
  
### 3. 
  - static content: 
     - can be responded by API gateway becuase of no sensitive info
     - cache 
  - replacing multiple client calls wigth single AI call 
  - also some features of recerse 
  - proxy (proxy server): 
      - serving static content 
      - Caching responses 
### 4. 
  - Routing based on headers, paths and params etc. 
  - also, some features of Load Balancer component
    - loading balancing 
    - A/B testing 
    - Canary Releases: A canary release is a technique used to mitigate the risk associated with rolling out new code and functionality to everyone 
      by making the new release only available to a small group of end users.
   
    
  
