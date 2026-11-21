# DNS, HTTP and HTTPS

## 1. Introduction

DNS, HTTP and HTTPS are important protocols used for communication over the internet.

- DNS converts domain names into IP addresses.
- HTTP is used to transfer data between web browsers and web servers.
- HTTPS provides secure communication using encryption.

## 2. Domain Name System (DNS)

DNS stands for Domain Name System.

It translates human-readable domain names into IP addresses that computers use to communicate.

### Example

When a user enters:

`www.google.com`

The DNS system finds the corresponding IP address of the server.

### How DNS Works

1. User enters a domain name in the browser.
2. Browser checks its local DNS cache.
3. If the address is not cached, a DNS query is sent to a DNS resolver.
4. The resolver finds the corresponding IP address.
5. The IP address is returned to the browser.
6. The browser connects to the destination server.

### Common DNS Record Types

| Record | Purpose |
|---|---|
| A | Maps a domain to an IPv4 address |
| AAAA | Maps a domain to an IPv6 address |
| CNAME | Creates an alias for another domain |
| MX | Identifies mail servers |
| NS | Identifies authoritative name servers |
| TXT | Stores text information, often used for verification |

### DNS Port

- UDP Port 53: Commonly used for DNS queries.
- TCP Port 53: Used for certain DNS operations, including zone transfers and responses requiring TCP.

## 3. Hypertext Transfer Protocol (HTTP)

HTTP stands for Hypertext Transfer Protocol.

It is an application-layer protocol used for communication between web clients and web servers.

### Features of HTTP

- Transfers web pages and other resources.
- Uses a request-response communication model.
- Does not provide encryption by itself.
- Commonly uses TCP port 80.

### HTTP Request Methods

| Method | Purpose |
|---|---|
| GET | Retrieves data from a server |
| POST | Sends data to a server |
| PUT | Creates or replaces a resource |
| DELETE | Deletes a resource |
| PATCH | Partially updates a resource |

### HTTP Status Codes

| Status Code | Meaning |
|---|---|
| 200 | OK |
| 301 | Moved Permanently |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

## 4. Hypertext Transfer Protocol Secure (HTTPS)

HTTPS stands for Hypertext Transfer Protocol Secure.

It is the secure version of HTTP. It uses TLS (Transport Layer Security) to protect communication between a browser and a web server.

### Features of HTTPS

- Encrypts communication between client and server.
- Protects data from being easily read during transmission.
- Helps verify server identity through digital certificates.
- Provides data integrity.
- Commonly uses TCP port 443.

### How HTTPS Works

1. Browser connects to the web server.
2. Server presents its digital certificate.
3. Browser verifies the certificate.
4. Client and server perform a TLS handshake.
5. Secure encryption keys are established.
6. Encrypted communication begins.

## 5. Difference Between HTTP and HTTPS

| HTTP | HTTPS |
|---|---|
| Hypertext Transfer Protocol | Hypertext Transfer Protocol Secure |
| Does not encrypt communication | Uses TLS encryption |
| Commonly uses port 80 | Commonly uses port 443 |
| Less secure for sensitive data | Protects data during transmission |
| Does not use TLS certificates | Uses digital certificates |

## 6. DNS vs HTTP vs HTTPS

| Protocol | Main Function | Default Port |
|---|---|---|
| DNS | Resolves domain names | 53 |
| HTTP | Transfers web resources | 80 |
| HTTPS | Securely transfers web resources | 443 |

## 7. Useful Linux Commands

### Check DNS Resolution

```bash
nslookup google.com
```

### Check Domain Information

```bash
dig google.com
```

### Test HTTP Connection

```bash
curl -I http://example.com
```

### Test HTTPS Connection

```bash
curl -I https://example.com
```

### Check Network Connectivity

```bash
ping -c 4 8.8.8.8
```

## 8. Importance in Cybersecurity

Understanding DNS, HTTP and HTTPS is important for cybersecurity professionals.

- DNS analysis helps identify suspicious domain lookups.
- HTTP analysis helps inspect web requests and responses.
- HTTPS protects sensitive information during transmission.
- DNS monitoring can help detect malicious domains.
- HTTPS certificate verification helps identify certificate-related security issues.
- Network traffic analysis helps investigate suspicious communication.

### Common Security Threats

- **DNS Spoofing:** Providing false DNS information to redirect users.
- **DNS Tunneling:** Using DNS queries and responses to transfer data covertly.
- **HTTP Interception:** Intercepting unencrypted HTTP communication.
- **Man-in-the-Middle Attack:** An attacker attempts to intercept or modify communication between two parties.

## 9. Conclusion

DNS, HTTP and HTTPS are essential protocols for internet communication. DNS helps locate servers, HTTP transfers web resources, and HTTPS protects communication using TLS encryption.

Understanding these protocols helps cybersecurity professionals analyze network traffic, identify suspicious activities and protect web communication.
