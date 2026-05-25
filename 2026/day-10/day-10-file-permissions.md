# Day 10 – File Permissions & File Operations Challenge 🚀

## 📌 Objective

Today’s goal was to practice Linux file operations and understand how file permissions work in real-world environments.

Tasks completed:
- Created files using `touch`, `echo`, and `vim`
- Read files using `cat`, `head`, and `tail`
- Understood Linux permission structure (`rwx`)
- Modified file permissions using `chmod`
- Tested permission-based access and execution

This hands-on challenge helped me understand how Linux controls access to files and directories.

---

# 📂 Task 1 – Create Files

## 1️⃣ Create Empty File

### Command
```bash
touch devops.txt
```

### Observation
Created an empty file named `devops.txt`.

---

## 2️⃣ Create File with Content

### Command
```bash
echo "Linux file permissions are important" > notes.txt
```

### Observation
Created `notes.txt` and added content using output redirection.

---

## 3️⃣ Create Script File

### Command
```bash
vim script.sh
```

### Content Added
```bash
echo "Hello DevOps"
```

### Observation
Created a shell script file using `vim`.

---

## Verify File Permissions

### Command
```bash
ls -l
```

### Sample Output
```bash
-rw-r--r-- 1 user user    0 devops.txt
-rw-r--r-- 1 user user   36 notes.txt
-rw-r--r-- 1 user user   19 script.sh
```

### Observation
Verified created files and their default permissions.

---

# 📖 Task 2 – Read Files

## Read notes.txt

### Command
```bash
cat notes.txt
```

### Observation
Displayed complete content of file.

---

## Open script.sh in Read-Only Mode

### Command
```bash
vim -R script.sh
```

### Observation
Opened file safely without editing.

---

## Display First 5 Lines of /etc/passwd

### Command
```bash
head -n 5 /etc/passwd
```

### Observation
Viewed first five system user entries.

---

## Display Last 5 Lines of /etc/passwd

### Command
```bash
tail -n 5 /etc/passwd
```

### Observation
Viewed last five entries of the file.

---

# 🔐 Task 3 – Understand Permissions

Linux file permissions follow this format:

```text
rwxrwxrwx
```

Where:

| Permission | Meaning | Value |
|------------|---------|-------|
| r | Read | 4 |
| w | Write | 2 |
| x | Execute | 1 |

### Command
```bash
ls -l devops.txt notes.txt script.sh
```

### Example Output
```bash
-rw-r--r-- devops.txt
-rw-r--r-- notes.txt
-rw-r--r-- script.sh
```

### Permission Understanding

#### Owner
- Read ✅
- Write ✅
- Execute ❌

#### Group
- Read ✅
- Write ❌
- Execute ❌

#### Others
- Read ✅
- Write ❌
- Execute ❌

### Observation
Files were readable by everyone but executable by no one.

---

# ⚙️ Task 4 – Modify Permissions

## Make script.sh Executable

### Command
```bash
chmod +x script.sh
./script.sh
```

### Output
```bash
Hello DevOps
```

### Observation
Added execute permission and successfully executed script.

---

## Make devops.txt Read-Only

### Command
```bash
chmod -w devops.txt
```

### Verify
```bash
ls -l devops.txt
```

### Observation
Removed write permission from file.

---

## Set notes.txt Permission to 640

### Command
```bash
chmod 640 notes.txt
```

### Verify
```bash
ls -l notes.txt
```

### Example Output
```bash
-rw-r----- notes.txt
```

### Observation
Owner can read/write, group can read, others no access.

---

## Create Directory with Permission 755

### Command
```bash
mkdir project
chmod 755 project
```

### Verify
```bash
ls -ld project
```

### Example Output
```bash
drwxr-xr-x project
```

### Observation
Owner has full access, group and others have read & execute access.

---

# 🧪 Task 5 – Test Permissions

## Try Writing to Read-Only File

### Command
```bash
echo "Testing" >> devops.txt
```

### Error
```bash
Permission denied
```

### Observation
System blocked write operation due to missing permission.

---

## Try Running File Without Execute Permission

### Command
```bash
./notes.txt
```

### Error
```bash
Permission denied
```

### Observation
Linux prevented execution because file lacked execute permission.

---

# 🛠 Commands Used

```bash
touch devops.txt

echo "Linux file permissions are important" > notes.txt

vim script.sh

ls -l

cat notes.txt

vim -R script.sh

head -n 5 /etc/passwd

tail -n 5 /etc/passwd

chmod +x script.sh

chmod -w devops.txt

chmod 640 notes.txt

mkdir project

chmod 755 project
```

---

# 💡 What I Learned

✅ How to create and read files in Linux  

✅ Understanding Linux permission structure (`rwx`)  

✅ How `chmod` controls file and directory access  

✅ Why execute permissions matter for scripts  

✅ How incorrect permissions can cause production issues  

---

# 🚀 Why This Matters for DevOps

Linux permissions are critical in DevOps because they control:

- Script execution
- Access to configs & secrets
- Shared access between applications
- Security of production systems

Even a small permission mistake can break deployments, services, or automation workflows.

---

# 🎯 Conclusion

This challenge improved my understanding of Linux file permissions and file operations.

Today I learned that troubleshooting is not always about fixing applications — sometimes it is simply about checking permissions 🔥

Small Linux fundamentals → Strong DevOps foundation 🚀

#90DaysOfDevOps  
#DevOpsKaJosh  
#TrainWithShubham  
#Linux  
#DevOps  
#LinuxCommands  
#LinuxAdministration  
#SystemAdministration  
#Automation  
#Cloud  
#Infrastructure  
#LearningInPublic
