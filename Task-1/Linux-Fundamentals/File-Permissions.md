# Linux File Permissions and Ownership

## 1. Introduction

Linux is a multi-user operating system. File permissions help control who can read, write, or execute files and directories.

Permissions are important for maintaining system security and preventing unauthorized access.

## 2. Types of Permissions

Linux provides three basic permissions:

| Permission | Symbol | Numeric Value | Description |
|---|---|---:|---|
| Read | r | 4 | Allows reading a file |
| Write | w | 2 | Allows modifying a file |
| Execute | x | 1 | Allows executing a file |

## 3. Permission Categories

Permissions are assigned to three categories:

- **User (u):** Owner of the file.
- **Group (g):** Members of the assigned group.
- **Others (o):** All other users.

## 4. Understanding Linux Permissions

Example:

```text
-rwxr-xr--
```

| Part | Meaning |
|---|---|
| `-` | Regular file |
| `rwx` | Owner permissions |
| `r-x` | Group permissions |
| `r--` | Others permissions |

## 5. chmod Command

The `chmod` command is used to change file permissions.

Syntax:

```bash
chmod permissions filename
```

Examples:

```bash
chmod 755 file.txt
chmod 644 file.txt
chmod +x script.sh
chmod u+w file.txt
```

### Numeric Permission Calculation

For permission `755`:

- Owner: 4 + 2 + 1 = 7
- Group: 4 + 1 = 5
- Others: 4 + 1 = 5

Therefore, `755` means owner has read, write, and execute permissions, while group and others have read and execute permissions.

## 6. chown Command

The `chown` command changes file ownership.

Syntax:

```bash
sudo chown username filename
```

Example:

```bash
sudo chown vishal file.txt
```

To change both owner and group:

```bash
sudo chown username:groupname file.txt
```

## 7. Viewing Permissions

The following command displays file permissions and ownership:

```bash
ls -l
```

Example output:

```text
-rw-r--r-- 1 vishal vishal 0 Nov 21  file.txt
```

## 8. Security Importance

- Prevents unauthorized file access.
- Protects sensitive system files.
- Restricts execution of unauthorized scripts.
- Helps maintain proper access control.
- Supports Linux system security and administration.

## 9. Conclusion

Linux file permissions are an important part of operating system security. Commands such as `chmod`, `chown`, and `ls -l` help administrators manage file access and ownership effectively.

**Practical note:** Execute and verify commands in your own Kali Linux lab before marking them as completed.
