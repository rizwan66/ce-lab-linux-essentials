# Linux Command Line Essentials - Lab Solution

**Student:** Rizwan 
**Date:** February 13, 2026  
**Environment:** AWS EC2 / macOS Terminal  

---
complete:13: command not found: compdef
R$ conda activate my_project
(my_project) R$ ssh -i ~/.ssh/bootcamp-week2-key.pem ec2-user@44.200.163.251
ssh: connect to host 44.200.163.251 port 22: Operation timed out
(my_project) R$ ping -c 3 44.200.163.251
PING 44.200.163.251 (44.200.163.251): 56 data bytes
Request timeout for icmp_seq 0
Request timeout for icmp_seq 1

--- 44.200.163.251 ping statistics ---
3 packets transmitted, 0 packets received, 100.0% packet loss
(my_project) R$ 
(my_project) R$ ssh -i ~/.ssh/bootcamp-week2-key.pem ec2-user@172.31.9.161

ssh: connect to host 172.31.9.161 port 22: Operation timed out
(my_project) R$ ssh -i ~/.ssh/bootcamp-week2-key.pem ec2-user@172.31.9.161

^C
(my_project) R$ ssh -i ~/.ssh/bootcamp-week2-key.pem ec2-user@44.200.163.251
The authenticity of host '44.200.163.251 (44.200.163.251)' can't be established.
ED25519 key fingerprint is SHA256:fjqJI9cIs9yVHWRuXzu//qoEz58blW6NAykXiU3t/gQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '44.200.163.251' (ED25519) to the list of known hosts.
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
[ec2-user@ip-172-31-9-161 ~]$ ls
[ec2-user@ip-172-31-9-161 ~]$ ls -l
total 0
[ec2-user@ip-172-31-9-161 ~]$ ls -la
total 12
drwx------. 3 ec2-user ec2-user  74 Feb 25 22:22 .
drwxr-xr-x. 3 root     root      22 Feb 25 22:22 ..
-rw-r--r--. 1 ec2-user ec2-user  18 Jan 28  2023 .bash_logout
-rw-r--r--. 1 ec2-user ec2-user 141 Jan 28  2023 .bash_profile
-rw-r--r--. 1 ec2-user ec2-user 492 Jan 28  2023 .bashrc
drwx------. 2 ec2-user ec2-user  29 Feb 25 22:22 .ssh
[ec2-user@ip-172-31-9-161 ~]$ ls -lh
total 0
[ec2-user@ip-172-31-9-161 ~]$ cd ~
[ec2-user@ip-172-31-9-161 ~]$ pws
-bash: pws: command not found
[ec2-user@ip-172-31-9-161 ~]$ pwd
/home/ec2-user
[ec2-user@ip-172-31-9-161 ~]$ cd /
[ec2-user@ip-172-31-9-161 /]$ pwd
/
[ec2-user@ip-172-31-9-161 /]$ ls
bin  boot  dev  etc  home  lib  lib64  local  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
[ec2-user@ip-172-31-9-161 /]$ cd -
/home/ec2-user
[ec2-user@ip-172-31-9-161 ~]$ cd /var/log
[ec2-user@ip-172-31-9-161 log]$ pwd
/var/log
[ec2-user@ip-172-31-9-161 log]$ ls -l
total 176
lrwxrwxrwx. 1 root   root                39 Feb 14 00:07 README -> ../../usr/share/doc/systemd/README.logs
drwxr-xr-x. 3 root   root                17 Feb 25 22:22 amazon
drwx------. 2 root   root                23 Feb 25 22:22 audit
-rw-rw----. 1 root   utmp                 0 Feb 14 00:07 btmp
drwxr-x---. 2 chrony chrony              72 Feb 25 22:22 chrony
-rw-r-----. 1 root   adm               3609 Feb 25 22:22 cloud-init-output.log
-rw-r-----. 1 root   adm             149774 Feb 25 22:22 cloud-init.log
-rw-r--r--. 1 root   root               392 Feb 25 22:22 dnf.librepo.log
-rw-r--r--. 1 root   root              1010 Feb 25 22:22 dnf.log
-rw-r--r--. 1 root   root                58 Feb 25 22:22 dnf.rpm.log
-rw-r--r--. 1 root   root                60 Feb 25 22:22 hawkey.log
drwxr-sr-x+ 3 root   systemd-journal     46 Feb 25 22:22 journal
-rw-rw-r--. 1 root   utmp            292292 Feb 25 22:47 lastlog
drwx------. 2 root   root                 6 Feb 14 00:07 private
drwxr-xr-x. 2 root   root                18 Feb 25 22:22 sa
drwxr-x---. 2 root   root                 6 Oct 17 22:54 sssd
-rw-------. 1 root   root                 0 Feb 14 00:07 tallylog
-rw-rw-r--. 1 root   utmp              2688 Feb 25 22:47 wtmp
[ec2-user@ip-172-31-9-161 log]$ cd ~
[ec2-user@ip-172-31-9-161 ~]$ cd /home/ec2-user
[ec2-user@ip-172-31-9-161 ~]$ cd Documents
-bash: cd: Documents: No such file or directory
[ec2-user@ip-172-31-9-161 ~]$ cd ..
[ec2-user@ip-172-31-9-161 home]$ ls ./
ec2-user
[ec2-user@ip-172-31-9-161 home]$ mkdir cloud-project
mkdir: cannot create directory ‘cloud-project’: Permission denied
[ec2-user@ip-172-31-9-161 home]$ mkdir -p app/config
mkdir: cannot create directory ‘app’: Permission denied
[ec2-user@ip-172-31-9-161 home]$ pwd
/home
[ec2-user@ip-172-31-9-161 home]$ la
-bash: la: command not found
[ec2-user@ip-172-31-9-161 home]$ pwd
/home
[ec2-user@ip-172-31-9-161 home]$ cd home
-bash: cd: home: No such file or directory
[ec2-user@ip-172-31-9-161 home]$ ls
ec2-user
[ec2-user@ip-172-31-9-161 home]$ cd ec2-user/
[ec2-user@ip-172-31-9-161 ~]$ mkdir -p app/config
[ec2-user@ip-172-31-9-161 ~]$ mkdir -p app/logs
[ec2-user@ip-172-31-9-161 ~]$ mkdir -p app/data
[ec2-user@ip-172-31-9-161 ~]$ mkdir -p scripts/deployment
[ec2-user@ip-172-31-9-161 ~]$ mkdir -p scripts/monitoring
[ec2-user@ip-172-31-9-161 ~]$ tree .
-bash: tree: command not found
[ec2-user@ip-172-31-9-161 ~]$ ls -R
.:
app  scripts

