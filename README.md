## AWS-Capstone-Project-1

This project demonstrates how to deploy a **highly available, auto-scaling PHP web application** using Amazon Web Services (AWS). It follows a **multi-tier architecture**, separating the web and database layers for better performance, security, and scalability.

## 🚀 Architecture Overview

**Services Used:**

- **Amazon EC2** – Hosts the PHP website
- **Amazon RDS (MySQL)** – Managed MySQL database in private subnet
- **Elastic Load Balancer (ALB)** – Distributes incoming traffic
- **Auto Scaling Group** – Automatically adjusts number of EC2 instances
- **Amazon VPC** – Custom Virtual Private Cloud with public and private subnets
- **Security Groups ** – Secure and control access to AWS resources

 **Key Features:**

- ✅ Multi-tier separation (Web & DB layers)
- ✅ High Availability across multiple Availability Zones
- ✅ Auto Scaling based on load
- ✅ Secure network design using VPC, subnets, and security groups
- ✅ Load balancing via ALB
- ✅ PHP application running on Apache/Nginx

## 🧱 Architecture Diagram

<img width="771" height="621" alt="image" src="https://github.com/user-attachments/assets/fea7ad84-dfb9-43d7-a3a8-9f95b5407f5d" />


## 🔧 Setup & Deployment Steps

### 1. **VPC & Networking Setup**
- Create a custom VPC
- Add public and private subnets across at least two Availability Zones
- Set up route tables and an Internet Gateway
- Add a NAT Gateway for instances in private subnet

### 2. **Launch EC2 Instances (PHP Web Server)**
- Use Amazon Linux or Ubuntu
- Install Apache/Nginx, PHP, and Git
- Create Index.php file in /var/www/html & paste the website code there.
- Ensure security groups allow HTTP (80) and SSH (22) only from your IP

### 3. **Configure Load Balancer**
- Create an Application Load Balancer (ALB)
- Register EC2 instances or Auto Scaling Group as target
- Set listener rules for HTTP traffic

### 4. **Set Up Auto Scaling Group**
- Define Launch Template
- Set minimum, maximum, and desired capacity
- Add scaling policies (CPU/Network utilization, etc.)

### 5. **Provision RDS (MySQL)**
- Launch a MySQL RDS instance in a private subnet
- Set security group to allow access from EC2 instances only

## 🛡️ Security Considerations

- EC2 instances are in public subnet, RDS in private subnet
- Security Groups are restricted to necessary ports/IPs
- SSH access is limited to your IP
- Database access is limited to web server subnet

## Output

<img width="1354" height="603" alt="image" src="https://github.com/user-attachments/assets/699b15a5-1c11-4817-bc40-e9ee2cefd1a2" />



<img width="1350" height="479" alt="image" src="https://github.com/user-attachments/assets/1abb5aa4-202f-452f-86b0-51407be8fab6" />







  
