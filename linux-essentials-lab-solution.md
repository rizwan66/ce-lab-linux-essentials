# Linux Command Line Essentials - Lab Solution

**Student:** Rix  
**Date:** February 13, 2026  
**Environment:** AWS EC2 / macOS Terminal  

---

## Part 1: Environment Setup and Navigation

### Step 1: Connect to Linux Environment

**Connection Command:**
```bash
# Record your actual connection command here
ssh -i your-key.pem ec2-user@your-instance-ip
```

**📋 Verification Output:**

**`whoami` output:**
```bash
# Your output here
# Example: ec2-user
```

**`pwd` output:**
```bash
# Your output here
# Example: /home/ec2-user
```

**`hostname` output:**
```bash
# Your output here
```

**`uname -a` output:**
```bash
# Your output here
```

---

### Step 2: Basic Navigation

**📋 Task: Navigate to `/var/log`, list contents, return home**

**Commands used:**
```bash
cd /var/log
pwd
ls -l
cd ~
pwd
```

**Output of `ls -l` in /var/log:**
```bash
# Paste first 10 lines of output here
```

**Key observations:**
- Number of files in /var/log: 
- Interesting log files noticed:

---

## Part 2: File and Directory Management

### Step 3: Creating Project Structure

**📋 Task: Create full directory structure**

**Commands executed:**
```bash
mkdir cloud-project
cd cloud-project
mkdir -p app/config
mkdir -p app/logs
mkdir -p app/data
mkdir -p scripts/deployment
mkdir -p scripts/monitoring
touch app/app.py
touch app/config/settings.json
touch app/config/database.conf
touch scripts/deployment/deploy.sh
touch README.md
echo "# Cloud Project" > README.md
echo "This is a sample cloud application." >> README.md
```

**Verification with `ls -R`:**
```bash
# Paste your ls -R output here
```

---

### Step 4: File Operations Practice

**📋 Task: Create test directory, backup, rename, delete**

**Step 1: Create test directory with 3 files**
```bash
mkdir test-dir
cd test-dir
touch file1.txt file2.txt file3.txt
echo "Test content 1" > file1.txt
echo "Test content 2" > file2.txt
echo "Test content 3" > file3.txt
ls -l
```

**Step 2: Make a backup copy**
```bash
cd ..
cp -r test-dir test-dir-backup
ls -l
```

**Step 3: Rename the backup**
```bash
mv test-dir-backup test-dir-archive
ls -l
```

**Step 4: Delete only the backup**
```bash
rm -r test-dir-archive
ls -l
```

**All commands documented:**
```bash
# Complete sequence:
mkdir test-dir
cd test-dir
touch file1.txt file2.txt file3.txt
cd ..
cp -r test-dir test-dir-backup
mv test-dir-backup test-dir-archive
rm -r test-dir-archive
```

**Verification that original still exists:**
```bash
ls -l test-dir
# Output here
```

---

## Part 3: Viewing and Searching File Contents

### Step 5: Reading Files

**Created log file at:** `~/cloud-project/app/logs/application.log`

**📋 Task: View last 3 lines**

**Command:**
```bash
tail -n 3 app/logs/application.log
```

**Output:**
```bash
# Paste the last 3 lines here
```

---

### Step 6: Searching with grep

**📋 Task 1: Count ERROR messages**

**Command:**
```bash
grep -c "ERROR" app/logs/application.log
```

**Result:** `___` ERROR messages found

---

**📋 Task 2: Find WARNING messages with line numbers**

**Command:**
```bash
grep -n "WARNING" app/logs/application.log
```

**Output:**
```bash
# Paste output here
```

---

**📋 Task 3: Extract all user login events**

**Command:**
```bash
grep "User login" app/logs/application.log
```

**Output:**
```bash
# Paste output here
```

**Users who logged in:**
- alice@example.com
- bob@example.com

---

## Part 4: File Permissions and Ownership

### Step 7: Understanding Permissions

**📋 Task: Create and secure a script**

**Step 1: Create script file**
```bash
cat > scripts/test.sh << 'EOF'
#!/bin/bash
echo "This is a test script"
echo "It performs important operations"
EOF
```

**Step 2: Check initial permissions**
```bash
ls -l scripts/test.sh
```

**Initial permissions:**
```bash
# Output here (e.g., -rw-r--r--)
```

**Step 3: Make executable for owner only**
```bash
chmod 700 scripts/test.sh
# or
chmod u+x scripts/test.sh
```

**Step 4: Verify the change**
```bash
ls -l scripts/test.sh
```

**Final permissions:**
```bash
# Output here (e.g., -rwx------)
```

---

### Step 8: Practical Scenarios

**📋 Task: Create secure backup script**

**Commands:**
```bash
cat > scripts/backup.sh << 'EOF'
#!/bin/bash
# Secure backup script
echo "Starting backup..."
tar -czf backup-$(date +%Y%m%d).tar.gz ~/cloud-project
echo "Backup completed!"
EOF

chmod 700 scripts/backup.sh
ls -l scripts/backup.sh
```

**Permissions verified:**
```bash
# Output showing -rwx------
```

**Explanation:** Only the owner (you) can read, write, and execute this script. Group and others have no permissions, which is appropriate for a backup script that might handle sensitive data.