./app:
config  data  logs

./app/config:

./app/data:

./app/logs:

./scripts:
deployment  monitoring

./scripts/deployment:

./scripts/monitoring:
[ec2-user@ip-172-31-9-161 ~]$ touch app/app.py
[ec2-user@ip-172-31-9-161 ~]$ touch app/config/settings.json
[ec2-user@ip-172-31-9-161 ~]$ touch app/config/database.conf
[ec2-user@ip-172-31-9-161 ~]$ touch scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ touch README.md
[ec2-user@ip-172-31-9-161 ~]$ echo "# Cloud Project" > README.md
[ec2-user@ip-172-31-9-161 ~]$ echo "This is a sample cloud application." >> README.md
[ec2-user@ip-172-31-9-161 ~]$ cat > app/app.py << 'EOF'
#!/usr/bin/env python3
# Simple cloud application
print("Hello from the cloud!")
EOF
[ec2-user@ip-172-31-9-161 ~]$ cp app/app.py app/app-backup.py
[ec2-user@ip-172-31-9-161 ~]$ cp -r app app-backup
[ec2-user@ip-172-31-9-161 ~]$ mv app/app-backup.py app/app-old.py
[ec2-user@ip-172-31-9-161 ~]$ mv app/app-old.py scripts/
[ec2-user@ip-172-31-9-161 ~]$ mv app-backup app-archive
[ec2-user@ip-172-31-9-161 ~]$ rm scripts/app-old.py
[ec2-user@ip-172-31-9-161 ~]$ rmdir app-archive/logs
[ec2-user@ip-172-31-9-161 ~]$ rm -r app-archive
[ec2-user@ip-172-31-9-161 ~]$ rm -i filename
rm: cannot remove 'filename': No such file or directory
[ec2-user@ip-172-31-9-161 ~]$ rm -i filename
rm: cannot remove 'filename': No such file or directory
[ec2-user@ip-172-31-9-161 ~]$ cat > app/logs/application.log << 'EOF'
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
[ec2-user@ip-172-31-9-161 ~]$ cat app/logs/application.log
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
[ec2-user@ip-172-31-9-161 ~]$ cat -n app/logs/application.log
     1  2026-01-14 08:00:01 INFO Application started
     2  2026-01-14 08:00:05 INFO Connected to database
     3  2026-01-14 08:00:10 DEBUG Loading configuration
     4  2026-01-14 08:01:23 INFO User login: alice@example.com
     5  2026-01-14 08:02:45 WARNING Database connection slow
     6  2026-01-14 08:03:12 INFO User login: bob@example.com
     7  2026-01-14 08:05:34 ERROR Failed to process request
     8  2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
     9  2026-01-14 08:06:00 INFO Request completed successfully
    10  2026-01-14 08:07:22 INFO User logout: alice@example.com
    11  2026-01-14 08:08:45 WARNING Memory usage at 85%
    12  2026-01-14 08:10:00 INFO Scheduled backup started
    13  2026-01-14 08:15:30 INFO Backup completed successfully
    14  2026-01-14 08:20:00 DEBUG Garbage collection triggered
    15  2026-01-14 08:25:15 INFO Health check: OK
[ec2-user@ip-172-31-9-161 ~]$ less app/logs/application.log

[1]+  Stopped                 less app/logs/application.log
[ec2-user@ip-172-31-9-161 ~]$ head -n 5 app/logs/application.log
2026-01-14 08:00:01 INFO Application started
2026-01-14 08:00:05 INFO Connected to database
2026-01-14 08:00:10 DEBUG Loading configuration
2026-01-14 08:01:23 INFO User login: alice@example.com
2026-01-14 08:02:45 WARNING Database connection slow
[ec2-user@ip-172-31-9-161 ~]$ tail app/logs/application.log
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
[ec2-user@ip-172-31-9-161 ~]$ tail -n 5 app/logs/application.log
2026-01-14 08:08:45 WARNING Memory usage at 85%
2026-01-14 08:10:00 INFO Scheduled backup started
2026-01-14 08:15:30 INFO Backup completed successfully
2026-01-14 08:20:00 DEBUG Garbage collection triggered
2026-01-14 08:25:15 INFO Health check: OK
[ec2-user@ip-172-31-9-161 ~]$ tail -f app/logs/application.log
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

