# aws-ec2-apache-web-server
Deployed and managed an Apache Web Server on AWS EC2 using Amazon Linux, SSH, Security Groups and Linux Administration.
# 🚀 Cloud-Based Web Server Deployment Using AWS EC2 and Apache

![AWS](https://img.shields.io/badge/AWS-EC2-orange)
![Linux](https://img.shields.io/badge/Linux-Amazon%20Linux-blue)
![Apache](https://img.shields.io/badge/Apache-HTTP%20Server-red)
![SSH](https://img.shields.io/badge/SSH-Enabled-green)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 📌 Project Overview

This project demonstrates the deployment of a static website on AWS EC2 using Apache HTTP Server running on Amazon Linux 2023.

The primary objective was to gain practical experience in:

- AWS EC2 Instance Management
- Linux Administration
- SSH Connectivity
- Apache Web Server Deployment
- Security Group Configuration
- Networking Fundamentals
- Website Hosting

---

## 🏗️ Architecture

```text
Internet
    │
    ▼
AWS Security Group
(Port 22, Port 80)
    │
    ▼
EC2 Instance
(Amazon Linux 2023)
    │
    ▼
Apache HTTP Server
    │
    ▼
Static Website
```

---

## 🛠️ Technologies Used

- AWS EC2
- Amazon Linux 2023
- Apache HTTP Server (httpd)
- SSH
- Linux Commands
- Security Groups
- Networking

---

## ⚙️ Implementation Steps

### Step 1: Created EC2 Instance

- Amazon Linux 2023
- t2.micro Instance
- SSH Key Pair Authentication

### Step 2: Configured Security Group

Allowed inbound traffic:

| Protocol | Port |
|-----------|--------|
| SSH | 22 |
| HTTP | 80 |

### Step 3: Connected to EC2 using SSH

```bash
ssh -i dhanu-key.pem ec2-user@<public-ip>
```

### Step 4: Updated Linux Packages

```bash
sudo dnf update -y
```

### Step 5: Installed Apache Web Server

```bash
sudo dnf install httpd -y
```

### Step 6: Started Apache Service

```bash
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Step 7: Created and Hosted Website

Website files were deployed under:

```bash
/var/www/html
```

### Step 8: Verified Deployment

- Website accessible through browser
- Apache service running successfully
- Port 80 listening
- Access logs generated

---

# 📸 Project Screenshots

## EC2 Instance Running

![EC2 Instance](01-ec2-instance-running.png)

---

## Security Group Configuration

![Security Group](02-security-group-rules.png)

---

## SSH Login

![SSH Login](03-ssh-login-success.png)

---

## Linux Server Information

![Linux Info](04-linux-server-info.png)

---

## Apache Installation

![Apache Installation](06-apache-installation.png)

---

## Apache Service Running

![Apache Running](07-httpd-running.png)

---

## Website Files

![Website Files](08-index-html-created.png)

---

## Live Website

![Live Website](09-live-website.png)

---

## Website Verification from CLI

![Website Verification](10-website-working-cli.png)

---

## Apache Access Logs

![Access Logs](11-access-logs.png)

---

## Open Ports Verification

![Open Ports](11-open-ports.png)

---

## 🔍 Verification Commands

Check Apache Service Status:

```bash
systemctl status httpd
```

Check Listening Ports:

```bash
ss -tulnp
```

View Apache Access Logs:

```bash
sudo tail /var/log/httpd/access_log
```

---

## 🎯 Key Learnings

- AWS EC2 Deployment
- Linux System Administration
- SSH Authentication
- Apache Web Server Management
- Security Group Configuration
- Networking and Port Management
- Website Hosting
- Access Log Monitoring

---

## 🚀 Future Enhancements

- HTTPS Configuration using SSL/TLS
- Domain Integration using Route 53
- Load Balancer Configuration
- Docker Container Deployment
- CI/CD Integration

---

## 👩‍💻 Author

### Dhanu Sri R

**LinkedIn:**  
https://www.linkedin.com/in/dhanu-sri-r-846655398/

**GitHub:**  
https://github.com/Dhanu-Kotari

---
