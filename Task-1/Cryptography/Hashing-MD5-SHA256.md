# Hashing: MD5 and SHA-256

## 1. Introduction

Hashing is a process of converting input data into a fixed-length string of characters using a mathematical algorithm called a hash function.

It is commonly used in cybersecurity to verify data integrity and securely store password representations.

Unlike encryption, hashing is designed to be a one-way process. A hash cannot normally be reversed to recover the original input.

## 2. Important Features of Hashing

- Produces a fixed-length output for a given algorithm.
- The same input produces the same hash.
- A small change in input produces a significantly different hash.
- It is designed to be computationally difficult to reverse.
- It helps detect changes in files and data.

## 3. What is MD5?

MD5 stands for Message Digest Algorithm 5.

- Produces a 128-bit hash.
- Usually represented as a 32-character hexadecimal string.
- Commonly used in older checksum applications.
- Has known collision vulnerabilities.
- Not recommended for password storage or security-sensitive integrity verification.

Example:

Input:
`hello`

MD5 Hash:
`5d41402abc4b2a76b9719d911017c592`

## 4. What is SHA-256?

SHA-256 stands for Secure Hash Algorithm 256-bit.

- Part of the SHA-2 family.
- Produces a 256-bit hash.
- Usually represented as a 64-character hexadecimal string.
- Widely used for integrity verification and security applications.
- More secure against collision attacks than MD5.

Example:

Input:
`hello`

SHA-256 Hash:
`2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824`

## 5. Difference Between MD5 and SHA-256

| MD5 | SHA-256 |
|---|---|
| Produces 128-bit hash | Produces 256-bit hash |
| 32 hexadecimal characters | 64 hexadecimal characters |
| Faster but outdated | More secure for general integrity checking |
| Vulnerable to collision attacks | No practical collision attack is currently known |
| Not suitable for security-sensitive use | Widely used for integrity verification |

## 6. Hashing vs Encryption

| Hashing | Encryption |
|---|---|
| Designed as a one-way process | Reversible using the correct key |
| Does not require a decryption key | Requires a decryption key |
| Used for integrity verification | Used for confidentiality |
| Example: SHA-256 | Example: AES |

## 7. Practical Exercise Using Kali Linux

The following commands can be used to generate MD5 and SHA-256 hashes.

### Step 1: Create a sample file

```bash
echo "Hello Cybersecurity" > sample.txt
```

### Step 2: Generate MD5 hash

```bash
md5sum sample.txt
```

### Step 3: Generate SHA-256 hash

```bash
sha256sum sample.txt
```

### Step 4: Modify the file

```bash
echo "Modified content" > sample.txt
```

### Step 5: Generate hashes again

```bash
md5sum sample.txt
sha256sum sample.txt
```

### Observation

After modifying the file, the generated hashes will change significantly.

This demonstrates how hashing can help detect changes in data.

## 8. Real-World Applications

Hashing is used in:

- File integrity verification.
- Digital signatures.
- Password storage using secure password-hashing algorithms.
- Software download verification.
- Blockchain technology.
- Security monitoring and forensic investigations.

**Important:** Passwords should be stored using dedicated password-hashing algorithms such as Argon2id, bcrypt, scrypt or PBKDF2 with unique salts. Plain MD5 and SHA-256 are not suitable for password storage.

## 9. Conclusion

Hashing is an important cybersecurity technique used to verify data integrity. MD5 is considered outdated due to collision vulnerabilities, while SHA-256 provides stronger security for general-purpose hashing and integrity verification.
