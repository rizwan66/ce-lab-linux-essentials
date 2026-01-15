# Lab: Linux Command Line Essentials for Cloud Engineering

**Estimated Time:** 90-120 minutes  
**Difficulty:** Beginner to Intermediate  
**Prerequisites:** Basic understanding of operating systems, access to Linux terminal

## Learning Objectives

By the end of this lab, you will be able to:
- Navigate the Linux filesystem using command-line tools
- Create, move, copy, and delete files and directories
- View and search file contents using various commands
- Understand and manage file permissions
- Use piping and redirection for command composition
- Manage basic Linux processes
- Apply these skills in cloud engineering contexts

## Scenario

You've joined a cloud engineering team, and most cloud infrastructure work happens via command-line interfaces (CLI). AWS, Azure, and GCP all provide CLI tools that assume Linux/Unix proficiency. Before working with cloud resources, you need to master Linux fundamentals.

## Lab Overview

You will:
1. Connect to a Linux environment
2. Practice filesystem navigation
3. Create and manipulate files and directories
4. Work with file contents (viewing, searching, editing)
5. Understand and modify file permissions
6. Use pipes, redirects, and command chaining
7. Monitor and manage processes
8. Apply these skills to cloud-related scenarios

## Prerequisites

- Access to a Linux environment (choose one):
  - AWS EC2 instance (t2.micro Free Tier)
  - Local Linux machine
  - WSL (Windows Subsystem for Linux)
  - macOS Terminal
  - Cloud9 IDE
- SSH client (if using EC2)

---

## Part 1: Environment Setup and Navigation

### Step 1: Connect to Your Linux Environment

**If using AWS EC2:**
```bash
ssh -i your-key.pem ec2-user@your-instance-ip
```

**If using local Linux/WSL/macOS:**
- Open Terminal application

**Verify your environment:**
```bash
whoami          # Display current user
hostname        # Show system hostname
uname -a        # Show system information
pwd             # Print working directory
```

**Expected Output:**
```
[ec2-user@ip-172-31-45-67 ~]$ whoami
ec2-user

[ec2-user@ip-172-31-45-67 ~]$ pwd
/home/ec2-user
```

**📋 Record:** Output of `whoami` and `pwd` in your solution file.

### Step 2: Basic Navigation Commands

Practice moving around the filesystem.

**Commands to try:**
```bash
# List current directory contents
ls

# List with details (permissions, size, date)
ls -l

# List including hidden files
ls -la

# List in human-readable sizes
ls -lh

# Change to home directory
cd ~
pwd

# Change to root directory
cd /
pwd
ls

# Go back to previous directory
cd -

# Navigate to specific paths
cd /var/log
pwd
ls -l

# Return to home
cd ~
```

**Practice these patterns:**
```bash
# Absolute path (starts with /)
cd /home/ec2-user

# Relative path (from current location)
cd Documents

# Parent directory
cd ..

# Current directory (useful in commands)
ls ./
```

**📋 Task:** Navigate to `/var/log`, list the contents, then return to your home directory. Document the commands.

---

## Part 2: File and Directory Management

### Step 3: Creating Directories and Files

Create a project structure for a cloud application.

```bash
# Create project directory
mkdir cloud-project
cd cloud-project

# Create nested directories (use -p to create parents)
mkdir -p app/config
mkdir -p app/logs
mkdir -p app/data
mkdir -p scripts/deployment
mkdir -p scripts/monitoring

# Verify structure
tree .
# Or if tree not available:
ls -R
```

**Create files:**
```bash
# Using touch (creates empty file)
touch app/app.py
touch app/config/settings.json
touch app/config/database.conf
touch scripts/deployment/deploy.sh
touch README.md

# Create file with content using echo
echo "# Cloud Project" > README.md
echo "This is a sample cloud application." >> README.md

# Create file using cat with heredoc
cat > app/app.py << 'EOF'
#!/usr/bin/env python3
# Simple cloud application
print("Hello from the cloud!")
EOF
```

**📋 Task:** Create the full directory structure shown above and verify with `ls -R`.

### Step 4: Copying, Moving, and Deleting

Practice file operations.

```bash
# Copy file
cp app/app.py app/app-backup.py

# Copy directory recursively
cp -r app app-backup

# Move/rename file
mv app/app-backup.py app/app-old.py

# Move file to different directory
mv app/app-old.py scripts/

# Rename directory
mv app-backup app-archive

# Delete file
rm scripts/app-old.py

# Delete empty directory
rmdir app-archive/logs

# Delete directory and contents (use with caution!)
rm -r app-archive
```

