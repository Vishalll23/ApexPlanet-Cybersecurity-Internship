# Task 1 – Lab Environment Setup

## 1. Objective
The objective of this practical was to create an isolated cybersecurity lab environment using Kali Linux and Metasploitable 2 virtual machines in Oracle VirtualBox.

## 2. Tools and Technologies Used
- Oracle VirtualBox 7.2.12
- Kali Linux
- Metasploitable 2
- Host-Only Network Adapter
- Windows Host Machine

## 3. Lab Environment Configuration

Two virtual machines were configured for practical cybersecurity exercises.

| Virtual Machine | Purpose | IP Address |
|---|---|---|
| Kali Linux | Testing and security assessment machine | 192.168.56.101 |
| Metasploitable 2 | Vulnerable target machine | 192.168.56.102 |

**Network Configuration:**
- Network Mode: Host-Only Adapter
- Network Adapter: VirtualBox Host-Only Ethernet Adapter
- Network Subnet: 192.168.56.0/24

Kali Linux was configured with two network adapters:
- Adapter 1: NAT
- Adapter 2: Host-Only

Metasploitable 2 was configured with:
- Adapter 1: Host-Only
- Other adapters: Disabled

## 4. Installation and Configuration Steps

1. Installed and configured Oracle VirtualBox.
2. Prepared the Kali Linux virtual machine.
3. Downloaded the Metasploitable 2 archive.
4. Extracted the archive and located the VMDK virtual disk.
5. Created a new virtual machine named Metasploitable 2.
6. Attached the existing Metasploitable virtual disk.
7. Configured the Host-Only network adapter.
8. Connected both virtual machines to the same Host-Only network.
9. Started both virtual machines and verified their network configurations.

## 5. Network Configuration Verification

### Kali Linux

Command used:

```bash
ip -br a
```

Observed Host-Only interface:

- Interface: eth1
- IP Address: 192.168.56.101/24

### Metasploitable 2

Command used:

```bash
ifconfig
```

Observed interface:

- Interface: eth0
- IP Address: 192.168.56.102
- Subnet Mask: 255.255.255.0

## 6. Connectivity Testing

To verify communication between Kali Linux and Metasploitable 2, the following command was executed from Kali Linux:

```bash
ping -c 4 192.168.56.102
```

**Observed Result:**

- Packets Transmitted: 4
- Packets Received: 4
- Packet Loss: 0%
- Average Response Time: Approximately 4.992 ms

The successful ping test confirmed that both virtual machines can communicate through the Host-Only network.

## 7. Security Considerations

- Metasploitable 2 is an intentionally vulnerable operating system.
- It is kept isolated using Host-Only networking.
- NAT and Bridged networking are disabled for Metasploitable 2.
- All future security testing will be performed only within the authorized lab environment.

## 8. Learning Outcomes

- Understood virtual machine configuration in VirtualBox.
- Learned how to configure Host-Only networking.
- Understood the difference between NAT and Host-Only networking.
- Practised identifying IP addresses using Linux commands.
- Successfully established communication between two virtual machines.
- Prepared an isolated environment for future vulnerability assessment and security testing.

## 9. Conclusion

Successfully configured a cybersecurity practice lab using Kali Linux and Metasploitable 2. Both virtual machines were connected through an isolated Host-Only network, and connectivity was verified through a successful ping test.

This environment will be used for further practical exercises involving network reconnaissance, vulnerability assessment, and cybersecurity tools.
