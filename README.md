Architecture Diagram
![image alt](https://github.com/teajo99/aws-hmrc-fraud-intelligence-platform/blob/ffa287577216672c54730955b8ae599b02b90565/aws-hmrc-fraud-intelligence-platform/Architecture%20Diagram.png)

# Cloud-Based Fraud Intelligence System (AWS EC2 + Flask + NGINX)
Overview

This project is a cloud-based fraud intelligence and monitoring system built on Amazon EC2, designed to simulate a scalable backend service for real-time risk evaluation and alerting.

The system demonstrates a 3-layer web architecture using a reverse proxy (NGINX), a Python-based API service (Flask), and a frontend dashboard, deployed in a Linux-based AWS environment.

# It focuses on core cloud engineering concepts such as:

server deployment
network routing
API design
system debugging and troubleshooting

# Architecture
System Flow

User Request → NGINX Reverse Proxy → Flask API Service → Fraud Risk Engine → JSON Response → Dashboard UI

# High-Level Design
Web traffic is handled by NGINX acting as a reverse proxy
Requests are forwarded to a Flask API running on EC2
The API processes fraud risk logic and returns structured responses
A static dashboard displays real-time results

# Cloud Infrastructure
Amazon EC2 → Application hosting (Linux server environment)
Amazon VPC → Network isolation and security boundary
Security Groups → Controlled access to HTTP (80) and API (5000) ports

# Technologies Used
AWS EC2 (Linux / Amazon Linux)
Python 3
Flask (REST API backend)
NGINX (Reverse proxy web server)
HTML / CSS (Frontend dashboard)
SSH (remote server management)

# Key Features
REST API for fraud risk evaluation
Rule-based fraud detection logic simulation
Real-time dashboard UI
Reverse proxy architecture using NGINX
Linux-based cloud deployment on AWS EC2
Manual debugging and system troubleshooting
Secure port and access configuration via security groups

# API Endpoint
Fraud Detection API
http://54.226.227.215:5000/fraud-check
Example Response
{
  "status": "FRAUD DETECTED",
  "reason": "High income anomaly",
  "riskScore": 95
}

# Deployment Architecture
Launch EC2 instance in AWS
Configure Linux environment (Python, dependencies)
Deploy Flask API on port 5000
Install and configure NGINX
Route traffic from port 80 → Flask service
Deploy frontend dashboard to NGINX web root
Configure security groups for controlled access

# System Design Decisions
Flask was used for lightweight and fast API development
NGINX was used as a reverse proxy to separate web serving and backend logic
EC2 provides full control over OS-level configuration and deployment
Port separation (80/5000) simulates real-world service isolation
Stateless API design allows future scalability improvements

# Key Skills Demonstrated
Cloud infrastructure deployment on AWS
Linux server administration and SSH management
Web server configuration (NGINX reverse proxy)
REST API development using Flask
Networking fundamentals (ports, routing, security groups)
Debugging real deployment issues in cloud environments
End-to-end application deployment workflow

# Challenges & Solutions
Configured AWS security groups to allow controlled HTTP/API access
Resolved NGINX installation and service configuration issues
Debugged Flask service binding and port exposure problems
Verified system connectivity between NGINX and backend API
Handled Linux-level service management and troubleshooting

# Screenshots
EC2 Instance Running

./screenshots/ec2-running.png

Flask API Response

./screenshots/flask-api.png

Web Dashboard UI

./screenshots/website.png

# Future Improvements
Infrastructure Enhancements
Integrate Amazon RDS for persistent fraud logs
Implement auto-scaling using EC2 Auto Scaling Groups
Add load balancing for distributed traffic handling
DevOps Improvements
CI/CD pipeline using GitHub Actions
Infrastructure as Code using Terraform
Automated deployment pipeline
Observability
CloudWatch logging and monitoring
Centralized application logging

# Summary

This project demonstrates a cloud-deployed, multi-layer web application architecture using AWS EC2, NGINX, and Flask. It highlights practical experience in deploying, configuring, and debugging real server environments while following cloud engineering best practices.