^C
[ec2-user@ip-172-31-9-161 ~]$ ^C
[ec2-user@ip-172-31-9-161 ~]$ grep "ERROR" app/logs/application.log
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
[ec2-user@ip-172-31-9-161 ~]$ grep -i "error" app/logs/application.log
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
[ec2-user@ip-172-31-9-161 ~]$ grep -n "ERROR" app/logs/application.log
7:2026-01-14 08:05:34 ERROR Failed to process request
8:2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
[ec2-user@ip-172-31-9-161 ~]$ grep -c "INFO" app/logs/application.log
9
[ec2-user@ip-172-31-9-161 ~]$ grep -v "DEBUG" app/logs/application.log
2026-01-14 08:00:01 INFO Application started
2026-01-14 08:00:05 INFO Connected to database
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
2026-01-14 08:25:15 INFO Health check: OK
[ec2-user@ip-172-31-9-161 ~]$ grep -r "login" app/
app/logs/application.log:2026-01-14 08:01:23 INFO User login: alice@example.com
app/logs/application.log:2026-01-14 08:03:12 INFO User login: bob@example.com
[ec2-user@ip-172-31-9-161 ~]$ grep -C 2 "ERROR" app/logs/application.log
2026-01-14 08:02:45 WARNING Database connection slow
2026-01-14 08:03:12 INFO User login: bob@example.com
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
2026-01-14 08:06:00 INFO Request completed successfully
2026-01-14 08:07:22 INFO User logout: alice@example.com
[ec2-user@ip-172-31-9-161 ~]$ grep -E "ERROR|WARNING" app/logs/application.log
2026-01-14 08:02:45 WARNING Database connection slow
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
2026-01-14 08:08:45 WARNING Memory usage at 85%
[ec2-user@ip-172-31-9-161 ~]$ grep "User login" app/logs/application.log
2026-01-14 08:01:23 INFO User login: alice@example.com
2026-01-14 08:03:12 INFO User login: bob@example.com
[ec2-user@ip-172-31-9-161 ~]$ grep -E "ERROR|WARNING" app/logs/application.log | wc -l
4
[ec2-user@ip-172-31-9-161 ~]$ grep "08:0[5-9]" app/logs/application.log
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
2026-01-14 08:06:00 INFO Request completed successfully
2026-01-14 08:07:22 INFO User logout: alice@example.com
2026-01-14 08:08:45 WARNING Memory usage at 85%
[ec2-user@ip-172-31-9-161 ~]$ ls -l app/app.py
-rw-r--r--. 1 ec2-user ec2-user 81 Feb 25 23:22 app/app.py
[ec2-user@ip-172-31-9-161 ~]$ chmod +x scripts/deployment/deploy.sh
#
[ec2-user@ip-172-31-9-161 ~]$ chmod +x scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ ls -l scripts/deployment/deploy.sh
-rwxr-xr-x. 1 ec2-user ec2-user 0 Feb 25 23:22 scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ chmod 754 scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ chmod 754 scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ chmod go-w app/config/database.conf
[ec2-user@ip-172-31-9-161 ~]$ chmod a+r README.md
[ec2-user@ip-172-31-9-161 ~]$ chmod -R 755 scripts/
[ec2-user@ip-172-31-9-161 ~]$ sudo chown username file
chown: invalid user: ‘username’
[ec2-user@ip-172-31-9-161 ~]$ sudo chown username:groupname file
chown: invalid user: ‘username:groupname’
[ec2-user@ip-172-31-9-161 ~]$ sudo chown -R username:groupname directory/
chown: invalid user: ‘username:groupname’
[ec2-user@ip-172-31-9-161 ~]$ echo "DB_PASSWORD=secret123" > app/config/database.conf
[ec2-user@ip-172-31-9-161 ~]$ chmod 600 app/config/database.conf
[ec2-user@ip-172-31-9-161 ~]$ ls -l app/config/database.conf
-rw-------. 1 ec2-user ec2-user 22 Feb 25 23:31 app/config/database.conf
[ec2-user@ip-172-31-9-161 ~]$ cat > scripts/deployment/deploy.sh << 'EOF'
#!/bin/bash
echo "Deploying application..."
# Deployment logic here
EOF
[ec2-user@ip-172-31-9-161 ~]$ chmod 750 scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ ls -l scripts/deployment/deploy.sh
-rwxr-x---. 1 ec2-user ec2-user 68 Feb 25 23:32 scripts/deployment/deploy.sh
[ec2-user@ip-172-31-9-161 ~]$ echo "Log entry" > test.log
[ec2-user@ip-172-31-9-161 ~]$ echo "Another entry" >> test.log
[ec2-user@ip-172-31-9-161 ~]$ ls /nonexistent 2> error.log
[ec2-user@ip-172-31-9-161 ~]$ ls /nonexistent > output.log 2>&1
[ec2-user@ip-172-31-9-161 ~]$ ls /nonexistent &> combined.log
[ec2-user@ip-172-31-9-161 ~]$ command > /dev/null 2>&1
[ec2-user@ip-172-31-9-161 ~]$ grep "ERROR" app/logs/application.log | wc -l
2
[ec2-user@ip-172-31-9-161 ~]$ grep "User login" app/logs/application.log | cut -d':' -f4 | sort | uniq
 alice@example.com
 bob@example.com
[ec2-user@ip-172-31-9-161 ~]$ cat app/logs/application.log | awk '{print $3}' | sort | uniq -c | sort -rn | head -5
      9 INFO
      2 WARNING
      2 ERROR
      2 DEBUG
[ec2-user@ip-172-31-9-161 ~]$ ls -lh | sort -k5 -hr | head -10
-rw-r--r--. 1 ec2-user ec2-user 60 Feb 25 23:33 combined.log
-rw-r--r--. 1 ec2-user ec2-user 60 Feb 25 23:32 output.log
-rw-r--r--. 1 ec2-user ec2-user 60 Feb 25 23:32 error.log
drwxr-xr-x. 5 ec2-user ec2-user 58 Feb 25 23:23 app
-rw-r--r--. 1 ec2-user ec2-user 52 Feb 25 23:22 README.md
drwxr-xr-x. 4 ec2-user ec2-user 42 Feb 25 23:23 scripts
-rw-r--r--. 1 ec2-user ec2-user 24 Feb 25 23:32 test.log
total 20K
[ec2-user@ip-172-31-9-161 ~]$ tail -f app/logs/application.log | grep --line-buffered "ERROR"
2026-01-14 08:05:34 ERROR Failed to process request
2026-01-14 08:05:35 ERROR Stack trace: NullPointerException
find . -name "*.py" | wc -l
 