**Safe deletion practices:**
```bash
# Use -i for interactive confirmation
rm -i filename

# Use -v for verbose output
rm -v filename

# Combine flags
rm -iv filename
```

**📋 Task:** 
1. Create a test directory with 3 files
2. Make a backup copy
3. Rename the backup
4. Delete only the backup
5. Document all commands

---

## Part 3: Viewing and Searching File Contents

### Step 5: Reading Files

Different ways to view file content.

**Create sample log file:**
```bash
cat > app/logs/application.log << 'EOF'
2026-01-14 08:00:01 INFO Application started
2026-01-14 08:00:05 INFO Connected to database
2026-01-14 08:00:10 DEBUG Loading configuration
2026-01-14 08:01:23 INFO User login: alice@example.com
2026-01-14 08:02:45 WARNING Database connection slow
2026-01-14 08:03:12 INFO User login: bob@example.com
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
2026-01-14 08:06:00 INFO Request completed successfully
2026-01-14 08:07:22 INFO User logout: alice@example.com
2026-01-14 08:08:45 WARNING Memory usage at 85%
2026-01-14 08:10:00 INFO Scheduled backup started
2026-01-14 08:15:30 INFO Backup completed successfully
2026-01-14 08:20:00 DEBUG Garbage collection triggered
2026-01-14 08:25:15 INFO Health check: OK
EOF
```

**View commands:**
```bash
# Display entire file
cat app/logs/application.log

# Display with line numbers
cat -n app/logs/application.log

# View large files (page by page)
less app/logs/application.log
# Press 'space' for next page, 'b' for previous, 'q' to quit

# Show first 10 lines
head app/logs/application.log

# Show first 5 lines
head -n 5 app/logs/application.log

# Show last 10 lines
tail app/logs/application.log

# Show last 5 lines
tail -n 5 app/logs/application.log

# Follow log file in real-time (useful for monitoring)
tail -f app/logs/application.log
# Press Ctrl+C to stop
```

**📋 Task:** View the last 3 lines of the log file and record the output.

### Step 6: Searching with grep

Find specific content in files.

```bash
# Search for ERROR messages
grep "ERROR" app/logs/application.log

# Case-insensitive search
grep -i "error" app/logs/application.log

# Show line numbers
grep -n "ERROR" app/logs/application.log

# Count occurrences
grep -c "INFO" app/logs/application.log

# Invert match (show lines NOT containing pattern)
grep -v "DEBUG" app/logs/application.log

# Search recursively in directory
grep -r "login" app/

# Show context (2 lines before and after)
grep -C 2 "ERROR" app/logs/application.log

# Multiple patterns with regex
grep -E "ERROR|WARNING" app/logs/application.log
```

**Practical examples:**
```bash
# Find all users who logged in
grep "User login" app/logs/application.log

# Find errors and warnings only
grep -E "ERROR|WARNING" app/logs/application.log | wc -l

# Search for specific time range
grep "08:0[5-9]" app/logs/application.log
```

**📋 Task:** 
1. Count how many ERROR messages exist
2. Find all WARNING messages with line numbers
3. Extract all user login events

---

## Part 4: File Permissions and Ownership

### Step 7: Understanding Permissions

Linux file permissions control read (r), write (w), and execute (x) access.

**View permissions:**
```bash
ls -l app/app.py
# Output: -rw-r--r-- 1 ec2-user ec2-user 89 Jan 14 08:00 app.py
#         │  │  │  │
#         │  │  │  └─ others permissions (r--)
#         │  │  └──── group permissions (r--)
#         │  └─────── owner permissions (rw-)
#         └────────── file type (- = file, d = directory)
```

**Permission values:**
```
r (read)    = 4
w (write)   = 2
x (execute) = 1

Common combinations:
7 (rwx) = 4+2+1
6 (rw-) = 4+2
5 (r-x) = 4+1
4 (r--) = 4
0 (---) = 0
```

**Modify permissions:**
```bash
# Make script executable
chmod +x scripts/deployment/deploy.sh
ls -l scripts/deployment/deploy.sh

# Set specific permissions (owner:rwx, group:rx, others:r)
chmod 754 scripts/deployment/deploy.sh

# Remove write permission for group and others
chmod go-w app/config/database.conf

# Add read permission for all
chmod a+r README.md

# Recursive permission change
chmod -R 755 scripts/
```

