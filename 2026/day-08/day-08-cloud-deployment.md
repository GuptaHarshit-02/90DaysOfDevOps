# Day 08 – Cloud Server Setup: Docker, Nginx & Web Deployment 🚀

## 📌 Objective

Today's goal was to deploy a real web server on AWS cloud and learn practical server management.

Tasks completed:
- Launched an AWS EC2 instance
- Connected remotely using SSH
- Installed Nginx web server
- Configured Security Groups for HTTP access
- Extracted and saved Nginx logs into a file
- Verified webpage accessibility from the internet

This hands-on task helped me understand how real cloud deployments work in DevOps.

---

# ☁️ Part 1 – Launch Cloud Instance & SSH Access

## Step 1 – Launch AWS EC2 Instance

Created an Ubuntu EC2 instance on AWS Free Tier.

### Configuration Used
- Instance Type: `t2.micro`
- Operating System: `Ubuntu`
- Key Pair: `my-key.pem`
- Security Group:
  - SSH → Port 22
  - HTTP → Port 80

### Observation
Successfully launched EC2 instance and received public IP address.

---

## Step 2 – Connect via SSH

### Command
```bash
ssh -i my-key.pem ubuntu@<ec2-public-ip>
```

### Observation
Successfully connected to AWS EC2 instance through SSH.

---

# ⚙️ Part 2 – Install Docker & Nginx

## Step 1 – Update System

### Command
```bash
sudo apt update && sudo apt upgrade -y
```

### Observation
Updated all packages to the latest version.

---

## Step 2 – Install Docker

### Command
```bash
sudo apt install docker.io -y
```

### Verify Docker Status
```bash
systemctl status docker
```

### Observation
Docker service installed and running successfully.

---

## Step 3 – Install Nginx

### Command
```bash
sudo apt install nginx -y
```

### Verify Nginx Status
```bash
systemctl status nginx
```

### Observation
Nginx installed successfully and service status showed active (running).

---

# 🌐 Part 3 – Security Group Configuration

Updated AWS Security Group rules to allow web traffic.

### Inbound Rules Added

| Type | Port | Purpose |
|------|------|----------|
| SSH | 22 | Remote access |
| HTTP | 80 | Web server access |

---

## Test Web Access

Opened browser and visited:

```text
http://<ec2-public-ip>
```

### Result
Successfully viewed the **Nginx Welcome Page** in browser.

### Screenshot Captured
- `nginx-webpage.png`

---

# 📜 Part 4 – Extract Nginx Logs

## Step 1 – View Nginx Logs

### Command
```bash
cat /var/log/nginx/access.log
```

### Observation
Viewed incoming web requests and browser access logs.

---

## Step 2 – Save Logs to File

### Command
```bash
cat /var/log/nginx/access.log > nginx-logs.txt
```

### Observation
Successfully exported Nginx logs to a separate file.

---

## Step 3 – Download Logs to Local Machine

### Command
```bash
scp -i my-key.pem ubuntu@<ec2-public-ip>:~/nginx-logs.txt .
```

### Observation
Downloaded log file from AWS EC2 instance to local machine securely.

---

# 🛠 Commands Used

```bash
ssh -i my-key.pem ubuntu@<ec2-public-ip>

sudo apt update && sudo apt upgrade -y

sudo apt install docker.io -y

systemctl status docker

sudo apt install nginx -y

systemctl status nginx

cat /var/log/nginx/access.log

cat /var/log/nginx/access.log > nginx-logs.txt

scp -i my-key.pem ubuntu@<ec2-public-ip>:~/nginx-logs.txt .
```

---

# 🚨 Challenges Faced

## Problem
Nginx webpage was not accessible from browser.

### Root Cause
HTTP port (80) was not enabled in AWS Security Group.

### Solution
Added inbound HTTP rule:

```text
Port 80 → Allow Anywhere (0.0.0.0/0)
```

After updating Security Group settings, the webpage started working successfully.

---

# 💡 What I Learned

✅ How to launch an AWS EC2 instance  
✅ How to connect to cloud servers using SSH  
✅ How to install and manage Docker & Nginx  
✅ AWS Security Group configuration basics  
✅ How to access and extract Nginx logs  
✅ Basic troubleshooting for inaccessible web services  

---

# 🚀 Why This Matters for DevOps

This exercise taught me:

- Cloud infrastructure provisioning
- Remote server management through SSH
- Service deployment and management
- Security Group & firewall basics
- Log management and troubleshooting

These are essential real-world DevOps skills used in production environments.

---

# 📸 Screenshots Added

- `ssh-connection.png`
- `nginx-webpage.png`
- `docker-nginx.png`

---

# 📁 Files Added

- `day-08-cloud-deployment.md`
- `nginx-logs.txt`

---

# 🎯 Conclusion

This was my first practical cloud deployment exercise where I launched an AWS EC2 instance, connected remotely, installed services, configured access rules, and verified a live webpage.

This task helped me better understand how real-world infrastructure works in DevOps and cloud environments.

Small consistent learning → Real DevOps skills 🚀

#90DaysOfDevOps  
#DevOpsKaJosh  
#TrainWithShubham  
#AWS  
#EC2  
#CloudComputing  
#Linux  
#DevOps  
#Docker  
#Nginx  
#SSH  
#Automation  
#LearningInPublic
