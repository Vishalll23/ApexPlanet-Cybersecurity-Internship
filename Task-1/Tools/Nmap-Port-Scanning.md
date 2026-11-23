# Nmap – Network Scanning and Enumeration

## 1. Objective
To understand network scanning, identify open ports, detect running services, and perform operating system detection using Nmap.

## 2. Introduction
Nmap (Network Mapper) is an open-source network scanning tool used to discover hosts, open ports, and services running on a network.

It is commonly used by network administrators and cybersecurity professionals for network discovery and security assessments.

## 3. Tool Used
- Kali Linux
- Nmap 7.99
- Metasploitable 2 (Target VM)

## 4. Lab Configuration

| Machine | IP Address |
|---|---|
| Kali Linux | 192.168.56.101 |
| Metasploitable 2 | 192.168.56.102 |

Both machines were connected through a VirtualBox Host-Only network.

## 5. Practical Implementation

### Practical 1: Nmap Version Verification

```bash
nmap --version
```

Verified that Nmap 7.99 was installed.

### Practical 2: Basic Port Scanning

```bash
nmap 192.168.56.102
```

The scan identified open TCP ports and their associated services.

Observed examples:
- 21 – FTP
- 22 – SSH
- 23 – Telnet
- 80 – HTTP
- 3306 – MySQL
- 5432 – PostgreSQL
- 5900 – VNC

The scan reported 23 open TCP ports and 977 closed TCP ports.

### Practical 3: Service Version Detection

```bash
nmap -sV 192.168.56.102
```

This option attempts to identify the software and version running on detected open ports.

### Practical 4: Operating System Detection

```bash
sudo nmap -O 192.168.56.102
```

This option attempts to identify the target operating system using network responses.

## 6. Important Nmap Options

| Option | Description |
|---|---|
| `-sV` | Service version detection |
| `-O` | Operating system detection |
| `-p` | Specify ports |
| `-sS` | TCP SYN scan |
| `-A` | Enables several advanced detection features |

## 7. Learning Outcomes
- Understood the purpose of network scanning.
- Identified open and closed TCP ports.
- Learned basic service detection.
- Practiced operating system detection.
- Understood how Nmap supports network security assessments.

## 8. Screenshots
Practical screenshots are stored in:

`Task-1/Tools/Screenshots/`

## 9. Conclusion
Nmap was successfully used to scan the Metasploitable 2 lab machine, identify open TCP ports, detect services, and attempt operating system identification. These activities demonstrate the importance of network discovery during security assessments.
