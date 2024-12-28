---
title: "🎯How to Set File Permissions in Linux.🎉"
datePublished: Sat Dec 28 2024 18:00:53 GMT+0000 (Coordinated Universal Time)
cuid: cm58hmgyl003109le9npgducm
slug: how-to-set-file-permissions-in-linux
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1735315310591/538a3ae1-55ba-479e-b6e6-7a73e8121b28.png
tags: ubuntu, linux, devops, os

---

## **1\. File Permission Basics**

Each file and directory in Linux has three permission categories:

* **Owner (u)**: The user who owns the file.
    
* **Group (g)**: Users in the group associated with the file.
    
* **Others (o)**: Everyone else who can access the system.
    

Permissions control three operations:

* **Read (r)**: View the contents of the file or list a directory.
    
* **Write (w)**: Modify the file or add/delete files in a directory.
    
* **Execute (x)**: Run a file as a program or access a directory.
    

## **2\. Permission Syntax**

To see permissions, use:

```plaintext
ls -l
```

Output example:

```plaintext
-rwxr-xr-- 1 user group  4096 Dec 27 12:00 file.txt
```

### Breaking it down:

1. `-rwxr-xr--`: Permission string:
    
    * First character: File type:
        
        * `-`: Regular file
            
        * `d`: Directory
            
        * `l`: Symbolic link
            
    * Next 9 characters: Permissions in three groups of three:
        
        * `rwx`: Owner can read, write, and execute.
            
        * `r-x`: Group can read and execute, but not write.
            
        * `r--`: Others can only read.
            
2. `1`: Number of links to the file.
    
3. `user`: File owner.
    
4. `group`: Group associated with the file.
    
5. `4096`: File size in bytes.
    
6. `Dec 27 12:00`: Last modified date.
    
7. `file.txt`: File name.
    

Linux file permissions are essential for securing files and directories, determining who can read, write, or execute them. Here's an **in-depth explanation** of Linux file permissions:

## **3\. Modifying File Permissions**

Permissions can be changed using the `chmod` command.

### **Symbolic Mode**

Assign permissions using letters:

* `u`: Owner
    
* `g`: Group
    
* `o`: Others
    
* `a`: All (u, g, o)
    

Operators:

* `+`: Add permission
    
* `-`: Remove permission
    
* `=`: Set specific permission
    

Examples:

```plaintext
chmod u+x file.txt               # Add execute permission for the owner.
chmod g-w file.txt               # Remove write permission for the group.
chmod o=r file.txt               # Set read-only permission for others.
chmod a+x script.sh              # Add execute permission for everyone.
```

### **Numeric Mode**

Assign permissions using octal values:

* **4**: Read (`r`)
    
* **2**: Write (`w`)
    
* **1**: Execute (`x`)
    
* **0**: No permission
    

Combine values for each group:

* **7 (4+2+1)**: Read, write, and execute.
    
* **6 (4+2)**: Read and write.
    
* **5 (4+1)**: Read and execute.
    
* **4**: Read-only.
    

Examples:

```plaintext
chmod 755 file.txt               # Owner: rwx, Group: r-x, Others: r-x
chmod 644 file.txt               # Owner: rw-, Group: r--, Others: r--
chmod 700 secret                 # Owner: rwx, Group: ---, Others: ---
```

---

## **4\. Ownership**

File ownership is managed with two identifiers:

* **User (owner)**: Specifies the user who owns the file.
    
* **Group**: Specifies the group associated with the file.
    

### Change Ownership

Use the `chown` command:

```plaintext
chown user file.txt                      # Change owner to 'user'.
chown user:group file.txt                # Change owner to 'user' and group to 'group'.
chown :group file.txt                    # Change group only.
```

Example:

```plaintext
sudo chown alice:developers report.txt
```

## **5\. Default Permissions**

### **Umask**

The **umask** (user mask) determines default permissions for newly created files/directories.  
Default permissions:

* File: `666` (read and write for all).
    
* Directory: `777` (read, write, and execute for all).
    

Umask subtracts permissions:

```plaintext
umask 022                 # Removes write permission for group and others.
```

### View or set `umask`:

```plaintext
umask                     # View current umask.
umask 027                 # Set umask to 027.
```

## **6\. File Permission Commands Summary**

| **Command** | **Description** |
| --- | --- |
| `ls -l` | View file permissions. |
| `chmod` | Change file permissions. |
| `chown` | Change file ownership. |
| `chgrp` | Change file group. |
| `umask` | Set default permissions. |
| `setfacl` | Modify ACL permissions. |
| `getfacl` | View ACL permissions. |

## **7\. Practical Examples**

1. Make a script executable:
    
    ```plaintext
    chmod +x script.sh
    ```
    
2. Restrict directory access to the owner:
    
    ```plaintext
    chmod 700 secret
    ```
    
3. Allow a user to edit a file without changing ownership:
    
    ```plaintext
    setfacl -m u:username:rw file.txt
    ```
    
    ## **8\. Security Best Practices**
    
    * Use **least privilege**: Assign only the permissions needed for a task.
        
    * Regularly audit permissions with `ls -l` .
        
    * Avoid using `777` permissions as it grants unrestricted access to all.
        
    * Secure sensitive files with `chmod 600` or `chmod 700`.