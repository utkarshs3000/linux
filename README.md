# RHEL Linux Security & SOC Investigation Lab

## Executive Summary

This repository documents my hands-on Linux practice on **Red Hat Enterprise Linux (RHEL)** with a security-focused approach. Instead of only learning commands, I used them to perform tasks that are useful in an entry-level SOC environment: reviewing users and permissions, checking processes and services, investigating SSH authentication activity, tracing open ports to running processes, reviewing logs, checking installed packages, and examining scheduled tasks.

The main goal of this project was to build a practical Linux foundation for **SOC Analyst / Cyber Defense Analyst** roles. Each lab shows what I practiced, the commands I used, the result I observed, and why that activity matters during a security investigation.

---

## What This Project Demonstrates

- RHEL/Linux command-line navigation and file investigation
- File permissions, ownership, users and groups
- Process identification and termination
- Service status checks and service log review
- SSH access and authentication-log analysis
- Successful and failed login investigation
- Open-port and listening-process investigation
- Package and software version checks
- Cron/scheduled-task inspection
- Environment variable inspection
- Basic evidence collection and Linux troubleshooting
- Understanding how normal Linux administration connects to SOC investigations

---

## Hands-On Labs

| Lab | What I Practiced | SOC Relevance |
|---|---|---|
| [Files and Directories](filesystem.md) | Navigating, creating, copying, moving, reading and searching files with `pwd`, `ls`, `cd`, `cp`, `mv`, `cat`, `less`, `grep` and `find` | Helps locate suspicious files, logs and configuration evidence |
| [Permissions](permissions.md) | Viewing and changing file permissions with `ls` and `chmod` | Helps identify unsafe access permissions or unexpected file changes |
| [Users and Groups](users-and-groups.md) | Creating a test user/group, checking account details and changing ownership with `useradd`, `id`, `getent`, `usermod` and `chown` | Helps investigate accounts, privileges, group membership and file ownership |
| [Processes](processes.md) | Starting a background process, identifying its PID and details, and stopping it with `ps`, `grep` and `kill` | Helps investigate unknown or suspicious processes |
| [Services and Logs](services.md) | Listing running services, checking `NetworkManager`, and reviewing service logs with `systemctl` and `journalctl` | Helps identify unexpected services, failures and unusual service activity |
| [SSH](ssh.md) | Checking `sshd` and logging in to RHEL through SSH using a test account | Helps understand remote access and SSH activity |
| [SSH & Authentication Logs](logs.md) | Reviewing successful SSH logins, failed passwords and authentication failures using `journalctl` and `/var/log/secure` | Helps investigate suspicious logins, password guessing and unauthorized-access attempts |
| [Network & Open Ports](networking-%26-open-ports.md) | Starting a local web server on port `8080`, identifying the listening port, tracing it to its process, checking activity and stopping it | Helps investigate unknown services, open ports and suspicious processes |
| [Package Management](package-mgmt.md) | Checking installed OpenSSH packages and versions with `rpm` and `dnf` | Helps identify installed software, versions and potentially outdated packages |
| [Cron Jobs](cron.md) | Checking `crond`, creating a scheduled task and confirming execution | Helps identify scheduled tasks that could be used for persistence |
| [Environment Variables](env-variables.md) | Viewing, creating and removing environment variables with `env`, `export` and `unset` | Helps identify unusual PATH values or environment changes |

---

## SOC-Focused Investigation Practice

A major part of this project was learning how to move from a simple observation to an investigation.

### Example 1 — Authentication Investigation

I generated SSH login activity with a test account and reviewed the related RHEL logs. I was able to identify both **successful logins and failed password attempts**.

The investigation flow was:

```text
SSH login attempt
        ↓
Check sshd logs
        ↓
Identify user and authentication result
        ↓
Compare failed and successful attempts
        ↓
Decide whether the activity needs further investigation
```

This gave me practical experience with Linux authentication evidence instead of only reading about log analysis.

### Example 2 — Open Port and Process Investigation

I started a local Python web server on port `8080` and then treated it as an unknown service that needed to be investigated.

I used Linux tools to:

1. Confirm that port `8080` was listening.
2. Identify the process using the port.
3. Check the process details.
4. Check where the process was running from.
5. Review its activity.
6. Stop the process.
7. Confirm that the port was no longer listening.

The investigation flow was:

```text
Open port detected
        ↓
Identify listening process
        ↓
Check PID, user and command
        ↓
Check process location/activity
        ↓
Decide whether it is expected
        ↓
Stop and verify if required
```

This exercise helped me understand how **network evidence and endpoint/process evidence connect together** during an investigation.

---

## Commands Practiced

```bash
# Files and navigation
pwd
ls
cd
cp
mv
cat
less
grep
find

# Permissions and ownership
chmod
chown

# Users and groups
useradd
passwd
id
getent
groupadd
usermod

# Processes
ps
ps aux
grep
kill

# Services and logs
systemctl
journalctl

# Networking and remote access
ss
ssh
curl
wget

# Process/file investigation
readlink

# Package management
rpm
dnf

# Scheduled tasks
crontab

# Environment
env
export
unset
```

---

## Skills I Can Apply From This Project

After completing these labs, I am comfortable with the basic RHEL tasks needed to start investigating a Linux endpoint, including:

- Finding files and searching for useful information
- Checking file permissions and ownership
- Reviewing users and group membership
- Identifying running processes and their owners
- Checking active services and their logs
- Reviewing SSH authentication activity
- Identifying failed and successful login attempts
- Finding listening ports and tracing them to processes
- Checking installed packages and versions
- Reviewing cron jobs for scheduled activity
- Checking environment variables for unusual changes

I am continuing to build these skills toward an entry-level **SOC / Cyber Defense Analyst** role, with the goal of being able to investigate Linux alerts using evidence from users, processes, services, logs and network activity.

---

## Why Linux Matters for SOC Work

Linux systems are common across servers, cloud environments and security infrastructure. For a SOC analyst, knowing Linux makes it easier to answer questions such as:

- Which user performed this action?
- Is this process expected?
- What service is running?
- What is listening on this port?
- Did an SSH login succeed or fail?
- Is there a suspicious scheduled task?
- Where can I find evidence of what happened?

This project is my practical foundation for answering those questions using RHEL.

---

## Repository

**GitHub:** [github.com/utkarshs3000/linux](https://github.com/utkarshs3000/linux)

---

> **Note:** All activities in this repository were performed in my own lab environment for learning and defensive-security practice.
