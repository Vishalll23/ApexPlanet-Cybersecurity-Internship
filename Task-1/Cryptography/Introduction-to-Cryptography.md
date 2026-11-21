# Introduction to Cryptography

## 1. Introduction

Cryptography is the technique of protecting information by converting readable data into an unreadable format so that only authorized users can access it.

It plays an important role in cybersecurity by protecting sensitive information during storage and communication.

## 2. Important Cryptography Terms

| Term | Meaning |
|---|---|
| Plaintext | Original readable information |
| Ciphertext | Encrypted, unreadable information |
| Encryption | Process of converting plaintext into ciphertext |
| Decryption | Process of converting ciphertext back into plaintext |
| Key | Value used by an encryption or decryption algorithm |
| Cipher | Algorithm used for encryption and decryption |

### Example

Original Message (Plaintext):

`HELLO`

Encrypted Message (Ciphertext):

`KHOOR`

In this simple Caesar cipher example, each letter is shifted three positions forward.

## 3. Types of Cryptography

Cryptography is mainly divided into three categories:

1. Symmetric-key cryptography
2. Asymmetric-key cryptography
3. Hash functions

## 4. Symmetric-Key Cryptography

Symmetric encryption uses the same secret key for both encryption and decryption.

### How It Works

1. Sender enters the original message.
2. Encryption algorithm uses a secret key.
3. Message is converted into ciphertext.
4. Receiver uses the same secret key.
5. Original message is recovered through decryption.

### Example Algorithms

- AES (Advanced Encryption Standard)
- DES (Data Encryption Standard)
- 3DES (Triple DES)

AES is widely used for protecting sensitive information.

### Advantages

- Fast encryption and decryption.
- Suitable for large amounts of data.
- Requires less computational power than many asymmetric methods.

### Disadvantages

- Secret key must be shared securely.
- Key management becomes difficult when many users communicate.

## 5. Asymmetric-Key Cryptography

Asymmetric encryption uses two mathematically related keys:

- **Public Key:** Can be shared with others.
- **Private Key:** Must be kept secret by its owner.

Data encrypted using the recipient's public key can generally be decrypted using the corresponding private key.

### How It Works

1. Receiver generates a public and private key pair.
2. Receiver shares the public key.
3. Sender encrypts the message using the receiver's public key.
4. Receiver decrypts the message using the private key.

### Example Algorithms

- RSA
- ECC (Elliptic Curve Cryptography)
- ElGamal

### Advantages

- Supports secure key exchange.
- Private keys do not need to be shared.
- Supports digital signatures.

### Disadvantages

- Generally slower than symmetric encryption.
- Requires more computational resources.
- Needs proper public-key verification.

## 6. Difference Between Symmetric and Asymmetric Cryptography

| Symmetric Cryptography | Asymmetric Cryptography |
|---|---|
| Uses one shared secret key | Uses a public-private key pair |
| Faster | Generally slower |
| Key sharing must be secured | Public key can be shared |
| Suitable for bulk data encryption | Useful for key exchange and digital signatures |
| Example: AES | Example: RSA, ECC |

## 7. Real-World Applications of Cryptography

Cryptography is used in many areas:

- Online banking and financial transactions.
- Secure websites using HTTPS.
- Password and sensitive data protection.
- Secure messaging applications.
- Digital signatures and certificates.
- Secure communication between servers.

## 8. Importance in Cybersecurity

Cryptography helps achieve important security objectives:

- **Confidentiality:** Prevents unauthorized users from reading information.
- **Integrity:** Helps detect unauthorized changes to data.
- **Authentication:** Helps verify identities.
- **Non-repudiation:** Digital signatures can provide evidence of origin and help prevent denial of signed actions.

## 9. Conclusion

Cryptography is an essential part of modern cybersecurity. Symmetric and asymmetric encryption protect information, secure communication and support authentication. Understanding these concepts provides a foundation for learning hashing, digital signatures, certificates and TLS.