---

## Part 5: Pipes, Redirects, and Command Chaining

### Step 10: Piping Practice

**📋 Task 1: Count total lines in all .log files**

**Command:**
```bash
find . -name "*.log" -exec wc -l {} + | tail -1
# or
cat app/logs/*.log | wc -l
```

**Result:** `___` total lines

---

**📋 Task 2: Find unique log levels and count occurrences**

**Command:**
```bash
cat app/logs/application.log | awk '{print $3}' | sort | uniq -c
```

**Output:**
```bash
# Paste output here showing counts per log level
# Example:
#   4 DEBUG
#  10 INFO
#   2 ERROR
#   2 WARNING
```

---

**📋 Task 3: List files sorted by size**

**Command:**
```bash
ls -lhS ~/cloud-project
# or for recursive:
find ~/cloud-project -type f -exec ls -lh {} + | sort -k5 -hr
```

**Output (top 5 files):**
```bash
# Paste here
```

---

## Part 6: Process Management

### Step 11: Process Management

**📋 Task: Start background process, list, kill**

**Step 1: Start long-running command**
```bash
sleep 300 &
```

**Output:**
```bash
# Record the job number and PID
# Example: [1] 12345
```

---

**Step 2: List all jobs**
```bash
jobs
```

**Output:**
```bash
# Paste output here
```

---

**Step 3: Kill the process**
```bash
kill %1
# or
kill 12345  # using actual PID
```

**Verification:**
```bash
jobs
# Should show empty or terminated
```

---

## Part 7: Cloud Engineering Scenarios

### Step 12: AWS CLI Log Analysis

**Created CloudTrail log at:** `~/aws-logs/cloudtrail.json`

**📋 Task 1: Count events per user**

**Command:**
```bash
grep -o '"userName":"[^"]*"' ~/aws-logs/cloudtrail.json | sort | uniq -c
```

**Output:**
```bash
# Paste here
# Example:
#   2 "userName":"alice"
#   1 "userName":"bob"
#   2 "userName":"charlie"
```

**Summary:**
- alice: ___ events
- bob: ___ events
- charlie: ___ events

---

**📋 Task 2: What EC2 operations occurred?**

**Command:**
```bash
grep "EC2" ~/aws-logs/cloudtrail.json | grep -o '"eventName":"[^"]*"'
```

**Output:**
```bash
# Paste here
```

**EC2 Operations found:**
1. RunInstances
2. TerminateInstances

---

**📋 Task 3: List all unique event types**

**Command:**
```bash
grep -o '"eventName":"[^"]*"' ~/aws-logs/cloudtrail.json | cut -d'"' -f4 | sort | uniq
```

**Output:**
```bash
# Paste here
```

**Unique event types:**
1. CreateBucket
2. DeleteBucket
3. PutObject
4. RunInstances
5. TerminateInstances

---

### Step 13: System Monitoring

**📋 System Information**

**1. Total disk space and usage**

**Command:**
```bash
df -h
```

**Output:**
```bash
# Paste df -h output here
```

**Summary:**
- Total disk space: ___GB
- Used: ___GB
- Available: ___GB
- Usage percentage: ___%

---

**2. Available memory**

**Command:**
```bash
free -h
```

**Output:**
```bash
# Paste output here
```

**Summary:**
- Total memory: ___GB
- Used: ___GB
- Available: ___GB

---

**3. Number of CPU cores**

**Command:**
```bash
lscpu | grep "^CPU(s):"
# or
nproc
```

**Output:**
```bash
# Paste output here
```

**Number of CPU cores:** ___

---

## Verification Checklist

Mark completed items:

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

## Key Commands Learned

### Most Useful Commands
```bash
# Navigation
pwd, cd, ls -la

# File operations
touch, mkdir -p, cp -r, mv, rm -r

# Viewing
cat, less, head, tail -f

# Searching
grep -r, find

# Permissions
chmod 755, chmod u+x

# Pipes & Redirection
command | grep pattern
command > file.txt
command >> file.txt

# Process management
ps aux, top, kill, jobs, bg, fg
```

---

## Cloud Engineering Applications

**How these skills apply to AWS/Cloud work:**

1. **EC2 Instance Management**: SSH into instances and navigate logs
2. **Log Analysis**: Parse CloudWatch logs, CloudTrail events
3. **Script Deployment**: Create and manage deployment scripts
4. **Permission Management**: Secure configuration files and credentials
5. **Process Monitoring**: Monitor application processes on EC2
6. **Automation**: Chain commands for automated workflows

---

## Personal Notes & Insights

**Challenges encountered:**


**"Aha!" moments:**


**Questions for further research:**


---

## Cleanup Commands Executed

```bash
cd ~
rm -rf cloud-project
rm -rf aws-logs
rm -rf test-dir
```

**Cleanup verified:** Yes / No

---

## Lab Completion

**Completion Date:** _______________  
**Time Spent:** _______________  
**Overall Difficulty:** Easy / Medium / Hard  
**Confidence Level:** 1-10: ___  

**Next Steps:**
- Practice these commands daily
- Integrate into AWS CLI workflows
- Create personal cheat sheet
- Move on to next bootcamp module

---

**End of Lab Solution**