^C
[ec2-user@ip-172-31-9-161 ~]$ du -sh * | sort -h
4.0K    README.md
4.0K    combined.log
4.0K    error.log
4.0K    output.log
4.0K    scripts
4.0K    test.log
12K     app
[ec2-user@ip-172-31-9-161 ~]$ ps aux | grep python | grep -v grep
[ec2-user@ip-172-31-9-161 ~]$ grep -oE '\b[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\b' app/logs/application.log | sort | uniq -c
[ec2-user@ip-172-31-9-161 ~]$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  1.8 172328 17304 ?        Ss   22:22   0:01 /usr/lib/systemd/systemd --switched-root --system --
root           2  0.0  0.0      0     0 ?        S    22:22   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        I<   22:22   0:00 [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   22:22   0:00 [rcu_par_gp]
root           5  0.0  0.0      0     0 ?        I<   22:22   0:00 [slub_flushwq]
root           6  0.0  0.0      0     0 ?        I<   22:22   0:00 [netns]
root           8  0.0  0.0      0     0 ?        I<   22:22   0:00 [kworker/0:0H-events_highpri]
root          10  0.0  0.0      0     0 ?        I<   22:22   0:00 [mm_percpu_wq]
root          11  0.0  0.0      0     0 ?        I    22:22   0:00 [rcu_tasks_kthread]
root          12  0.0  0.0      0     0 ?        I    22:22   0:00 [rcu_tasks_rude_kthread]
root          13  0.0  0.0      0     0 ?        I    22:22   0:00 [rcu_tasks_trace_kthread]
root          14  0.0  0.0      0     0 ?        S    22:22   0:00 [ksoftirqd/0]
root          15  0.0  0.0      0     0 ?        I    22:22   0:00 [rcu_preempt]
root          16  0.0  0.0      0     0 ?        S    22:22   0:00 [migration/0]
root          18  0.0  0.0      0     0 ?        S    22:22   0:00 [cpuhp/0]
root          19  0.0  0.0      0     0 ?        S    22:22   0:00 [cpuhp/1]
root          20  0.0  0.0      0     0 ?        S    22:22   0:00 [migration/1]
root          21  0.0  0.0      0     0 ?        S    22:22   0:00 [ksoftirqd/1]
root          23  0.0  0.0      0     0 ?        I<   22:22   0:00 [kworker/1:0H-events_highpri]
root          26  0.0  0.0      0     0 ?        S    22:22   0:00 [kdevtmpfs]
root          27  0.0  0.0      0     0 ?        I<   22:22   0:00 [inet_frag_wq]
root          28  0.0  0.0      0     0 ?        S    22:22   0:00 [kauditd]
root          29  0.0  0.0      0     0 ?        S    22:22   0:00 [khungtaskd]
root          30  0.0  0.0      0     0 ?        S    22:22   0:00 [oom_reaper]
root          32  0.0  0.0      0     0 ?        I<   22:22   0:00 [writeback]
root          33  0.0  0.0      0     0 ?        S    22:22   0:00 [kcompactd0]
root          34  0.0  0.0      0     0 ?        SN   22:22   0:00 [khugepaged]
root          35  0.0  0.0      0     0 ?        I<   22:22   0:00 [cryptd]
root          36  0.0  0.0      0     0 ?        I<   22:22   0:00 [kintegrityd]
root          37  0.0  0.0      0     0 ?        I<   22:22   0:00 [kblockd]
root          38  0.0  0.0      0     0 ?        I<   22:22   0:00 [blkcg_punt_bio]
root          40  0.0  0.0      0     0 ?        I<   22:22   0:00 [tpm_dev_wq]
root          41  0.0  0.0      0     0 ?        I<   22:22   0:00 [md]
root          42  0.0  0.0      0     0 ?        I<   22:22   0:00 [edac-poller]
root          43  0.0  0.0      0     0 ?        S    22:22   0:00 [watchdogd]
root          44  0.0  0.0      0     0 ?        I<   22:22   0:00 [kworker/0:1H-kblockd]
root          53  0.0  0.0      0     0 ?        S    22:22   0:00 [kswapd0]
root          71  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfsalloc]
root          72  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs_mru_cache]
root          75  0.0  0.0      0     0 ?        I<   22:22   0:00 [kthrotld]
root         122  0.0  0.0      0     0 ?        I<   22:22   0:00 [nvme-wq]
root         124  0.0  0.0      0     0 ?        I<   22:22   0:00 [nvme-reset-wq]
root         126  0.0  0.0      0     0 ?        I<   22:22   0:00 [nvme-delete-wq]
root         153  0.0  0.0      0     0 ?        I<   22:22   0:00 [mld]
root         154  0.0  0.0      0     0 ?        I<   22:22   0:00 [ipv6_addrconf]
root         155  0.0  0.0      0     0 ?        I<   22:22   0:00 [kworker/1:1H-kblockd]
root         173  0.0  0.0      0     0 ?        I<   22:22   0:00 [kstrp]
root         183  0.0  0.0      0     0 ?        I<   22:22   0:00 [zswap-shrink]
root         184  0.0  0.0      0     0 ?        I<   22:22   0:00 [kworker/u5:0]
root         774  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-buf/nvme0n1]
root         775  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-conv/nvme0n]
root         776  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-reclaim/nvm]
root         777  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-blockgc/nvm]
root         778  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-inodegc/nvm]
root         779  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-log/nvme0n1]
root         780  0.0  0.0      0     0 ?        I<   22:22   0:00 [xfs-cil/nvme0n1]
root         781  0.0  0.0      0     0 ?        S    22:22   0:00 [xfsaild/nvme0n1p1]
root         827  0.0  1.6  53544 15204 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-journald
root        1240  0.0  1.2  32128 11552 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-udevd
systemd+    1263  0.0  1.5  22572 14968 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-resolved
root        1266  0.0  0.0      0     0 ?        I<   22:22   0:00 [rpciod]
root        1270  0.0  0.0      0     0 ?        I<   22:22   0:00 [xprtiod]
root        1272  0.0  0.0      0     0 ?        I<   22:22   0:00 [ena]
root        1295  0.0  0.2  21192  2276 ?        S<sl 22:22   0:00 /sbin/auditd
root        1402  0.0  0.6  16372  6416 ?        Ss   22:22   0:00 /usr/bin/systemd-inhibit --what=handle-suspend-key:h
root        1405  0.0  0.1  81428  1576 ?        Ssl  22:22   0:00 /usr/sbin/irqbalance --foreground
libstor+    1406  0.0  0.2   2780  1992 ?        Ss   22:22   0:00 /usr/bin/lsmd -d
root        1409  0.0  0.8  16876  7952 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-homed
root        1410  0.0  1.0  18716 10032 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-logind
dbus        1432  0.0  0.4   8492  4100 ?        Ss   22:22   0:00 /usr/bin/dbus-broker-launch --scope system --audit
systemd+    1434  0.0  1.0 236852  9736 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-networkd
dbus        1436  0.0  0.3   5388  2908 ?        S    22:22   0:00 dbus-broker --log 4 --controller 9 --machine-id ec2d
root        1439  0.0  0.1   2692  1136 ?        S    22:22   0:00 /usr/sbin/acpid -f
root        1441  0.0  0.3 281952  3728 ?        Ssl  22:22   0:00 /usr/sbin/gssproxy -D
root        1512  0.0  2.0 1240432 19364 ?       Ssl  22:22   0:00 /usr/bin/amazon-ssm-agent
root        1517  0.0  0.9  14396  8620 ?        Ss   22:22   0:00 sshd: /usr/sbin/sshd -D [listener] 0 of 10-100 start
root        1537  0.0  0.2   4784  2628 ?        Ss   22:22   0:00 /usr/sbin/atd -f
root        1538  0.0  0.1 221368  1044 tty1     Ss+  22:22   0:00 /sbin/agetty -o -p -- \u --noclear - linux
root        1539  0.0  0.1 221412  1072 ttyS0    Ss+  22:22   0:00 /sbin/agetty -o -p -- \u --keep-baud 115200,57600,38
chrony      1550  0.0  0.4  86464  3924 ?        S    22:22   0:00 /usr/sbin/chronyd -F 2
root        2317  0.0  1.1  15864 10388 ?        Ss   22:46   0:00 sshd: ec2-user [priv]
root        2320  0.0  0.7  16372  6896 ?        Ss   22:46   0:00 /usr/lib/systemd/systemd-userdbd
ec2-user    2325  0.0  1.4  22000 14040 ?        Ss   22:46   0:00 /usr/lib/systemd/systemd --user
ec2-user    2328  0.0  0.7 173668  6632 ?        S    22:46   0:00 (sd-pam)
ec2-user    2335  0.0  0.6  15864  6284 ?        R    22:46   0:00 sshd: ec2-user@pts/0
ec2-user    2336  0.0  0.5 224184  5148 pts/0    Ss   22:46   0:00 -bash
root        2667  0.0  0.0      0     0 ?        I    22:59   0:00 [kworker/u4:1-events_unbound]
root        2970  0.0  0.0      0     0 ?        I    23:10   0:00 [kworker/1:1-events]
root        2971  0.0  0.0      0     0 ?        I    23:10   0:00 [kworker/0:0-events]
root        3312  0.0  0.0      0     0 ?        I    23:23   0:00 [kworker/1:2-cgroup_free]
ec2-user    3366  0.0  0.2 221764  2580 pts/0    T    23:25   0:00 less app/logs/application.log
root        3372  0.0  0.0      0     0 ?        I    23:26   0:00 [kworker/u4:2-events_unbound]
root        3423  0.0  0.0      0     0 ?        I    23:26   0:00 [kworker/0:2-cgroup_release]
root        3494  0.0  0.0      0     0 ?        I    23:29   0:00 [kworker/1:0-cgroup_release]
root        3548  0.0  0.0      0     0 ?        I    23:30   0:00 [kworker/1:3-events_power_efficient]
root        3610  0.0  0.0      0     0 ?        I    23:31   0:00 [kworker/u4:0-events_unbound]
root        3617  0.0  0.7  16732  6840 ?        S    23:33   0:00 systemd-userwork: waiting...
root        3618  0.0  0.7  16732  6824 ?        S    23:33   0:00 systemd-userwork: waiting...
root        3620  0.0  0.7  16732  6824 ?        S    23:33   0:00 systemd-userwork: waiting...
root        3671  0.0  0.0      0     0 ?        I    23:33   0:00 [kworker/0:1]
ec2-user    3695  0.0  0.3 223600  2872 pts/0    R+   23:34   0:00 ps aux
[ec2-user@ip-172-31-9-161 ~]$ ps u
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
ec2-user    2336  0.0  0.5 224184  5148 pts/0    Ss   22:46   0:00 -bash
ec2-user    3366  0.0  0.2 221764  2580 pts/0    T    23:25   0:00 less app/logs/application.log
ec2-user    3696  0.0  0.3 223600  2876 pts/0    R+   23:34   0:00 ps u
[ec2-user@ip-172-31-9-161 ~]$ ps auxf
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           2  0.0  0.0      0     0 ?        S    22:22   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [rcu_par_gp]
root           5  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [slub_flushwq]
root           6  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [netns]
root           8  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kworker/0:0H-events_highpri]
root          10  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [mm_percpu_wq]
root          11  0.0  0.0      0     0 ?        I    22:22   0:00  \_ [rcu_tasks_kthread]
root          12  0.0  0.0      0     0 ?        I    22:22   0:00  \_ [rcu_tasks_rude_kthread]
root          13  0.0  0.0      0     0 ?        I    22:22   0:00  \_ [rcu_tasks_trace_kthread]
root          14  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [ksoftirqd/0]
root          15  0.0  0.0      0     0 ?        I    22:22   0:00  \_ [rcu_preempt]
root          16  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [migration/0]
root          18  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [cpuhp/0]
root          19  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [cpuhp/1]
root          20  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [migration/1]
root          21  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [ksoftirqd/1]
root          23  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kworker/1:0H-events_highpri]
root          26  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [kdevtmpfs]
root          27  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [inet_frag_wq]
root          28  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [kauditd]
root          29  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [khungtaskd]
root          30  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [oom_reaper]
root          32  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [writeback]
root          33  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [kcompactd0]
root          34  0.0  0.0      0     0 ?        SN   22:22   0:00  \_ [khugepaged]
root          35  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [cryptd]
root          36  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kintegrityd]
root          37  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kblockd]
root          38  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [blkcg_punt_bio]
root          40  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [tpm_dev_wq]
root          41  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [md]
root          42  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [edac-poller]
root          43  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [watchdogd]
root          44  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kworker/0:1H-kblockd]
root          53  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [kswapd0]
root          71  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfsalloc]
root          72  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs_mru_cache]
root          75  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kthrotld]
root         122  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [nvme-wq]
root         124  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [nvme-reset-wq]
root         126  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [nvme-delete-wq]
root         153  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [mld]
root         154  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [ipv6_addrconf]
root         155  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kworker/1:1H-xfs-log/nvme0n1p1]
root         173  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kstrp]
root         183  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [zswap-shrink]
root         184  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [kworker/u5:0]
root         774  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-buf/nvme0n1]
root         775  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-conv/nvme0n]
root         776  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-reclaim/nvm]
root         777  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-blockgc/nvm]
root         778  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-inodegc/nvm]
root         779  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-log/nvme0n1]
root         780  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xfs-cil/nvme0n1]
root         781  0.0  0.0      0     0 ?        S    22:22   0:00  \_ [xfsaild/nvme0n1p1]
root        1266  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [rpciod]
root        1270  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [xprtiod]
root        1272  0.0  0.0      0     0 ?        I<   22:22   0:00  \_ [ena]
root        2667  0.0  0.0      0     0 ?        I    22:59   0:00  \_ [kworker/u4:1-events_unbound]
root        2970  0.0  0.0      0     0 ?        I    23:10   0:00  \_ [kworker/1:1-events]
root        2971  0.0  0.0      0     0 ?        I    23:10   0:00  \_ [kworker/0:0-events]
root        3312  0.0  0.0      0     0 ?        I    23:23   0:00  \_ [kworker/1:2-cgroup_free]
root        3372  0.0  0.0      0     0 ?        I    23:26   0:00  \_ [kworker/u4:2-events_unbound]
root        3423  0.0  0.0      0     0 ?        I    23:26   0:00  \_ [kworker/0:2-cgroup_release]
root        3494  0.0  0.0      0     0 ?        I    23:29   0:00  \_ [kworker/1:0-cgroup_release]
root        3548  0.0  0.0      0     0 ?        I    23:30   0:00  \_ [kworker/1:3-events_power_efficient]
root        3610  0.0  0.0      0     0 ?        I    23:31   0:00  \_ [kworker/u4:0-events_unbound]
root        3671  0.0  0.0      0     0 ?        I    23:33   0:00  \_ [kworker/0:1]
root           1  0.0  1.8 172328 17304 ?        Ss   22:22   0:01 /usr/lib/systemd/systemd --switched-root --system --
root         827  0.0  1.6  53544 15204 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-journald
root        1240  0.0  1.2  32128 11552 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-udevd
systemd+    1263  0.0  1.5  22572 14968 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-resolved
root        1295  0.0  0.2  21192  2276 ?        S<sl 22:22   0:00 /sbin/auditd
root        1402  0.0  0.6  16372  6416 ?        Ss   22:22   0:00 /usr/bin/systemd-inhibit --what=handle-suspend-key:h
root        1439  0.0  0.1   2692  1136 ?        S    22:22   0:00  \_ /usr/sbin/acpid -f
root        1405  0.0  0.1  81428  1576 ?        Ssl  22:22   0:00 /usr/sbin/irqbalance --foreground
libstor+    1406  0.0  0.2   2780  1992 ?        Ss   22:22   0:00 /usr/bin/lsmd -d
root        1409  0.0  0.8  16876  7952 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-homed
root        1410  0.0  1.0  18716 10032 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-logind
dbus        1432  0.0  0.4   8492  4100 ?        Ss   22:22   0:00 /usr/bin/dbus-broker-launch --scope system --audit
dbus        1436  0.0  0.3   5388  2908 ?        S    22:22   0:00  \_ dbus-broker --log 4 --controller 9 --machine-id 
systemd+    1434  0.0  1.0 236852  9736 ?        Ss   22:22   0:00 /usr/lib/systemd/systemd-networkd
root        1441  0.0  0.3 281952  3728 ?        Ssl  22:22   0:00 /usr/sbin/gssproxy -D
root        1512  0.0  2.0 1240432 19364 ?       Ssl  22:22   0:00 /usr/bin/amazon-ssm-agent
root        1517  0.0  0.9  14396  8620 ?        Ss   22:22   0:00 sshd: /usr/sbin/sshd -D [listener] 0 of 10-100 start
root        2317  0.0  1.1  15864 10388 ?        Ss   22:46   0:00  \_ sshd: ec2-user [priv]
ec2-user    2335  0.0  0.6  15864  6284 ?        S    22:46   0:00      \_ sshd: ec2-user@pts/0
ec2-user    2336  0.0  0.5 224184  5148 pts/0    Ss   22:46   0:00          \_ -bash
top - 23:39:54 up  1:17,  1 user,  load average: 0.00, 0.00, 0.00
Tasks:  99 total,   1 running,  97 sleeping,   1 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :    916.8 total,    581.2 free,    171.7 used,    164.0 buff/cache
MiB Swap:      0.0 total,      0.0 free,      0.0 used.    613.6 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                         
   3699 ec2-user  20   0  224020   3484   2824 R   0.3   0.4   0:00.22 top                                             
      1 root      20   0  172328  17304  10800 S   0.0   1.8   0:01.09 systemd                                         
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kthreadd                                        
      3 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 rcu_gp                                          
      4 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 rcu_par_gp                                      
      5 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 slub_flushwq                                    
      6 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 netns                                           
      8 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/0:0H-events_highpri                     
     10 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 mm_percpu_wq                                    
     11 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_kthread                               
     12 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_rude_kthread                          
     13 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tasks_trace_kthread                         
     14 root      20   0       0      0      0 S   0.0   0.0   0:00.04 ksoftirqd/0                                     
     15 root      20   0       0      0      0 I   0.0   0.0   0:00.08 rcu_preempt                                     
     16 root      rt   0       0      0      0 S   0.0   0.0   0:00.01 migration/0                                     
     18 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/0                                         
     19 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/1                                         
     20 root      rt   0       0      0      0 S   0.0   0.0   0:00.03 migration/1                                     
     21 root      20   0       0      0      0 S   0.0   0.0   0:00.05 ksoftirqd/1                                     
     23 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/1:0H-events_highpri                     
     26 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kdevtmpfs                                       
     27 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 inet_frag_wq                                    
     28 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kauditd                                         
     29 root      20   0       0      0      0 S   0.0   0.0   0:00.00 khungtaskd                                      
     30 root      20   0       0      0      0 S   0.0   0.0   0:00.00 oom_reaper                                      
     32 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 writeback                                       
     33 root      20   0       0      0      0 S   0.0   0.0   0:00.12 kcompactd0                                      
     34 root      39  19       0      0      0 S   0.0   0.0   0:00.00 khugepaged                                      
     35 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 cryptd                                          
     36 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kintegrityd                                     
     37 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kblockd                                         
     38 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 blkcg_punt_bio                                  
     40 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 tpm_dev_wq                                      
     41 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 md                                              
     42 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 edac-poller                                     
     43 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 watchdogd                                       
     44 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/0:1H-kblockd                            
     53 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kswapd0                                         
     71 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 xfsalloc                                        
     72 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 xfs_mru_cache                                   
     75 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kthrotld                                        
    122 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 nvme-wq                                         
    124 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 nvme-reset-wq                                   
    126 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 nvme-delete-wq                                  
    153 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 mld                                             
    154 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 ipv6_addrconf                                   
    155 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/1:1H-kblockd                            
    173 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kstrp                                           
