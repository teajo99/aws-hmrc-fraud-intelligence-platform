
# HMRC Fraud Intelligence Platform (AWS EC2 + Linux + Flask + NGINX)

## Overview

This project is a cloud-based fraud intelligence and monitoring system deployed on AWS EC2 using Linux, Flask, and NGINX.

It simulates a government-grade HMRC tax fraud detection platform that processes fraud risk data through a backend API and displays a real-time monitoring dashboard.

---

## Architecture

Browser Request
→ NGINX Web Server (Port 80)
→ Static Dashboard (HTML)
→ Flask Fraud Detection API (Port 5000)

---

## Technologies Used

- AWS EC2
- Linux (Amazon Linux)
- Python 3
- Flask
- NGINX
- HTML/CSS
- SSH

---

## Features

- Fraud detection API endpoint
- Risk scoring simulation
- Real-time styled dashboard UI
- Linux server deployment
- NGINX web hosting
- AWS EC2 cloud infrastructure
- Manual troubleshooting and debugging

---

## API Endpoint

Fraud Detection API:

http://YOUR-EC2-IP:5000/fraud-check

---

## Example Response

{
  "status": "FRAUD DETECTED",
  "reason": "High income anomaly",
  "riskScore": 95
}

---

## Deployment Steps Summary

1. Launch AWS EC2 instance
2. Connect via SSH
3. Install Python & Flask
4. Run Flask API on port 5000
5. Install and start NGINX
6. Deploy HTML dashboard to /usr/share/nginx/html
7. Open Security Group ports (80, 5000)

---

## Key Skills Demonstrated

- Cloud infrastructure (AWS EC2)
- Linux server administration
- Web server configuration (NGINX)
- Backend API development (Flask)
- Networking and security groups
- Real-world troubleshooting
- Deployment workflow understanding

---

## Challenges & Troubleshooting

- Configured AWS security group rules for HTTP and API access
- Resolved NGINX installation and service startup issues
- Debugged Flask API connectivity and port exposure
- Verified Linux service status and network routing

---

## Screenshots

### EC2 Instance Running
(./screenshots/ec2-running.png)

### Flask API Working
(./screenshots/flask-api.png)

### Website Dashboard
(./screenshots/website.png)

---

## Future Improvements

- Connect Flask API to NGINX reverse proxy
- Add DynamoDB for storing fraud logs
- Integrate AWS Lambda fraud detection engine
- Automate deployment using Terraform
- Add CI/CD pipeline using GitHub Actions
