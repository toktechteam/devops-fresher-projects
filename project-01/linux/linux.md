# Linux Fundamentals for DevOps Engineers

## Introduction
Linux is an essential skill for DevOps engineers. Mastering Linux commands helps in managing servers, automation, and troubleshooting issues in cloud environments. This guide covers essential Linux commands with practical examples, real-world use cases, and best practices.

---

## 📌 1. Checking Disk Space
✅ **Command:** `df -kh`
✅ **Use Case:** Check available and used disk space in human-readable format.
✅ **Example Output:**

```bash
Filesystem      Size  Used Avail Use% Mounted on  
/dev/xvda1      50G   20G   30G  40% /
```
✅ **Real-World Application:** Used before deploying an application to ensure enough disk space is available.

---

## 📌 2. Checking Memory Usage
✅ **Command:** `free -m`
✅ **Use Case:** Check available and used RAM in megabytes.
✅ **Example Output:**

```bash
              total        used        free      shared  buff/cache   available  
Mem:          16000        8000        4000        1000        4000       10000  
```
✅ **Real-World Application:** Helps troubleshoot performance issues in cloud servers.

---

## 📌 3. Checking CPU Usage
✅ **Command:** `top`
✅ **Use Case:** Monitor running processes and CPU/memory usage.
✅ **Example Output:**

```bash
Tasks:  125 total,   2 running,  123 sleeping,   0 stopped,   0 zombie
%Cpu(s):  10.0 us,  5.0 sy,  0.0 ni, 80.0 id,  5.0 wa,  0.0 hi,  0.0 si,  0.0 st
```
✅ **Real-World Application:** Used to identify high CPU-consuming processes.

---

## 📌 4. Checking Running Processes
✅ **Command:** `ps aux`
✅ **Use Case:** List all running processes with details.
✅ **Example Output:**

```bash
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root      1234  2.5  1.3  52340  3276 ?        S    10:00   0:05 nginx
```
✅ **Real-World Application:** Helps identify processes consuming high CPU/memory.

---

## 📌 5. Running Commands in the Background
✅ **Command:** `command &`
✅ **Use Case:** Run a command in the background.
✅ **Example:**

```bash
nohup myscript.sh &
```
✅ **Real-World Application:** Used to keep a process running even after logging out.

---

## 📌 6. Redirecting Output (stdout & stderr)
✅ **Command:** `command > output.txt 2>&1`
✅ **Use Case:** Redirect standard output and error to a file.
✅ **Example:**

```bash
ls -l > output.log 2>&1
```
✅ **Real-World Application:** Used to capture logs for debugging.

---

## 📌 7. Using `awk` for Text Processing
✅ **Command:** `awk '{print $1}' filename`
✅ **Use Case:** Extract specific columns from text files.
✅ **Example:**

```bash
awk '{print $2}' file.txt
```
✅ **Real-World Application:** Used in log analysis and data parsing.

---

## 📌 8. Using `sed` for Stream Editing
✅ **Command:** `sed 's/old/new/g' filename`
✅ **Use Case:** Replace text in files.
✅ **Example:**

```bash
sed 's/error/warning/g' logfile.txt
```
✅ **Real-World Application:** Automating text replacements in configuration files.

---

## 📌 9. Secure Copy (scp)
✅ **Command:** `scp file user@remote:/path`
✅ **Use Case:** Transfer files securely between systems.
✅ **Example:**

```bash
scp myfile.txt user@192.168.1.100:/home/user/
```
✅ **Real-World Application:** Deploying application files to remote servers.

---

## 📌 10. Cron Jobs for Scheduling Tasks
✅ **Command:** `crontab -e`
✅ **Use Case:** Schedule jobs at specific intervals.
✅ **Example Crontab Entry:**

```bash
0 2 * * * /path/to/script.sh
```
✅ **Real-World Application:** Automating backups, log rotation, and system updates.

### 📌 Cron Job Syntax Breakdown

```
* * * * * /path/to/command
│ │ │ │ │
│ │ │ │ └─── Day of the week (0-6, Sunday=0)
│ │ │ └───── Month (1-12)
│ │ └─────── Day of the month (1-31)
│ └───────── Hour (0-23)
└─────────── Minute (0-59)
```
✅ **Example Use Cases:**
- `0 0 * * * /backup.sh` → Runs backup every midnight.
- `*/5 * * * * /check_status.sh` → Runs every 5 minutes.

---

These additions ensure a comprehensive understanding of Linux commands essential for DevOps workflows.
