# Day 07 – Linux File System Hierarchy & Scenario-Based Practice 🚀

## 📌 Objective

Today’s goal was to:
- Understand the Linux File System Hierarchy
- Learn where important files and directories are located
- Practice real-world troubleshooting scenarios step by step like a DevOps Engineer

This practice helped strengthen Linux fundamentals and troubleshooting mindset.

---

# 📂 Part 1 – Linux File System Hierarchy

---

## 1️⃣ `/` – Root Directory

### Purpose
The root directory is the starting point of the entire Linux file system.  
Everything in Linux exists under `/`.

### Command
```bash
ls -l /
```

### Example Folders Seen
```bash
bin/
etc/
home/
var/
```

### I would use this when...
I need to navigate the complete Linux file system structure.

---

## 2️⃣ `/home` – User Home Directories

### Purpose
Contains personal directories for normal users.

### Command
```bash
ls -l /home
```

### Example Folders Seen
```bash
ubuntu/
user1/
```

### I would use this when...
Accessing user files, scripts, or personal configurations.

---

## 3️⃣ `/root` – Root User Home Directory

### Purpose
Home directory for the root (administrator) user.

### Command
```bash
ls -l /root
```

### Example Files Seen
```bash
.bashrc
.ssh/
```

### I would use this when...
Working with root-level administrative tasks.

---

## 4️⃣ `/etc` – Configuration Files

### Purpose
Stores system-wide configuration files.

### Command
```bash
ls -l /etc
```

### Example Files/Folders Seen
```bash
hostname
ssh/
nginx/
```

### I would use this when...
Editing service configurations or troubleshooting application settings.

---

## 5️⃣ `/var/log` – Log Files

### Purpose
Contains system and application log files.  
Very important for troubleshooting in DevOps.

### Command
```bash
ls -l /var/log
```

### Example Files Seen
```bash
syslog
auth.log
kern.log
```

### I would use this when...
Investigating system errors or application failures.

---

## 6️⃣ `/tmp` – Temporary Files

### Purpose
Stores temporary files created by applications and users.

### Command
```bash
ls -l /tmp
```

### Example Files Seen
```bash
tempfile.txt
systemd-private-*
```

### I would use this when...
Testing scripts or storing temporary troubleshooting files.

---

## 7️⃣ `/bin` – Essential Command Binaries

### Purpose
Contains essential Linux commands required for basic system operation.

### Command
```bash
ls -l /bin
```

### Example Commands Seen
```bash
ls
cp
mv
cat
```

### I would use this when...
Running important Linux commands.

---

## 8️⃣ `/usr/bin` – User Command Binaries

### Purpose
Contains additional user-level command binaries and applications.

### Command
```bash
ls -l /usr/bin
```

### Example Commands Seen
```bash
python3
git
docker
vim
```

### I would use this when...
Using installed software and development tools.

---

## 9️⃣ `/opt` – Optional Applications

### Purpose
Used for optional or third-party software installations.

### Command
```bash
ls -l /opt
```

### Example Folders Seen
```bash
google/
custom-app/
```

### I would use this when...
Installing custom applications or third-party tools.

---

# 🛠 Hands-On Practice

## Find Largest Log Files

### Command
```bash
du -sh /var/log/* 2>/dev/null | sort -h | tail -5
```

### Observation
Identified the largest log files consuming storage.

---

## Check Hostname Configuration

### Command
```bash
cat /etc/hostname
```

### Observation
Displayed the system hostname.

---

## Check Home Directory

### Command
```bash
ls -la ~
```

### Observation
Viewed hidden files and user directory contents.

---

# 🚨 Part 2 – Scenario-Based Practice

---

# ✅ Solved Example – Check if Service is Running

## Step 1 – Check Service Status

### Command
```bash
systemctl status nginx
```

### Why?
Shows whether the service is active, stopped, or failed.

---

## Step 2 – List Available Services

### Command
```bash
systemctl list-units --type=service
```

### Why?
Displays all running services available on the system.

---

## Step 3 – Check if Service Starts on Boot

### Command
```bash
systemctl is-enabled nginx
```

### Why?
Checks whether the service automatically starts after reboot.

---

## What I Learned
Always check service status first before taking action.

---

# 🔥 Scenario 1 – Service Not Starting

### Problem
A web application service called `myapp` failed after reboot.

---

## Step 1

### Command
```bash
systemctl status myapp
```

### Why?
Checks if the service is active, failed, or stopped.

---

## Step 2

### Command
```bash
journalctl -u myapp -n 50
```

### Why?
Reads recent logs to identify service startup errors.

---

## Step 3

### Command
```bash
systemctl is-enabled myapp
```

### Why?
Checks if the service is configured to start automatically on boot.

---

## Step 4

### Command
```bash
systemctl restart myapp
```

### Why?
Attempts to restart the service after troubleshooting.

---

# ⚙️ Scenario 2 – High CPU Usage

### Problem
Application server is slow due to high CPU usage.

---

## Step 1

### Command
```bash
top
```

### Why?
Monitors live CPU and memory usage.

---

## Step 2

### Command
```bash
ps aux --sort=-%cpu | head -10
```

### Why?
Displays top CPU-consuming processes.

---

## Step 3

### Command
```bash
htop
```

### Why?
Provides interactive process monitoring.

---

## What I Learned
CPU-intensive processes can slow down the entire system.

---

# 📜 Scenario 3 – Finding Service Logs

### Problem
Developer asks for Docker service logs.

---

## Step 1

### Command
```bash
systemctl status docker
```

### Why?
Checks Docker service health first.

---

## Step 2

### Command
```bash
journalctl -u docker -n 50
```

### Why?
Displays last 50 log lines for Docker service.

---

## Step 3

### Command
```bash
journalctl -u docker -f
```

### Why?
Follows Docker logs in real time.

---

## What I Learned
systemd services store logs in journald.

---

# 🔐 Scenario 4 – File Permission Issue

### Problem
Script is showing “Permission denied”.

---

## Step 1 – Check Permissions

### Command
```bash
ls -l /home/user/backup.sh
```

### Why?
Checks current file permissions.

---

## Step 2 – Add Execute Permission

### Command
```bash
chmod +x /home/user/backup.sh
```

### Why?
Adds execute permission to the script.

---

## Step 3 – Verify Permissions

### Command
```bash
ls -l /home/user/backup.sh
```

### Why?
Confirms execute permission was added.

---

## Step 4 – Run Script

### Command
```bash
./backup.sh
```

### Why?
Verifies that the script executes successfully.

---

# 💡 Key Learnings

Today I learned:
- Linux file system hierarchy basics
- Where logs, configs, binaries, and user files are stored
- Step-by-step troubleshooting approach
- Importance of logs and permissions in Linux

Good troubleshooting is about:
✅ Understanding the problem  
✅ Checking logs carefully  
✅ Verifying resources and permissions  
✅ Taking action after investigation  

---

# 🚀 Conclusion

This practice improved my understanding of:
- Linux internals
- Troubleshooting workflows
- System services
- File permissions
- Log analysis

These are real-world DevOps skills used during production incidents and technical interviews.

#90DaysOfDevOps  
#DevOpsKaJosh  
#TrainWithShubham  
#Linux  
#DevOps  
#LinuxCommands  
#Troubleshooting  
#SystemAdministration  
#Docker  
#Automation  
#LearningInPublic