**Change ownership:**
```bash
# Change owner (requires sudo)
sudo chown username file

# Change owner and group
sudo chown username:groupname file

# Recursive ownership change
sudo chown -R username:groupname directory/
```

**📋 Task:**
1. Create a script file `scripts/test.sh`
2. Check its permissions
3. Make it executable for owner only
4. Verify the change

### Step 8: Practical Permission Scenarios

**Secure configuration file:**
```bash
# Create config file with sensitive data
echo "DB_PASSWORD=secret123" > app/config/database.conf

# Secure it (only owner can read/write)
chmod 600 app/config/database.conf

# Verify
ls -l app/config/database.conf
# Expected: -rw------- (600)
```

**Deployment script:**
```bash
# Create deployment script
cat > scripts/deployment/deploy.sh << 'EOF'
#!/bin/bash
echo "Deploying application..."
# Deployment logic here
EOF

# Make executable for owner, readable for group
chmod 750 scripts/deployment/deploy.sh

# Verify
ls -l scripts/deployment/deploy.sh
# Expected: -rwxr-x--- (750)
```

**📋 Task:** Create a secure backup script with appropriate permissions (only you can execute it).

---

## Part 5: Pipes, Redirects, and Command Chaining

### Step 9: Redirection Operators

Control input/output of commands.

```bash
# Redirect output to file (overwrite)
echo "Log entry" > test.log

# Append to file
echo "Another entry" >> test.log

# Redirect errors to file
ls /nonexistent 2> error.log

# Redirect both stdout and stderr
ls /nonexistent > output.log 2>&1

# Or simpler syntax
ls /nonexistent &> combined.log

# Discard output (send to /dev/null)
command > /dev/null 2>&1
```

### Step 10: Piping Commands

Chain commands together using pipes (`|`).

```bash
# Count ERROR lines
grep "ERROR" app/logs/application.log | wc -l

# Sort and find unique users
grep "User login" app/logs/application.log | cut -d':' -f4 | sort | uniq

# Show top 5 most common log levels
cat app/logs/application.log | awk '{print $3}' | sort | uniq -c | sort -rn | head -5

# Find large files in current directory
ls -lh | sort -k5 -hr | head -10

# Live monitoring with filtering
tail -f app/logs/application.log | grep --line-buffered "ERROR"
```

**Practical examples:**
```bash
# Find all .py files and count them
find . -name "*.py" | wc -l

# Get disk usage of all directories, sorted
du -sh * | sort -h

# Show processes containing "python"
ps aux | grep python | grep -v grep

# Extract and sort unique IP addresses from log
grep -oE '\b[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\b' app/logs/application.log | sort | uniq -c
```

**📋 Task:**
1. Count total lines in all `.log` files
2. Find unique log levels and count occurrences
3. List files sorted by size

---

## Part 6: Process Management

### Step 11: Viewing and Managing Processes

Monitor and control running processes.

**View processes:**
```bash
# Show all processes
ps aux

# Show processes for current user
ps u

# Show process tree
ps auxf
# Or
pstree

# Real-time process monitoring
top
# Press 'q' to quit

# Or use htop (if available)
htop
```

**Process information:**
```bash
# Find specific process
ps aux | grep python

# Or use pgrep
pgrep -a python

# Show process by PID
ps -p 1234

# Get process parent-child relationship
ps -f --ppid PPID
```

**Manage processes:**
```bash
# Run command in background
sleep 100 &

# List background jobs
jobs

# Bring job to foreground
fg %1

# Send to background (first suspend with Ctrl+Z)
# Ctrl+Z
bg %1

# Kill process by PID
kill 1234

# Force kill
kill -9 1234

# Kill by name
pkill python

# Check if process is still running
ps -p 1234
```

**📋 Task:**
1. Start a long-running command in the background
2. List all jobs
3. Kill the process

---

## Part 7: Cloud Engineering Scenarios

### Step 12: AWS CLI Log Analysis

Simulate analyzing AWS CLI output.

