# Digital Certificates and SSL/TLS

## 1. Introduction

Digital certificates and SSL/TLS are important technologies used to secure communication over the internet.

They help verify the identity of websites and protect information exchanged between clients and servers.

## 2. What is a Digital Certificate?

A digital certificate is an electronic document used to verify the identity of a website, server or organization.

It is issued and digitally signed by a trusted Certificate Authority (CA).

### Information in a Digital Certificate

A digital certificate generally contains:

- Website or subject name.
- Public key.
- Certificate issuer.
- Validity period.
- Serial number.
- Digital signature of the Certificate Authority.

## 3. What is a Certificate Authority (CA)?

A Certificate Authority is a trusted organization that issues and signs digital certificates.

### Functions of a CA

- Verifies the identity of certificate applicants according to its validation process.
- Issues digital certificates.
- Digitally signs certificates.
- Helps browsers establish trust in website identities.
- Supports certificate revocation.

Examples of Certificate Authorities include Let's Encrypt, DigiCert and GlobalSign.

## 4. What is SSL?

SSL stands for Secure Sockets Layer.

It was an earlier security protocol designed to protect communication over networks.

SSL is now outdated and insecure. Modern secure web communication uses TLS instead.

## 5. What is TLS?

TLS stands for Transport Layer Security.

It is a cryptographic protocol that protects communication between applications over a network.

### Main Features of TLS

- **Confidentiality:** Encrypts transmitted data.
- **Integrity:** Helps detect unauthorized changes to data.
- **Authentication:** Helps verify the server's identity using digital certificates.

## 6. Difference Between SSL and TLS

| SSL | TLS |
|---|---|
| Older security protocol | Modern security protocol |
| Outdated and insecure | Provides stronger security |
| No longer recommended | Used in modern secure communication |
| Earlier versions include SSL 2.0 and SSL 3.0 | Modern versions include TLS 1.2 and TLS 1.3 |

## 7. How HTTPS Uses TLS

HTTPS uses TLS to secure communication between a web browser and a web server.

### Basic Working Process

1. Browser connects to a website.
2. Server sends its digital certificate.
3. Browser verifies the certificate and its trust chain.
4. Client and server perform a TLS handshake.
5. They establish shared encryption keys.
6. Secure encrypted communication begins.

## 8. What is a TLS Handshake?

A TLS handshake is the process through which a client and server establish the parameters and keys needed for secure communication.

In TLS 1.3, the simplified process includes:

1. **ClientHello:** Client sends supported TLS versions, cryptographic options and key-share information.
2. **ServerHello:** Server selects the security parameters and responds with its key-share information.
3. **Certificate and Authentication:** Server provides its certificate and proves possession of the corresponding private key.
4. **Key Establishment:** Both sides derive shared session keys.
5. **Secure Communication:** Encrypted application data is exchanged.

## 9. Types of Digital Certificates

| Certificate Type | Purpose |
|---|---|
| Domain Validated (DV) | Verifies control over a domain |
| Organization Validated (OV) | Includes organization identity validation |
| Extended Validation (EV) | Uses a more extensive organization validation process |
| Wildcard Certificate | Secures a domain and its subdomains at one level |
| Multi-Domain Certificate | Secures multiple domain names |

## 10. Useful Linux Commands

### Check HTTPS Response

```bash
curl -I https://example.com
```

### Display Certificate Information

```bash
openssl s_client -connect example.com:443 -servername example.com
```

### Display Certificate Details

```bash
openssl s_client -connect example.com:443 -servername example.com </dev/null 2>/dev/null | openssl x509 -noout -subject -issuer -dates
```

### Check OpenSSL Version

```bash
openssl version
```

## 11. Importance in Cybersecurity

Digital certificates and TLS are important because they:

- Protect sensitive information during transmission.
- Help verify website identities.
- Reduce the risk of communication interception.
- Protect online banking and payment transactions.
- Support secure communication between applications and servers.

## 12. Conclusion

Digital certificates help establish trust in online identities, while TLS protects communication through encryption, authentication and integrity checks.

Together, they form an essential part of modern internet security.
