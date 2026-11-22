# AES-256 Encryption and Decryption Using OpenSSL

## 1. Objective
To understand symmetric encryption and decryption using the AES-256-CBC algorithm with OpenSSL.

## 2. Introduction
AES (Advanced Encryption Standard) is a symmetric encryption algorithm. It uses the same secret key to encrypt and decrypt data.

AES-256 uses a 256-bit key and is widely used to protect sensitive information.

## 3. Tools Used
- Kali Linux
- OpenSSL
- Terminal

## 4. Practical Implementation

### Step 1: Create a Sample File

```bash
echo "This is my cybersecurity practical file" > secret.txt
```

### Step 2: Encrypt the File

```bash
openssl enc -aes-256-cbc -salt -pbkdf2 -in secret.txt -out secret.enc
```

A password was entered to protect the encrypted file.

### Step 3: Decrypt the File

```bash
openssl enc -aes-256-cbc -d -pbkdf2 -in secret.enc -out decrypted.txt
```

The same password was entered to decrypt the file.

### Step 4: Verify the Decrypted Content

```bash
cat decrypted.txt
```

**Output:**
```text
This is my cybersecurity practical file
```

## 5. Understanding the Commands

| Command / Option | Purpose |
|---|---|
| `openssl enc` | Performs encryption or decryption |
| `-aes-256-cbc` | Selects AES-256-CBC algorithm |
| `-salt` | Adds a random salt during encryption |
| `-pbkdf2` | Uses PBKDF2 for password-based key derivation |
| `-in` | Specifies input file |
| `-out` | Specifies output file |
| `-d` | Enables decryption |

## 6. Result
Successfully encrypted a text file using AES-256-CBC and decrypted it using the same password. The original content was recovered successfully.

## 7. Learning Outcomes
- Understood symmetric encryption.
- Learned the working of AES-256-CBC.
- Practiced file encryption and decryption using OpenSSL.
- Understood the purpose of salt and PBKDF2.
- Verified encrypted data by recovering the original content.

## 8. Screenshots
Screenshots of the encryption and decryption process are available in:

`Task-1/Cryptography/Screenshots/`

- `08-AES-Encryption.png`
- `09-AES-Decryption.png`

## 9. Conclusion
This practical demonstrated how OpenSSL can protect files using AES-256 encryption. It also showed how the original data can be recovered securely using the correct password and matching encryption settings.