[ec2-user@ip-172-31-9-161 ~]$ ^C
[ec2-user@ip-172-31-9-161 ~]$ 



(my_project) R$ ssh -i ~/.ssh/bootcamp-week2-key.pem ec2-user@44.200.163.251
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
Last login: Wed Feb 25 22:47:00 2026 from 91.35.25.152
[ec2-user@ip-172-31-9-161 ~]$ df -h
Filesystem        Size  Used Avail Use% Mounted on
devtmpfs          4.0M     0  4.0M   0% /dev
tmpfs             459M     0  459M   0% /dev/shm
tmpfs             184M  436K  183M   1% /run
/dev/nvme0n1p1    8.0G  1.5G  6.5G  19% /
tmpfs             459M     0  459M   0% /tmp
/dev/nvme0n1p128   10M  1.3M  8.7M  13% /boot/efi
tmpfs              92M     0   92M   0% /run/user/1000
[ec2-user@ip-172-31-9-161 ~]$ du -sh ~/cloud-project
du: cannot access '/home/ec2-user/cloud-project': No such file or directory
[ec2-user@ip-172-31-9-161 ~]$ free -h
               total        used        free      shared  buff/cache   available
Mem:           916Mi       185Mi       564Mi       0.0Ki       166Mi       599Mi
Swap:             0B          0B          0B
[ec2-user@ip-172-31-9-161 ~]$ lscpu
Architecture:                x86_64
  CPU op-mode(s):            32-bit, 64-bit
  Address sizes:             46 bits physical, 48 bits virtual
  Byte Order:                Little Endian
