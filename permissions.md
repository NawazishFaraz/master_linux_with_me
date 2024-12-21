# Linux Permissions vs ACLs

## Overview

In Linux, both **Permissions** and **Access Control Lists (ACLs)** are used to manage file and directory access. While permissions provide basic control over file access, ACLs offer more granular and detailed access management.

---

## 1. Permissions

### Definition
Permissions in Linux define the access control for a file or directory for three categories:
- **User (Owner)**
- **Group**
- **Others**

### Permission Types
- `r`: Read
- `w`: Write
- `x`: Execute

# Access Control Lists (ACLs) in Linux

## Overview

**Access Control Lists (ACLs)** provide a more granular and flexible method of defining file access permissions than traditional Linux file permissions. ACLs allow you to specify permissions for multiple users and groups on a single file or directory.

---

## 2. What Are ACLs?

ACLs enable more detailed control over file access by allowing you to define permissions for individual users or groups, beyond the standard owner, group, and others permissions.

### Key Features:
- **Multiple Users/Groups**: Set permissions for specific users or groups.
- **Fine-Grained Control**: Assign read, write, and execute permissions to each user or group independently.
- **Default ACLs**: ACLs can be inherited by new files and directories created within a directory.

---

## . Managing ACLs

### Check ACLs:
To view the ACLs of a file or directory, use the `getfacl` command:
```bash
getfacl myfile.txt
```

Set ACL: You can set an ACL using the setfacl command.
```bash
setfacl -m u:username:rwx myfile.txt  # Give user "username" read, write, and execute permissions
```