**Create sample AWS-style log:**
```bash
mkdir -p ~/aws-logs
cat > ~/aws-logs/cloudtrail.json << 'EOF'
{"eventTime":"2026-01-14T08:00:00Z","eventName":"CreateBucket","userIdentity":{"userName":"alice"},"resources":[{"type":"AWS::S3::Bucket","name":"my-app-bucket"}]}
{"eventTime":"2026-01-14T08:05:00Z","eventName":"PutObject","userIdentity":{"userName":"bob"},"resources":[{"type":"AWS::S3::Object","name":"data.csv"}]}
{"eventTime":"2026-01-14T08:10:00Z","eventName":"DeleteBucket","userIdentity":{"userName":"alice"},"resources":[{"type":"AWS::S3::Bucket","name":"old-bucket"}]}
{"eventTime":"2026-01-14T08:15:00Z","eventName":"RunInstances","userIdentity":{"userName":"charlie"},"resources":[{"type":"AWS::EC2::Instance","name":"i-1234567890"}]}
{"eventTime":"2026-01-14T08:20:00Z","eventName":"TerminateInstances","userIdentity":{"userName":"charlie"},"resources":[{"type":"AWS::EC2::Instance","name":"i-0987654321"}]}
EOF
```

**Analysis tasks:**
```bash
# Count events by user
grep -o '"userName":"[^"]*"' ~/aws-logs/cloudtrail.json | sort | uniq -c

# Find all S3 operations
grep "S3" ~/aws-logs/cloudtrail.json

# Extract event names
grep -o '"eventName":"[^"]*"' ~/aws-logs/cloudtrail.json | cut -d'"' -f4 | sort | uniq

# Find operations by specific user
grep '"userName":"alice"' ~/aws-logs/cloudtrail.json | grep -o '"eventName":"[^"]*"'
```

**📋 Task:** Analyze the CloudTrail log and determine:
1. How many events per user?
2. What EC2 operations occurred?
3. List all unique event types

### Step 13: System Monitoring for Cloud Resources

Monitor system resources like you would for EC2 instances.

```bash
# Check disk usage
df -h

# Check specific directory size
du -sh ~/cloud-project

# Memory usage
free -h

# CPU information
lscpu

# Check running services (systemd systems)
systemctl list-units --type=service --state=running

# Network connections
netstat -tuln
# Or
ss -tuln

# Check system load
uptime

# View system logs
sudo tail -f /var/log/syslog
# Or
sudo journalctl -f
```

**📋 Task:** Document your system's:
1. Total disk space and usage
2. Available memory
3. Number of CPU cores

---

## Verification Checklist

- [ ] Successfully connected to Linux environment
- [ ] Navigated filesystem using cd, pwd, ls
- [ ] Created directories and files
- [ ] Copied, moved, and deleted files safely
- [ ] Viewed file contents using cat, less, head, tail
- [ ] Searched files with grep
- [ ] Modified file permissions with chmod
- [ ] Used pipes and redirects effectively
- [ ] Monitored and managed processes
- [ ] Completed cloud engineering scenario tasks

---

## Cleanup

Remove practice files:
```bash
cd ~
rm -rf cloud-project
rm -rf aws-logs
```

---

## Common Commands Cheat Sheet

### Navigation
```bash
pwd          # Print working directory
cd           # Change directory
ls           # List files
ls -la       # List all with details
```

### File Operations
```bash
touch        # Create empty file
mkdir        # Create directory
cp           # Copy
mv           # Move/rename
rm           # Remove
```

### Viewing Files
```bash
cat          # Display entire file
less         # Page through file
head         # Show first lines
tail         # Show last lines
tail -f      # Follow file
```

### Searching
```bash
grep         # Search in files
find         # Find files
```

### Permissions
```bash
chmod        # Change permissions
chown        # Change ownership
```

### Process Management
```bash
ps           # Show processes
top/htop     # Monitor processes
kill         # Terminate process
jobs         # List jobs
bg/fg        # Background/foreground
```

---

## Key Takeaways

✅ **Command-line proficiency** is essential for cloud engineering  
✅ **File permissions** protect sensitive configuration and scripts  
✅ **Pipes and redirects** enable powerful command composition  
✅ **Process management** is crucial for troubleshooting  
✅ **Log analysis** skills transfer directly to cloud service logs  

---

## Next Steps

- Practice these commands daily until they become second nature
- Explore advanced tools: `awk`, `sed`, `jq` (for JSON)
- Learn shell scripting (bash) for automation
- Apply these skills when working with AWS CLI
- Study Linux system administration basics

**Congratulations!** You've built a solid foundation in Linux command-line skills! 🎉