CPU(s):                      2
  On-line CPU(s) list:       0,1
Vendor ID:                   GenuineIntel
  Model name:                Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
    CPU family:              6
    Model:                   85
    Thread(s) per core:      2
    Core(s) per socket:      1
    Socket(s):               1
    Stepping:                7
    BogoMIPS:                4999.99
    Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca c
                             mov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx p
                             dpe1gb rdtscp lm constant_tsc rep_good nopl xtopology nons
                             top_tsc cpuid tsc_known_freq pni pclmulqdq ssse3 fma cx16 
                             pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer 
                             aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowpref
                             etch cpuid_fault invpcid_single pti fsgsbase tsc_adjust bm
                             i1 avx2 smep bmi2 erms invpcid mpx avx512f avx512dq rdseed
                              adx smap clflushopt clwb avx512cd avx512bw avx512vl xsave
                             opt xsavec xgetbv1 xsaves ida arat pku ospke
Virtualization features:     
  Hypervisor vendor:         KVM
  Virtualization type:       full
Caches (sum of all):         
  L1d:                       32 KiB (1 instance)
  L1i:                       32 KiB (1 instance)
  L2:                        1 MiB (1 instance)
  L3:                        35.8 MiB (1 instance)
NUMA:                        
  NUMA node(s):              1
  NUMA node0 CPU(s):         0,1
