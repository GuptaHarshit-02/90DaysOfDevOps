# Linux Troubleshooting Runbook 🚀

## 📌 Day 05 – Linux Troubleshooting Drill: CPU, Memory, and Logs

Today’s goal was to perform a complete Linux troubleshooting drill by inspecting:
- CPU & Memory usage
- Disk & Storage health
- Network connectivity
- Service logs
- Basic incident troubleshooting workflow

This exercise helped me understand how DevOps Engineers investigate issues in real production environments.

---

# 🎯 Target Service

## Docker Service

The primary service selected for this troubleshooting drill was:
```bash
docker
```

---

# 🖥 Environment Basics

## 1️⃣ Check Kernel & System Information

### Command
```bash
uname -a
```

### Observation
Checked Linux kernel version, architecture, and system details.

---

## 2️⃣ Verify Linux Distribution

### Command
```bash
cat /etc/os-release
```

### Observation
Verified Ubuntu Linux distribution and operating system version.

---

# 📂 Filesystem Sanity Checks

## 3️⃣ Create Temporary Troubleshooting Directory

### Command
```bash
mkdir /tmp/runbook-demo
```

### Observation
Successfully created temporary troubleshooting workspace.

---

## 4️⃣ Copy and Verify File

### Command
```bash
cp /etc/hosts /tmp/runbook-demo/hosts-copy
ls -l /tmp/runbook-demo
```

### Observation
Verified file copy operation and checked permissions successfully.

---

# ⚙️ CPU & Memory Snapshot

## 5️⃣ Monitor Live Processes

### Command
```bash
top
```

### Observation
Monitored CPU and memory utilization in real time.  
No abnormal CPU spikes were observed.

---

## 6️⃣ Check Memory Usage

### Command
```bash
free -h
```

### Observation
Checked available RAM, used memory, and swap usage.  
System memory usage appeared healthy.

---

# 💾 Disk & Storage Snapshot

## 7️⃣ Check Disk Space

### Command
```bash
df -h
```

### Observation
Verified filesystem utilization and available storage space.  
No partitions were critically full.

---

## 8️⃣ Check Log Directory Size

### Command
```bash
du -sh /var/log
```

### Observation
Observed log directory size and verified logs were not consuming excessive disk space.

---

# 🌐 Network Snapshot

## 9️⃣ Check Listening Ports & Services

### Command
```bash
ss -tulpn
```

### Observation
Verified active network ports and running services including Docker and SSH.

---

## 🔟 Test Local Service Response

### Command
```bash
curl -I localhost
```

### Observation
Confirmed that the local service endpoint was responding successfully.

---

# 📜 Logs Reviewed

## 1️⃣1️⃣ Review Docker Service Logs

### Command
```bash
journalctl -u docker -n 50 --no-pager
```

### Observation
Reviewed recent Docker service logs.  
No major errors or restart failures were found.

---

## 1️⃣2️⃣ Review System Logs

### Command
```bash
tail -n 50 /var/log/syslog
```

### Observation
Checked recent system-level logs for warnings or abnormal activities.

---

# 🔍 Quick Findings

✅ System resources were healthy  
✅ Docker service was running properly  
✅ No critical disk usage issues observed  
✅ Network connectivity appeared normal  
✅ Logs did not show major failures  

---

# 🛠 Mini Troubleshooting Workflow

## Scenario
Docker containers were responding slowly.

---

## Steps Performed

### Step 1
Checked Docker service health:
```bash
systemctl status docker
```

### Step 2
Monitored system resource usage:
```bash
top
free -h
```

### Step 3
Verified disk space availability:
```bash
df -h
```

### Step 4
Inspected Docker logs:
```bash
journalctl -u docker -n 50
```

### Step 5
Tested local service connectivity:
```bash
curl -I localhost
```

---

# 🚨 If This Worsens (Next Steps)

If the issue continues or becomes worse, the next troubleshooting actions would be:

## 1️⃣ Restart Strategy
Carefully restart Docker service:
```bash
sudo systemctl restart docker
```

---

## 2️⃣ Increase Log Verbosity
Enable detailed debug logs for Docker to capture deeper troubleshooting information.

---

## 3️⃣ Advanced Investigation
Use advanced debugging tools:
```bash
strace
lsof
vmstat
```

These tools can help inspect process behavior, file usage, and system performance in detail.

---

# 💡 Key Learnings

Today I learned:
- How to collect evidence before taking action
- How to analyze CPU, memory, disk, network, and logs together
- How to build a repeatable troubleshooting workflow
- Importance of logs in production debugging

Good troubleshooting is not about randomly restarting services.  
It’s about understanding the system first and then making informed decisions.

---

# 🚀 Conclusion

This troubleshooting drill improved my confidence with:
- Linux fundamentals
- Service monitoring
- Log analysis
- Incident troubleshooting mindset

Hands-on practice is helping me become more comfortable with real-world DevOps operations every single day.

#90DaysOfDevOps  
#DevOpsKaJosh  
#TrainWithShubham  
#Linux  
#DevOps  
#Docker  
#CloudComputing  
#AWS  
#Troubleshooting  
#LinuxCommands  
#Automation  
#LearningInPublic
