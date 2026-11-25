# Netcat – Network Testing

## 1. Objective
To use Netcat to establish a TCP connection and identify a service running on a remote host.

## 2. Introduction
Netcat (nc) is a networking utility used to read and write data over TCP and UDP connections. It is useful for network troubleshooting, connectivity testing and banner grabbing.

## 3. Lab Environment
- Kali Linux
- Metasploitable 2
- VirtualBox Host-Only Network
- Target IP: `192.168.56.102`
- Target port: `21` (FTP)

## 4. Practical – FTP Banner Grabbing

**Command used:**

```bash
nc -nv 192.168.56.102 21
```

**Steps performed:**
1. Started Kali Linux and Metasploitable 2.
2. Opened the Kali terminal.
3. Connected to the FTP service using Netcat.
4. Observed the FTP server welcome banner.
5. Closed the connection using `QUIT`.

**Observation:**

The Netcat connection was used to interact with the FTP service on the Metasploitable test machine and inspect its welcome banner.

## 5. Important Options

| Option | Purpose |
|---|---|
| `-n` | Disables DNS resolution |
| `-v` | Enables verbose output |

## 6. Learning Outcomes
- Learned the basic use of Netcat.
- Established a TCP connection to a remote service.
- Understood service banner grabbing.
- Learned how to test network connectivity using Netcat.

## 7. Screenshot
Screenshot stored in:

`Task-1/Tools/Screenshots/18-Netcat-FTP-Banner.png`

## 8. Conclusion
Netcat was used to connect to the FTP service running on the isolated Metasploitable lab machine. This practical demonstrated basic TCP connectivity testing and service banner identification.
