# Lab Solution: Linux Command Line Essentials

**Student Name:** ___________________________  
**Date:** ___________________________  
**Environment Used:** ☐ EC2 ☐ Local Linux ☐ WSL ☐ macOS ☐ Cloud9

---

## Part 1: Environment Setup

### Connection Information

**Command used to connect:**
```bash
_____________________________________________________________
```

**Output of `whoami`:**
```
_____________________________________________________________
```

**Output of `pwd`:**
```
_____________________________________________________________
```

**Output of `uname -a`:**
```
_____________________________________________________________
```

---

## Part 2: Navigation Practice

### Task: Navigate to /var/log and back

**Commands executed:**
```bash
# Navigate to /var/log


# List contents


# Return to home directory

```

**Screenshot 1: /var/log directory listing**
![var/log contents](screenshots/01-var-log.png)

---

## Part 3: Directory Structure Creation

### Project Structure

**Commands to create directory structure:**
```bash
# Create cloud-project directory


# Create nested directories







# Create files






```

**Screenshot 2: Project structure (tree or ls -R output)**
![Project structure](screenshots/02-project-structure.png)

---

## Part 4: File Operations

### Copy, Move, Delete Practice

**Commands for test directory task:**
```bash
# Create test directory with files


# Make backup copy


# Rename backup


# Delete backup


# Verify final state

```

**Screenshot 3: File operations results**
![File operations](screenshots/03-file-operations.png)

---

## Part 5: Viewing File Contents

### Log File Analysis

**Output of last 3 lines:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**Command used:**
```bash
_____________________________________________________________
```

---

## Part 6: Searching with grep

### Task: Search log file

**1. Count ERROR messages:**
```bash
# Command:

# Output:
_____________________________________________________________
```

**2. Find WARNING messages with line numbers:**
```bash
# Command:

# Output:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**3. Extract user login events:**
```bash
# Command:

# Output:
_____________________________________________________________
_____________________________________________________________
```

**Screenshot 4: grep search results**
![grep results](screenshots/04-grep-results.png)

---

## Part 7: File Permissions

### Task: Create and secure script

**Commands executed:**
```bash
# Create test script


# Check initial permissions


# Make executable for owner only


# Verify permissions

```

**Initial permissions:** ___________________________

**Final permissions:** ___________________________

**Screenshot 5: Permission changes**
![Permissions](screenshots/05-permissions.png)

### Secure Backup Script

**Script content:**
```bash
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**Permissions set:**
```bash
# Command:

# Result (ls -l):
_____________________________________________________________
```

---

## Part 8: Pipes and Redirects

### Task: Command chaining

**1. Count total lines in all .log files:**
```bash
# Command:

# Result:
_____________________________________________________________
```

**2. Find unique log levels and count:**
```bash
# Command:

# Result:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**3. List files sorted by size:**
```bash
# Command:

# Result:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**Screenshot 6: Pipes and redirects output**
![Pipes output](screenshots/06-pipes-redirects.png)

---

## Part 9: Process Management

### Task: Background process

**1. Start long-running command in background:**
```bash
# Command:

# Output (job number):
_____________________________________________________________
```

**2. List all jobs:**
```bash
# Command:

# Output:
_____________________________________________________________
```

**3. Kill the process:**
```bash
# Command:

# Verification:
_____________________________________________________________
```

**Screenshot 7: Process management**
![Processes](screenshots/07-processes.png)

---

## Part 10: Cloud Engineering Scenarios

### CloudTrail Log Analysis

**1. Events per user:**
```bash
# Command:

# Result:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**2. EC2 operations:**
```bash
# Command:

# Result:
_____________________________________________________________
_____________________________________________________________
```

**3. Unique event types:**
```bash
# Command:

# Result:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**Screenshot 8: CloudTrail analysis**
![CloudTrail](screenshots/08-cloudtrail-analysis.png)

### System Monitoring

**1. Disk space:**
```bash
# Command: df -h

# Total space: _______________ 
# Used: _______________
# Available: _______________
# Usage %: _______________%
```

**2. Available memory:**
```bash
# Command: free -h

# Total: _______________
# Used: _______________
# Free: _______________
```

**3. CPU cores:**
```bash
# Command: lscpu

# CPU(s): _______________
# Model: _______________
```

**Screenshot 9: System resources**
![System resources](screenshots/09-system-resources.png)

---

## Command Cheat Sheet (Your Most Used)

**List your 10 most-used commands from this lab:**

1. _______________________________________________
2. _______________________________________________
3. _______________________________________________
4. _______________________________________________
5. _______________________________________________
6. _______________________________________________
7. _______________________________________________
8. _______________________________________________
9. _______________________________________________
10. _______________________________________________

---

## Reflection Questions

### 1. How do file permissions enhance security in cloud environments?

**Your answer:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

### 2. Why is piping commands together more efficient than intermediate files?

**Your answer:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

### 3. Describe a real-world scenario where you'd use `tail -f`.

**Your answer:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

### 4. What's the difference between killing with `kill` vs `kill -9`?

**Your answer:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

### 5. How does Linux CLI proficiency help with AWS CLI usage?

**Your answer:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

---

## Troubleshooting Log

**Did you encounter any issues?** (Yes/No): ______

**If yes, document:**

| Issue | Commands Tried | Solution | Time Spent |
|-------|---------------|----------|------------|
|       |               |          |            |
|       |               |          |            |
|       |               |          |            |

---

## Cleanup Confirmation

- [ ] Removed ~/cloud-project directory
- [ ] Removed ~/aws-logs directory
- [ ] Verified no leftover files

**Cleanup commands:**
```bash
_____________________________________________________________
_____________________________________________________________
```

---

## Self-Assessment

**Rate your confidence (1-5, where 5 is expert):**

| Skill | Before Lab | After Lab | Notes |
|-------|-----------|-----------|-------|
| Filesystem navigation | ___/5 | ___/5 | |
| File manipulation | ___/5 | ___/5 | |
| Viewing/searching files | ___/5 | ___/5 | |
| File permissions | ___/5 | ___/5 | |
| Pipes and redirects | ___/5 | ___/5 | |
| Process management | ___/5 | ___/5 | |
| Log analysis | ___/5 | ___/5 | |

---

## Bonus Challenges Completed

- [ ] Explored `awk` for text processing
- [ ] Created a shell script with multiple commands
- [ ] Used `find` with complex criteria
- [ ] Practiced `sed` for text replacement
- [ ] Set up custom bash aliases

**Bonus notes:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

---

## Instructor Verification

**Instructor Name:** ___________________________

**Date Reviewed:** ___________________________

**All tasks completed:** ☐ Yes ☐ No

**Comments:**
```
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________
```

**Grade/Status:** ___________________________

---

**Lab Status:** ☐ Complete ☐ Needs Revision

**Total Time Spent:** ________ minutes

**Submission Date:** ___________________________
