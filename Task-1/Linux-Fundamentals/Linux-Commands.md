# Linux Fundamentals – Essential Commands

## 1. Introduction

Linux is an open-source, Unix-like operating system widely used in servers, cloud computing, networking, and cybersecurity.

In cybersecurity, Linux is commonly used for system administration, security monitoring, network analysis, and penetration testing.

Kali Linux is a Debian-based Linux distribution designed for cybersecurity and penetration testing.

## 2. Basic Linux Commands

| Command | Description | Example |
|---|---|---|
| `pwd` | Displays the current working directory | `pwd` |
| `ls` | Lists files and directories | `ls -l` |
| `cd` | Changes the current directory | `cd Documents` |
| `mkdir` | Creates a new directory | `mkdir lab` |
| `touch` | Creates an empty file | `touch notes.txt` |
| `cat` | Displays file contents | `cat notes.txt` |
| `cp` | Copies files | `cp file.txt backup.txt` |
| `mv` | Moves or renames files | `mv old.txt new.txt` |
| `rm` | Removes files | `rm file.txt` |
| `clear` | Clears the terminal screen | `clear` |
| `whoami` | Displays the current username | `whoami` |
| `uname` | Displays system information | `uname -a` |

## 3. File and Directory Management

Linux provides commands to create, navigate, copy, move, and delete files and directories.

### Common commands

```bash
pwd
ls -la
mkdir cybersecurity
cd cybersecurity
touch report.txt
cat report.txt
```

### Explanation

- `pwd`: Shows the current directory.
- `ls -la`: Displays all files, including hidden files, with details.
- `mkdir`: Creates a directory.
- `cd`: Enters the selected directory.
- `touch`: Creates an empty file.
- `cat`: Displays file contents.

## 4. User and Permission Management

Linux uses file permissions to control access to files and directories.

There are three main permission categories:

- **User (u):** Owner of the file.
- **Group (g):** Users belonging to the file's group.
- **Others (o):** All other users.

### Permission types

| Permission | Symbol | Numeric Value |
|---|---|---|
| Read | r | 4 |
| Write | w | 2 |
| Execute | x | 1 |

### Important commands

```bash
ls -l
chmod 755 filename
chmod 644 filename
chown username filename
```

**Explanation:**

- `ls -l`: Displays file permissions and ownership.
- `chmod`: Changes file permissions.
- `chown`: Changes file ownership.

### Example: chmod 755

- Owner: Read, Write, Execute (7)
- Group: Read, Execute (5)
- Others: Read, Execute (5)

This is useful for controlling access to sensitive system files and scripts.

## 5. User Information Commands

| Command | Purpose |
|---|---|
| `whoami` | Shows current username |
| `id` | Displays user and group IDs |
| `who` | Shows logged-in users |
| `sudo` | Executes a command with elevated privileges |
| `passwd` | Changes a user's password |

Example:

```bash
whoami
id
sudo apt update
```

## 6. Process Management

A process is a running instance of a program.

Linux provides several commands to monitor and manage running processes.

| Command | Purpose |
|---|---|
| `ps` | Displays running processes |
| `ps aux` | Displays detailed process information |
| `top` | Monitors processes in real time |
| `kill` | Sends a signal to a process |
| `pgrep` | Searches for processes by name |

Example:

```bash
ps aux
top
```

Process monitoring is important for identifying unusual or suspicious system activity.

## 7. Package Management

Kali Linux uses the APT package management system to install, update, and remove software.

### Important commands

```bash
sudo apt update
sudo apt upgrade
sudo apt install nmap
sudo apt remove nmap
```

**Explanation:**

- `apt update`: Refreshes available package information.
- `apt upgrade`: Upgrades installed packages.
- `apt install`: Installs a package.
- `apt remove`: Removes an installed package.

## 8. System and Network Information

Linux provides commands to inspect network interfaces and connectivity.

| Command | Purpose |
|---|---|
| `ip a` | Displays IP addresses and interfaces |
| `ip route` | Displays routing information |
| `ping` | Tests network connectivity |
| `ss -tuln` | Displays listening TCP/UDP sockets |
| `hostname` | Displays system hostname |
| `curl` | Transfers data using supported network protocols |

Examples:

```bash
ip -br a
ip route
ping -c 4 192.168.56.102
ss -tuln
hostname
```

## 9. Log Monitoring

Linux system logs provide information about system events, authentication activity, and errors.

Important log locations:

| Log File | Purpose |
|---|---|
| `/var/log/auth.log` | Authentication-related events on Debian-based systems |
| `/var/log/syslog` | General system messages |
| `/var/log/kern.log` | Kernel-related messages |

Commands:

```bash
sudo tail -f /var/log/auth.log
sudo tail -n 20 /var/log/syslog
```

Log monitoring is an important activity for SOC analysts because it helps identify suspicious login attempts and unusual system events.

## 10. Practical Learning Outcomes

After studying these Linux fundamentals, the following concepts can be understood:

1. Navigating the Linux filesystem.
2. Creating and managing files and directories.
3. Understanding Linux file permissions.
4. Identifying users and groups.
5. Monitoring running processes.
6. Managing software packages.
7. Checking network interfaces and connectivity.
8. Understanding basic system log analysis.

## 11. Conclusion

Linux fundamentals are essential for cybersecurity professionals. Knowledge of Linux commands helps in system administration, network troubleshooting, permission management, process monitoring, and security log analysis.

These commands provide a foundation for further practical work in cybersecurity and SOC operations.

**Note:** Commands listed in this document are reference examples. Only mark practical exercises as completed after actually executing and verifying them in your Kali Linux environment.
