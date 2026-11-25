# Wireshark – Network Traffic Analysis

## 1. Objective
To capture and analyze network packets using Wireshark and understand ICMP, DNS, HTTP, and HTTPS traffic.

## 2. Introduction
Wireshark is an open-source network protocol analyzer used to capture and inspect network traffic.

It helps cybersecurity professionals understand network communication, troubleshoot connectivity issues, and investigate suspicious activities.

## 3. Tools Used
- Kali Linux
- Wireshark 4.6.6
- VirtualBox
- Metasploitable 2 (for ICMP practical)

## 4. Practical Implementation

### Practical 1: ICMP Packet Capture

**Objective:** Capture ICMP Echo Request and Echo Reply packets.

Command used:

```bash
ping -c 5 192.168.56.102
```

Wireshark interface: `eth1`

Display filter:

```text
icmp
```

**Observation:**
- Source IP: `192.168.56.101`
- Destination IP: `192.168.56.102`
- Echo Request packets were sent from Kali.
- Echo Reply packets were received from Metasploitable.

### Practical 2: DNS Traffic Analysis

**Objective:** Observe how DNS resolves domain names into IP addresses.

Command used:

```bash
nslookup google.com
```

Wireshark interface: `eth0`

Display filter:

```text
dns
```

**Observation:**
- Source IP: `10.0.2.15`
- Destination IP: `192.168.0.1`
- DNS queries and responses were captured.
- A records were used for IPv4 address resolution.
- AAAA records were used for IPv6 address resolution.

### Practical 3: HTTP Traffic Analysis

**Objective:** Observe unencrypted HTTP communication.

Command used:

```bash
curl -4 -v --max-time 20 http://neverssl.com/
```

Display filter:

```text
http
```

**Observation:**
- HTTP communication was successfully tested.
- HTTP request and response packets were inspected in Wireshark.
- HTTP does not provide TLS encryption.

### Practical 4: HTTPS Traffic Analysis

**Objective:** Observe encrypted HTTPS communication.

Command used:

```bash
curl -I https://example.com
```

Wireshark display filter:

```text
tls
```

**Observation:**
- HTTPS connection was successful.
- HTTP response returned status `200`.
- TLS traffic was captured.
- Application data transmitted through HTTPS is protected by TLS encryption.

## 5. Important Wireshark Display Filters

| Filter | Purpose |
|---|---|
| `icmp` | Displays ICMP packets |
| `dns` | Displays DNS packets |
| `http` | Displays HTTP packets |
| `tls` | Displays TLS traffic |
| `tcp` | Displays TCP packets |
| `udp` | Displays UDP packets |
| `ip.addr == 192.168.56.102` | Filters traffic involving a specific IP |

## 6. HTTP vs HTTPS Comparison

| HTTP | HTTPS |
|---|---|
| Uses port 80 by default | Uses port 443 by default |
| No TLS encryption | Uses TLS encryption |
| Application data is not protected by TLS | Application data is protected by TLS |
| Suitable for understanding plaintext web traffic | Used for secure web communication |

## 7. Learning Outcomes
- Learned how to capture live network packets.
- Understood ICMP communication.
- Analyzed DNS queries and responses.
- Observed HTTP communication.
- Understood TLS-based HTTPS protection.
- Practiced Wireshark display filters.

## 8. Screenshots
Practical screenshots are stored in:

`Task-1/Tools/Screenshots/`

The screenshots cover:
- ICMP packet capture
- DNS traffic analysis
- HTTP traffic analysis
- HTTPS traffic analysis

## 9. Conclusion
Wireshark was successfully used to capture and analyze different types of network traffic. The practical exercises helped demonstrate how devices communicate over networks and how TLS protects web communication.
