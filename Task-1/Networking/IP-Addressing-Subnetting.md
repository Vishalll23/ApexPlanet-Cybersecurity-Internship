# IP Addressing and Subnetting

## 1. Introduction

IP addressing is a method used to identify devices on a network. Every device connected to an IP network requires an IP address for communication.

## 2. Types of IP Addresses

### IPv4

- Uses 32-bit addresses.
- Written in four decimal octets.
- Example: `192.168.1.10`
- Each octet ranges from 0 to 255.

### IPv6

- Uses 128-bit addresses.
- Written in hexadecimal format.
- Example: `2001:db8::1`
- Developed to overcome IPv4 address limitations.

## 3. Public and Private IP Addresses

**Public IP:** Used to identify a network on the internet.

**Private IP:** Used for communication within local networks.

Common private IPv4 ranges:

| Class | Private IP Range |
|---|---|
| A | 10.0.0.0 – 10.255.255.255 |
| B | 172.16.0.0 – 172.31.255.255 |
| C | 192.168.0.0 – 192.168.255.255 |

## 4. Static and Dynamic IP

- **Static IP:** Manually assigned and generally remains unchanged.
- **Dynamic IP:** Automatically assigned, commonly through DHCP.

## 5. Subnet Mask

A subnet mask separates the network portion and host portion of an IPv4 address.

Example:

- IP Address: `192.168.1.10`
- Subnet Mask: `255.255.255.0`
- CIDR Notation: `/24`

## 6. CIDR Notation

CIDR stands for Classless Inter-Domain Routing.

It represents the network prefix using a slash followed by the number of network bits.

Examples:

- `/8` = 255.0.0.0
- `/16` = 255.255.0.0
- `/24` = 255.255.255.0

## 7. Basic Subnetting Example

Given:

- Network: `192.168.1.0/24`
- Subnet Mask: `255.255.255.0`
- Total addresses: 256
- Usable host addresses: 254
- Network Address: `192.168.1.0`
- Broadcast Address: `192.168.1.255`
- Usable Host Range: `192.168.1.1 – 192.168.1.254`

## 8. Difference Between Classful and Classless Addressing

| Classful Addressing | Classless Addressing |
|---|---|
| Uses fixed network classes | Uses variable prefix lengths |
| Less flexible | More flexible |
| Can waste IP addresses | Uses IP addresses efficiently |
| Based on Classes A, B and C | Uses CIDR notation |

## 9. Useful Linux Commands

```bash
ip addr
ip route
ip -br a
hostname -I
ping 192.168.1.1
```

These commands help inspect network interfaces, IP addresses, routing information and connectivity.

## 10. Importance in Cybersecurity

Understanding IP addressing and subnetting helps security professionals:

- Identify devices on a network.
- Understand network boundaries.
- Configure firewall rules.
- Analyze network traffic.
- Identify unusual network communication.

## Conclusion

IP addressing and subnetting are essential networking concepts. They help organize networks, manage communication and support network security.
