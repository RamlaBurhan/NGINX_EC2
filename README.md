# Deploy NGINX on AWS EC2 with custom domain 

#### This project guides you through: 

1. Deploying an NGINX web server on an AWS EC2 instance. 
2. Linking it to a custom subdomain  

 

[http://nginx.ramlaburhan.com] (http://nginx.ramlaburhan.com/) 










----

#### Pre-requisites: 
- A domain name  
- AWS Account 
- An EC2 Key pair  

---- 

#### These are the following key steps to launching your site: 
 
**Step 1) Launch EC2 instance**

I.  Allocated the instance an elastic IPv4 address 
II. Check Security groups 
Allow the following for the inbound rules:  
Port 80/tcp 
Port 443/tcp 
Port 22/tcp 

