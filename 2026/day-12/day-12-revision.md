# Day 12 – Breather & Revision (Days 01–11) 🚀

## 📌 Goal

Today was a revision and consolidation day to reinforce everything learned from Days 01–11.

Instead of learning new topics, I revisited Linux fundamentals, troubleshooting basics, file operations, permissions, ownership, and service monitoring to strengthen retention and confidence.

---

# 🧠 Mindset & Learning Plan Review

I revisited my Day 01 learning plan and reflected on my progress.

### Current Goal

* Strengthen Linux fundamentals
* Improve troubleshooting confidence
* Build practical DevOps skills through hands-on practice
* Become more comfortable with system administration and cloud concepts

### Tweaks Made

* Spend more time revising commands instead of only learning new ones
* Practice more troubleshooting scenarios
* Improve confidence with permissions and ownership commands

---

# ⚙️ Processes & Services Revision

## Command 1 – Check Running Processes

### Command

```bash
ps -ef | head
```

### Observation

Verified running system processes and understood how Linux handles background services.

---

## Command 2 – Check Service Health

### Command

```bash
systemctl status nginx
```

### Observation

Checked whether the Nginx service was active and running properly.

---

## Command 3 – Check Service Logs

### Command

```bash
journalctl -u nginx -n 20
```

### Observation

Reviewed recent logs for the Nginx service and refreshed troubleshooting basics.

---

# 📂 File Skills Revision

## Append Content to File

### Command

```bash
echo "Linux revision practice" >> notes.txt
```

### Observation

Practiced appending content without overwriting existing data.

---

## Check File Permissions

### Command

```bash
ls -l
```

### Observation

Verified file permissions and ownership structure.

---

## Modify Permissions

### Command

```bash
chmod 755 script.sh
```

### Observation

Updated file permission and refreshed execute permission understanding.

---

## Create Directory

### Command

```bash
mkdir revision-practice
```

### Observation

Created a practice directory for revision exercises.

---

## Copy File

### Command

```bash
cp notes.txt backup-notes.txt
```

### Observation

Practiced file backup and copy operations.

---

# 🚨 Cheat Sheet Refresh – Top 5 Commands for Incidents

These are the first commands I would use during troubleshooting:

| Command                      | Why I Would Use It           |
| ---------------------------- | ---------------------------- |
| `top`                        | Monitor CPU and memory usage |
| `ps -ef`                     | Check running processes      |
| `systemctl status <service>` | Verify service health        |
| `journalctl -u <service>`    | Check service logs           |
| `df -h`                      | Verify disk space            |

### Observation

These commands now feel like my quick troubleshooting toolkit.

---

# 👥 User & Group Sanity Check

## Ownership Verification

### Command

```bash
ls -l
```

### Observation

Verified file ownership and permissions.

---

## Verify User Details

### Command

```bash
id username
```

### Observation

Checked user ID, groups, and membership information.

---

# 🧪 Mini Self-Check

## 1️⃣ Which 3 commands save you the most time right now, and why?

### `top`

Helps monitor CPU and memory usage instantly.

### `systemctl status <service>`

Quickly checks if a service is healthy or failing.

### `ls -l`

Helps verify permissions and ownership immediately.

---

## 2️⃣ How do you check if a service is healthy?

Commands I would run first:

```bash
systemctl status nginx

journalctl -u nginx -n 20

ps -ef | grep nginx
```

### Why?

These commands help verify service status, logs, and running processes.

---

## 3️⃣ How do you safely change ownership and permissions?

### Example Command

```bash
sudo chown user:group file.txt
chmod 640 file.txt
```

### Why?

Always verify access requirements before changing ownership or permissions to avoid breaking services.

---

## 4️⃣ What will you focus on improving in the next 3 days?

* Linux troubleshooting speed
* File permissions and ownership confidence
* Service debugging using logs
* More hands-on Linux command practice

---

# 💡 Key Takeaways

✅ Revision is important for retention

✅ Linux troubleshooting becomes easier with repetition

✅ Permissions and ownership are critical in system administration

✅ Service logs are essential during troubleshooting

✅ Small daily practice builds confidence over time

---

# 🚀 Conclusion

Today was a reminder that learning is not only about moving forward — it’s also about reinforcing what we already learned.

This revision helped me feel more confident with Linux basics, troubleshooting commands, permissions, and ownership.

Small revision today → Stronger DevOps foundation tomorrow 🔥

#90DaysOfDevOps
#DevOpsKaJosh
#TrainWithShubham
#Linux
#DevOps
#LinuxCommands
#LinuxAdministration
#SystemAdministration
#Automation
#Infrastructure
#LearningInPublic