Vulnerabilities:             
  Gather data sampling:      Unknown: Dependent on hypervisor status
  Indirect target selection: Mitigation; Aligned branch/return thunks
  Itlb multihit:             KVM: Mitigation: VMX unsupported
  L1tf:                      Mitigation; PTE Inversion
  Mds:                       Vulnerable: Clear CPU buffers attempted, no microcode; SMT
                              Host state unknown
  Meltdown:                  Mitigation; PTI
  Mmio stale data:           Vulnerable: Clear CPU buffers attempted, no microcode; SMT
                              Host state unknown
  Reg file data sampling:    Not affected
  Retbleed:                  Vulnerable
  Spec rstack overflow:      Not affected
  Spec store bypass:         Vulnerable
  Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sa
                             nitization
  Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB
                             -eIBRS Not affected; BHI Retpoline
  Srbds:                     Not affected
  Tsa:                       Not affected
  Tsx async abort:           Not affected
  Vmscape:                   Not affected
[ec2-user@ip-172-31-9-161 ~]$ systemctl list-units --type=service --state=running
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
lines 1-14...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
lines 1-15...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
lines 1-16...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
lines 1-17...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
lines 1-19...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
lines 1-20...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
  user@1000.service          loaded active running User Manager for UID 1000

lines 1-22...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
  user@1000.service          loaded active running User Manager for UID 1000

LOAD   = Reflects whether the unit definition was properly loaded.
lines 1-23...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
  user@1000.service          loaded active running User Manager for UID 1000

LOAD   = Reflects whether the unit definition was properly loaded.
ACTIVE = The high-level unit activation state, i.e. generalization of SUB.
lines 1-24...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
  user@1000.service          loaded active running User Manager for UID 1000

LOAD   = Reflects whether the unit definition was properly loaded.
ACTIVE = The high-level unit activation state, i.e. generalization of SUB.
SUB    = The low-level unit activation state, values depend on unit type.
lines 1-25...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
  user@1000.service          loaded active running User Manager for UID 1000

LOAD   = Reflects whether the unit definition was properly loaded.
ACTIVE = The high-level unit activation state, i.e. generalization of SUB.
SUB    = The low-level unit activation state, values depend on unit type.
20 loaded units listed.
lines 1-26...skipping...
  UNIT                       LOAD   ACTIVE SUB     DESCRIPTION
  acpid.service              loaded active running ACPI Event Daemon
  amazon-ssm-agent.service   loaded active running amazon-ssm-agent
  atd.service                loaded active running Deferred execution scheduler
  auditd.service             loaded active running Security Auditing Service
  chronyd.service            loaded active running NTP client/server
  dbus-broker.service        loaded active running D-Bus System Message Bus
  getty@tty1.service         loaded active running Getty on tty1
  gssproxy.service           loaded active running GSSAPI Proxy Daemon
  irqbalance.service         loaded active running irqbalance daemon
  libstoragemgmt.service     loaded active running libstoragemgmt plug-in server daemon
  serial-getty@ttyS0.service loaded active running Serial Getty on ttyS0
  sshd.service               loaded active running OpenSSH server daemon
  systemd-homed.service      loaded active running Home Area Manager
  systemd-journald.service   loaded active running Journal Service
  systemd-logind.service     loaded active running User Login Management
  systemd-networkd.service   loaded active running Network Configuration
  systemd-resolved.service   loaded active running Network Name Resolution
  systemd-udevd.service      loaded active running Rule-based Manager for Device Event>
  systemd-userdbd.service    loaded active running User Database Manager
  user@1000.service          loaded active running User Manager for UID 1000

