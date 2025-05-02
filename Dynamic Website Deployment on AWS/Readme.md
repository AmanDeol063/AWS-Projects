# Dynamic Website Deployment on AWS 🚀

## 📄 Project Description
This project demonstrates how to deploy a dynamic, scalable, and secure website on AWS.  
The user accesses the application through an HTTPS endpoint managed by an Application Load Balancer.  
Traffic is routed to Tomcat servers running inside an Auto Scaling Group.  
Backend services like MySQL, RabbitMQ, and Memcached are deployed separately with private networking, managed securely via Route 53 Private DNS.

---

## ☁️ AWS Services Used
- **EC2 Instances** – Application servers and backend services
- **Elastic Load Balancer (ALB)** – Distributes traffic across servers
- **Auto Scaling Group** – Automatically manages Tomcat server scaling
- **Amazon Route 53 (Private Hosted Zone)** – DNS management for internal backend services
- **Security Groups** – Firewall rules to control traffic
- **Amazon VPC** – Custom networking environment
- **IAM** – Manage permissions securely

---


## 🛠️ Quick Setup Steps
1. Create a VPC, Subnets, and Internet Gateway.
2. Launch an Application Load Balancer and configure HTTPS listeners.
3. Deploy EC2 instances with Tomcat inside an Auto Scaling Group.
4. Launch backend EC2 instances for MySQL, RabbitMQ, and Memcached.
5. Configure Route 53 Private Hosted Zone for internal DNS resolution.
6. Set up security groups to restrict traffic between components.

---
