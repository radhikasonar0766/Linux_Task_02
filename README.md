#Linux_Task_02_RadhikaSonar

## Objective
To learn Linux user management, groups, file ownership, and permissions.

## Part A: Understanding Users
### Commands Used
```bash
whoami
id
cat /etc/passwd
```
## Part B: Create Users & Groups
### Groups Created
* interns
* cyberteam

### Users Created
* student1
* student2
* student3

### Commands Used
```bash
sudo groupadd interns
sudo groupadd cyberteam

sudo useradd -m student1
sudo useradd -m student2
sudo useradd -m student3

sudo usermod -aG interns student1
sudo usermod -aG cyberteam student2
```

### Verification
```bash
groups
id student1
id student2
```
## Part C: File Ownership
### Commands Used
```bash
mkdir CyberSecurity_Project
cd CyberSecurity_Project

touch report.txt notes.txt credentials.txt

ls -l
sudo chown student2 report.txt
```

## Part D: File Permissions
### Commands Used
```bash
touch security_policy.txt

chmod 444 security_policy.txt
chmod 664 security_policy.txt
chmod 777 security_policy.txt
```
### Permissions Applied
| Permission | Meaning      |
| ---------- | ------------ |
| 444        | Read Only    |
| 664        | Read & Write |
| 777        | Full Access  |

## Part E: Permission Analysis
### 755
* Owner: rwx
* Group: r-x
* Others: r-x
* Use: Scripts and directories

## Part F: Security Challenge
| File                | Permission | Reason            |
| ------------------- | ---------- | ----------------- |
| password_backup.txt | 600        | Sensitive data    |
| public_notice.txt   | 644        | Public reading    |
| system_log.txt      | 640        | Admin access only |
| personal_notes.txt  | 600        | Private file      |

### Reasoning
Sensitive files should be restricted, while public files can be readable by all users.

## Tools Used
whoami, id, cat, groupadd, useradd, usermod, groups, mkdir, touch, ls, chown, chmod

## Conclusion
This task helped me understand Linux users, groups, ownership, file permissions, and basic security concepts.
