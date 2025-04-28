AWS Architecture Project
Overview
This project is built on AWS and allows users to connect to an application securely using HTTPS. The project uses a Load Balancer to handle incoming traffic, Tomcat servers to process the requests, and backend servers to support the application with database and messaging services.

Architecture Details
User Access:
Users send HTTPS requests from their browser or application.

Application Load Balancer (ALB):
The requests first reach an Application Load Balancer.

It is protected by a Security Group that allows HTTPS traffic (port 443).

Tomcat EC2 Instances:
The Load Balancer forwards the request to EC2 instances running Tomcat.

These instances are managed by an Auto Scaling Group for high availability and scalability.

They are placed inside another Security Group that only allows traffic:

From the Load Balancer

On port 8080

DNS Management (Route 53):
Backend service IP addresses are managed using Amazon Route 53 Private Hosted Zone, making it easy for servers to find and connect with each other inside the network.

Backend EC2 Instances:
Separate EC2 instances run backend services:

MySQL (Database)

RabbitMQ (Message Broker)

Memcached (Caching System)
These instances are placed inside their own Security Group, with controlled access based on application needs.

Security Groups
Load Balancer Security Group:

Allows HTTPS (443) from the internet.

Tomcat Servers Security Group:

Only allows incoming traffic from the Load Balancer on port 8080.

Backend Servers Security Group:

Allows necessary communication between servers only (e.g., MySQL port 3306, RabbitMQ port 5672, etc.).

Key AWS Services Used
Amazon EC2 (Virtual Servers)

Elastic Load Balancing (ALB)

Auto Scaling Group

Amazon Route 53 Private Hosted Zone

Security Groups (Firewalls)
