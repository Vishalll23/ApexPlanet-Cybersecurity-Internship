# OSI and TCP/IP Models

## 1. Introduction

Computer networks use communication models to understand how data travels between devices.

Two important networking models are:

- **OSI Model:** Open Systems Interconnection Model.
- **TCP/IP Model:** Transmission Control Protocol / Internet Protocol Model.

These models divide network communication into different layers. Each layer performs a specific function and works with the layers above and below it.

## 2. OSI Model

The OSI model is a conceptual networking model developed by ISO. It consists of seven layers that explain how data moves from one device to another.

### Seven Layers of the OSI Model

| Layer | Name | Main Function | Examples |
|---|---|---|---|
| 7 | Application | Provides network services to applications | HTTP, FTP, DNS, SMTP |
| 6 | Presentation | Data translation, encryption and compression | JPEG, ASCII, encryption |
| 5 | Session | Establishes, manages and terminates sessions | RPC, NetBIOS |
| 4 | Transport | End-to-end communication and reliability | TCP, UDP |
| 3 | Network | Logical addressing and routing | IP, ICMP |
| 2 | Data Link | Frame delivery and MAC addressing | Ethernet, Wi-Fi |
| 1 | Physical | Transmits raw bits through physical media | Cables, signals, hubs |

### Explanation of Each Layer

**Layer 7 – Application Layer**

- Provides network services to applications.
- Allows users to access network resources.
- Examples: HTTP, HTTPS, FTP and DNS.

**Layer 6 – Presentation Layer**

- Converts data into a suitable format.
- Handles encryption, decryption and compression.
- Example: Data encoding and encryption.

**Layer 5 – Session Layer**

- Establishes communication sessions between devices.
- Maintains and terminates sessions.
- Example: Session management in network applications.

**Layer 4 – Transport Layer**

- Provides end-to-end data delivery.
- Handles segmentation and reassembly.
- Uses TCP and UDP protocols.
- Uses port numbers to identify applications.

**Layer 3 – Network Layer**

- Handles logical addressing and routing.
- Determines the path for data packets.
- Example: IPv4 and IPv6.

**Layer 2 – Data Link Layer**

- Transfers data between devices on the same local network.
- Uses MAC addresses.
- Performs framing and error detection.
- Example: Ethernet.

**Layer 1 – Physical Layer**

- Transmits raw binary bits (0s and 1s).
- Defines cables, connectors and transmission signals.
- Example: Ethernet cables and fiber-optic cables.

## 3. TCP/IP Model

The TCP/IP model is a practical networking model used for communication over the internet. It consists of four layers.

### Four Layers of the TCP/IP Model

| Layer | Main Function | Examples |
|---|---|---|
| Application | Provides network services and application communication | HTTP, HTTPS, DNS, FTP |
| Transport | Provides end-to-end communication | TCP, UDP |
| Internet | Handles IP addressing and routing | IPv4, IPv6, ICMP |
| Network Access | Handles local network communication and physical transmission | Ethernet, Wi-Fi |

### Explanation of Each Layer

**1. Application Layer**

- Provides services to user applications.
- Combines the functions of OSI Application, Presentation and Session layers.
- Examples: HTTP, HTTPS, DNS and FTP.

**2. Transport Layer**

- Provides communication between applications on different devices.
- Handles segmentation and port addressing.
- Uses TCP and UDP.

**3. Internet Layer**

- Handles logical addressing and packet routing.
- Transfers packets between different networks.
- Uses IP and ICMP protocols.

**4. Network Access Layer**

- Handles communication over the local network.
- Deals with MAC addressing and physical transmission.
- Uses technologies such as Ethernet and Wi-Fi.

## 4. Difference Between OSI and TCP/IP Models

| OSI Model | TCP/IP Model |
|---|---|
| Has 7 layers | Has 4 layers |
| Developed by ISO | Developed through DARPA research |
| Mainly a reference model | A practical protocol suite and model |
| Separates Session and Presentation layers | Includes their functions in Application layer |
| Separates Physical and Data Link layers | Combines them in Network Access layer |
| Helps understand network communication | Used in real-world internet communication |

## 5. OSI and TCP/IP Layer Mapping

| OSI Layers | TCP/IP Layers |
|---|---|
| Application | Application |
| Presentation | Application |
| Session | Application |
| Transport | Transport |
| Network | Internet |
| Data Link | Network Access |
| Physical | Network Access |

## 6. TCP vs UDP

TCP and UDP are transport layer protocols.

| TCP | UDP |
|---|---|
| Connection-oriented | Connectionless |
| Reliable data delivery | No delivery guarantee |
| Uses acknowledgements | Does not use acknowledgements by default |
| Maintains data order | Does not guarantee data order |
| Generally higher overhead | Generally lower overhead |
| Used in HTTPS, FTP and SSH | Used in DNS, VoIP and streaming applications |

## 7. TCP Three-Way Handshake

The TCP three-way handshake establishes a connection between a client and a server before data transfer.

### Three Steps

**Step 1: SYN**

The client sends a SYN packet to request a connection.

**Step 2: SYN-ACK**

The server responds with SYN-ACK to acknowledge the request.

**Step 3: ACK**

The client sends an ACK packet. The connection is now established.

### Handshake Diagram

```text
       CLIENT                 SERVER
          |                      |
          |------ SYN ---------->|
          |                      |
          |<---- SYN-ACK --------|
          |                      |
          |------- ACK -------->|
          |                      |
          |   CONNECTION READY  |
```

## 8. Common Network Protocols and Ports

| Protocol | Port Number | Purpose |
|---|---:|---|
| HTTP | 80 | Web communication |
| HTTPS | 443 | Secure web communication |
| FTP | 21 | File transfer control |
| SSH | 22 | Secure remote access |
| Telnet | 23 | Remote access without encryption |
| SMTP | 25 | Sending emails |
| DNS | 53 | Domain name resolution |
| DHCP | 67, 68 | Automatic IP assignment |
| POP3 | 110 | Receiving emails |
| IMAP | 143 | Email access and synchronization |

## 9. Importance of OSI and TCP/IP in Cybersecurity

Understanding these models helps cybersecurity professionals:

- Identify where network attacks occur.
- Analyze suspicious network traffic.
- Troubleshoot network communication.
- Understand firewall and packet-filtering operations.
- Monitor network protocols and ports.
- Investigate network-based security incidents.

Examples:

- **DDoS attacks:** Can target different network layers.
- **Port scanning:** Helps identify exposed services and ports.
- **Packet analysis:** Helps inspect network communication.
- **Application attacks:** Can target services operating at the application layer.

## 10. Useful Networking Commands

The following Linux commands help inspect network configuration and connectivity.

```bash
ip addr
ip route
ip -br a
ping -c 4 8.8.8.8
ss -tuln
```

## 11. Conclusion

The OSI and TCP/IP models are important foundations of computer networking. The OSI model explains communication through seven layers, while the TCP/IP model describes the practical architecture used for internet communication.

Understanding these models is essential for network troubleshooting, traffic analysis and cybersecurity operations.
