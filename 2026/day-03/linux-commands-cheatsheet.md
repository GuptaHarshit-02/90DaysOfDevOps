# Linux Commands Cheat Sheet 🚀

## 📂 File System Commands

| Command | Usage |
|---------|--------|
| pwd | Show current working directory |
| ls -la | List all files with permissions |
| cd /path | Change directory |
| mkdir dirname | Create a new directory |
| rm -rf dir | Remove directory recursively |
| cp file1 file2 | Copy files |
| mv old new | Move or rename files |
| touch file.txt | Create empty file |
| find / -name file | Search files by name |
| du -sh * | Show folder sizes |
| df -h | Show disk space usage |
| chmod 755 file | Change file permissions |
| chown user:user file | Change file ownership |

---

## ⚙️ Process Management Commands

| Command | Usage |
|---------|--------|
| ps -ef | Show running processes |
| top | Live process monitoring |
| htop | Interactive process viewer |
| kill PID | Kill process by PID |
| killall nginx | Kill process by name |
| systemctl status nginx | Check service status |
| systemctl restart nginx | Restart service |
| journalctl -xe | View system logs |
| free -m | Check memory usage |
| uptime | Show system uptime/load |

---

## 🌐 Networking Troubleshooting Commands

| Command | Usage |
|---------|--------|
| ping google.com | Test network connectivity |
| ip addr | Show IP addresses |
| curl ifconfig.me | Show public IP |
| curl -I google.com | Check HTTP response headers |
| dig google.com | DNS lookup |
| netstat -tulnp | Show listening ports |
| ss -tulnp | Modern alternative to netstat |
| traceroute google.com | Trace network path |
| nslookup google.com | Query DNS records |

---

## 📜 Log & Monitoring Commands

| Command | Usage |
|---------|--------|
| tail -f /var/log/syslog | Monitor logs live |
| cat file | Display file contents |
| less file | Read large files |
| grep "error" file | Search text in files |
| dmesg | View kernel logs |

---

## 💡 Useful Tips

- Use `man <command>` to open manual pages
- Use `history` to view previous commands
- Use `Ctrl + C` to stop running commands
- Use `Tab` for auto-completion

---

# DevOps Tip 🚀
The Linux terminal is your strongest troubleshooting weapon in production environments.

Master these commands daily and you'll debug faster, automate smarter, and grow as a DevOps Engineer.

#90DaysOfDevOps #DevOpsKaJosh #TrainWithShubham