LOAD   = Reflects whether the unit definition was properly loaded.
ACTIVE = The high-level unit activation state, i.e. generalization of SUB.
SUB    = The low-level unit activation state, values depend on unit type.
20 loaded units listed.
~

[ec2-user@ip-172-31-9-161 ~]$ netstat -tuln
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN     
tcp6       0      0 :::22                   :::*                    LISTEN     
udp        0      0 127.0.0.1:323           0.0.0.0:*                          
udp        0      0 172.31.9.161:68         0.0.0.0:*                          
udp6       0      0 ::1:323                 :::*                               
udp6       0      0 fe80::aeff:febd:56b:546 :::*                               
[ec2-user@ip-172-31-9-161 ~]$ 
[ec2-user@ip-172-31-9-161 ~]$ 
[ec2-user@ip-172-31-9-161 ~]$ uptime
 01:50:07 up  3:27,  1 user,  load average: 0.00, 0.00, 0.00
[ec2-user@ip-172-31-9-161 ~]$ sudo tail -f /var/log/syslog
tail: cannot open '/var/log/syslog' for reading: No such file or directory
tail: no files remaining
[ec2-user@ip-172-31-9-161 ~]$ sudo journalctl -f
Feb 26 01:50:28 ip-172-31-9-161.ec2.internal systemd[1]: refresh-policy-routes@ens5.service: Deactivated successfully.
Feb 26 01:50:28 ip-172-31-9-161.ec2.internal systemd[1]: Finished refresh-policy-routes@ens5.service - Refresh policy routes for ens5.
Feb 26 01:50:28 ip-172-31-9-161.ec2.internal audit[1]: SERVICE_START pid=1 uid=0 auid=4294967295 ses=4294967295 subj=system_u:system_r:init_t:s0 msg='unit=refresh-policy-routes@ens5 comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
Feb 26 01:50:28 ip-172-31-9-161.ec2.internal audit[1]: SERVICE_STOP pid=1 uid=0 auid=4294967295 ses=4294967295 subj=system_u:system_r:init_t:s0 msg='unit=refresh-policy-routes@ens5 comm="systemd" exe="/usr/lib/systemd/systemd" hostname=? addr=? terminal=? res=success'
Feb 26 01:50:29 ip-172-31-9-161.ec2.internal audit[7723]: USER_ACCT pid=7723 uid=1000 auid=1000 ses=3 subj=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023 msg='op=PAM:accounting grantors=pam_unix acct="ec2-user" exe="/usr/bin/sudo" hostname=? addr=? terminal=/dev/pts/0 res=success'
Feb 26 01:50:29 ip-172-31-9-161.ec2.internal sudo[7723]: ec2-user : TTY=pts/0 ; PWD=/home/ec2-user ; USER=root ; COMMAND=/usr/bin/journalctl -f
Feb 26 01:50:29 ip-172-31-9-161.ec2.internal audit[7723]: USER_CMD pid=7723 uid=1000 auid=1000 ses=3 subj=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023 msg='cwd="/home/ec2-user" cmd=6A6F75726E616C63746C202D66 exe="/usr/bin/sudo" terminal=pts/0 res=success'
Feb 26 01:50:29 ip-172-31-9-161.ec2.internal audit[7723]: CRED_REFR pid=7723 uid=1000 auid=1000 ses=3 subj=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023 msg='op=PAM:setcred grantors=pam_env,pam_unix acct="root" exe="/usr/bin/sudo" hostname=? addr=? terminal=/dev/pts/0 res=success'
Feb 26 01:50:29 ip-172-31-9-161.ec2.internal sudo[7723]: pam_unix(sudo:session): session opened for user root(uid=0) by ec2-user(uid=1000)
Feb 26 01:50:29 ip-172-31-9-161.ec2.internal audit[7723]: USER_START pid=7723 uid=1000 auid=1000 ses=3 subj=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023 msg='op=PAM:session_open grantors=pam_keyinit,pam_limits,pam_keyinit,pam_limits,pam_systemd,pam_unix acct="root" exe="/usr/bin/sudo" hostname=? addr=? terminal=/dev/pts/0 res=success'



Bash Get disk usage, memory stats, and CPU core count
IN
df -h / && echo "---" && vm_stat | awk '/Pages free|Pages active|Pages inactive|Pages wired/ {print}' && sysctl -n hw.memsize && echo "---" && sysctl -n hw.logicalcpu hw.physicalcpu

OUT
Filesystem        Size    Used   Avail Capacity iused ifree %iused  Mounted on
/dev/disk3s1s1   460Gi    15Gi    92Gi    15%    453k  960M    0%   /
---
Pages free:                               25011.
Pages active:                            162086.
Pages inactive:                          158820.
Pages wired down:                        164073.
17179869184
---
8
8
System Summary
Disk (/):

Metric    Value
Total    460 GB
Used    15 GB
Available    92 GB
Capacity    15% used
Memory:

Metric    Value
Total RAM    16 GB
Free pages    ~98 MB (25,011 × 4KB)
Active    ~633 MB
Inactive    ~620 MB
Wired    ~641 MB
CPU:

Metric    Value
Physical cores    8
Logical cores    8





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

Task: Analyze the CloudTrail log and determine:

How many events per user?
What EC2 operations occurred?
List all unique event types
I don't see a CloudTrail log file provided. Let me check the current directory for any log files.

Bash List files in home directory
IN
ls /Users/sumera/ | head -30

OUT
Applications

IN
ls /Users/sumera/aws-logs/

OUT
cloudtrail.json
Read cloudtrail.json
Here's the analysis of cloudtrail.json:

Events Per User
User    Count    Events
alice    2    CreateBucket, DeleteBucket
bob    1    PutObject
charlie    2    RunInstances, TerminateInstances
EC2 Operations
Event    User    Resource
RunInstances    charlie    i-1234567890
TerminateInstances    charlie    i-0987654321
Both EC2 operations were performed by charlie — he launched one instance and terminated a different one.

Unique Event Types (5 total)
CreateBucket
PutObject
DeleteBucket
RunInstances
TerminateInstances
Summary: 5 total events across 3 users. S3 activity from alice and bob, EC2 activity exclusively from charlie.



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
