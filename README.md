# Deploy NGINX on AWS EC2 with custom domain 

### This project guides you through: 

1. Deploying an NGINX web server on an AWS EC2 instance. 
2. Linking it to a custom subdomain  

 
[http://nginx.ramlaburhan.com](http://nginx.ramlaburhan.com/) 
![image alt](https://github.com/RamlaBurhan/NGINX_EC2/blob/d71f6448c8a75650f49cbab745ce684b7ce0a347/Image1.png)

----

## Pre-requisites: 
- A domain name  
- AWS Account 
- An EC2 Key pair  

---- 

### Below are the key steps to deploy NGINX on AWS EC2 with a custom domain:
 
### Step 1) Launch EC2 instance

##### I. Allocate the EC2 instance an elastic IPv4 address
##### II. Check security groups
##### Allow the following inbound rules:
- Port 80/tcp  
- Port 443/tcp
- port 22/tco

---

### Step 2) Create a DNS record for the NGINX subdomain

##### I. Map you domain to the Elastic IPv4 address assigned to the EC2 instance
![image alt](https://github.com/RamlaBurhan/NGINX_EC2/blob/431bf3aaa907d152901d1a7e14e83a34cf611573/image3.png)

##### II. Check if it is propagated:

```Bash
nslookup nginx.ramlaburhan.com
```
![image alt](https://github.com/RamlaBurhan/NGINX_EC2/blob/625691104a371c1b73aee41eae6f6d83e69be3e0/image7.png)

---

### Step 3) Install Nginx

##### I. Update and Install

```Bash
sudo dnf update -y
sudo dnf install nginx -y
```

##### II. Check status

```Bash 
sudo systemctl status nginx 
```
![image alt](https://github.com/RamlaBurhan/NGINX_EC2/blob/470d94bd6456bc1c5125bde94c4abc30ef54f546/Picture9.png)


##### III. Enable and Start NGINX

```Bash
Sudo systemctl enable --now nginx
```
![image alt](https://github.com/RamlaBurhan/NGINX_EC2/blob/aace06fb460c82485c48fed54e8cc2c4e19cba21/Picture1.png)

---

### Step 4) Launch website
Open browser and type:

[http://nginx.ramlaburhan.com](http://nginx.ramlaburhan.com)


