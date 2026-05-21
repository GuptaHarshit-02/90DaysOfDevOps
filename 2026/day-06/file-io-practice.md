# Linux Fundamentals – Read and Write Text Files 🚀

## 📌 Day 06 – File I/O Practice

Today I practiced basic Linux file read/write operations using fundamental Linux commands.

The goal of this exercise was to:
- Create a file
- Write content into a file
- Append new lines
- Read file contents
- Display specific parts of the file

This practice helped me understand how Linux handles text files, which are heavily used in DevOps for logs, configs, and scripts.

---

# 📂 File Creation

## 1️⃣ Create an Empty File

### Command
```bash
touch notes.txt
```

### Observation
Created an empty text file named `notes.txt`.

---

# ✍️ Writing Text into File

## 2️⃣ Write First Line into File

### Command
```bash
echo "Linux fundamentals are important" > notes.txt
```

### Observation
Added the first line into the file using `>` redirection.  
This overwrites existing content if the file already exists.

---

## 3️⃣ Append Second Line

### Command
```bash
echo "DevOps engineers work with text files daily" >> notes.txt
```

### Observation
Appended a new line into the file using `>>` without removing previous content.

---

## 4️⃣ Append Third Line Using tee

### Command
```bash
echo "Practice makes Linux easier" | tee -a notes.txt
```

### Observation
Used `tee -a` to display output on terminal and append it into the file at the same time.

---

# 📖 Reading File Content

## 5️⃣ Read Complete File

### Command
```bash
cat notes.txt
```

### Sample Output
```bash
Linux fundamentals are important
DevOps engineers work with text files daily
Practice makes Linux easier
```

### Observation
Displayed the complete content of the file.

---

# 🔍 Reading Specific Parts of File

## 6️⃣ Read First Two Lines

### Command
```bash
head -n 2 notes.txt
```

### Sample Output
```bash
Linux fundamentals are important
DevOps engineers work with text files daily
```

### Observation
Displayed only the first 2 lines from the file.

---

## 7️⃣ Read Last Two Lines

### Command
```bash
tail -n 2 notes.txt
```

### Sample Output
```bash
DevOps engineers work with text files daily
Practice makes Linux easier
```

### Observation
Displayed only the last 2 lines from the file.

---

# 📋 Final File Content

## notes.txt

```txt
Linux fundamentals are important
DevOps engineers work with text files daily
Practice makes Linux easier
```

---

# 💡 Key Learnings

Today I learned:
- How to create files in Linux
- Difference between `>` and `>>`
- How to append text safely
- How to read complete and partial file contents
- How `tee` helps display and write simultaneously

These commands are extremely useful in:
✅ Log management  
✅ Configuration updates  
✅ Shell scripting  
✅ Automation workflows  

---

# 🚀 Conclusion

This hands-on practice improved my confidence with Linux file handling basics.

Even simple commands like `cat`, `head`, `tail`, and `tee` are powerful tools used daily in DevOps and system administration.

Small Linux fundamentals today → Strong DevOps skills tomorrow 🔥

#90DaysOfDevOps  
#DevOpsKaJosh  
#TrainWithShubham  
#Linux  
#DevOps  
#LinuxCommands  
#FileHandling  
#Automation  
#LearningInPublic
