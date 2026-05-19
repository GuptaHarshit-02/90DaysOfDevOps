# Linux Practice – Processes and Services 🚀

## 📌 Objective
Today I practiced Linux fundamentals by working with:
- Running processes
- Systemd services
- Logs and troubleshooting commands

This hands-on practice helped me understand how Linux systems are monitored and managed in real DevOps environments.

---

# ⚙️ Process Checks

## 1️⃣ Check Running Processes

### Command
```bash
ps -ef | head
```

### Sample Output
```bash
UID        PID  PPID  C STIME TTY          TIME CMD
root         1     0  0 10:00 ?        00:00:02 /sbin/init
root       523     1  0 10:01 ?        00:00:01 sshd
ubuntu    1024   998  0 10:10 pts/0    00:00:00 bash
```

### Notes
Used to display all currently running processes in the system.

---

## 2️⃣ Monitor Live Processes

### Command
```bash
top
```

### Notes
Shows real-time CPU usage, memory usage, and running processes.

---

# 🔧 Service Checks

## 3️⃣ Check Docker Service Status

### Command
```bash
systemctl status docker
```

### Sample Output
```bash
● docker.service - Docker Application Container Engine
   Loaded: loaded (/lib/systemd/system/docker.service)
   Active: active (running)
```

### Notes
Used to verify whether Docker service is running properly or not.

---

## 4️⃣ List Active Services

### Command
```bash
systemctl list-units --type=service --state=running
```

### Notes
Displays all active running services on the Linux machine.

---

# 📜 Log Checks

## 5️⃣ Check Docker Service Logs

### Command
```bash
journalctl -u docker --no-pager | tail -n 10
```

### Notes
Used to inspect recent Docker logs and troubleshoot issues.

---

## 6️⃣ View System Logs

### Command
```bash
tail -n 20 /var/log/syslog
```

### Notes
Displays the latest entries from the system log file.

---

# 🛠 Mini Troubleshooting Workflow

## Problem
Docker container was not starting properly.

---

## Step 1 – Check Docker Service

### Command
```bash
systemctl status docker
```

### Observation
Docker service was running but containers were failing.

---

## Step 2 – Verify Docker Processes

### Command
```bash
ps -ef | grep docker
```

### Observation
Verified Docker daemon processes were active.

---

## Step 3 – Inspect Docker Logs

### Command
```bash
journalctl -u docker --no-pager | tail -n 20
```

### Observation
Checked logs for warnings and startup issues.

---

## Step 4 – Restart Docker Service

### Command
```bash
sudo systemctl restart docker
```

### Result
Docker service restarted successfully and containers started working properly.

---

# 💡 Key Learnings

Today I learned:
- How to inspect running processes
- How to monitor services using systemctl
- How to troubleshoot using logs
- Basic Linux troubleshooting workflow

In real production environments, most issues can be investigated by checking:
✅ Processes  
✅ Services  
✅ Logs  

---

# 🚀 Conclusion

This practice helped me improve my Linux troubleshooting fundamentals and gain more confidence with terminal-based debugging.

Consistent hands-on practice is helping me become stronger in Linux and DevOps concepts every day.

#90DaysOfDevOps  
#DevOpsKaJosh  
#TrainWithShubham  
#Linux  
#DevOps  
#Docker  
#SystemAdministration
