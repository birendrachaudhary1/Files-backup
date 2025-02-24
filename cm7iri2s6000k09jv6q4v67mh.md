---
title: "Module 4 - Linux Fundamentals🌀."
datePublished: Mon Feb 24 2025 07:54:30 GMT+0000 (Coordinated Universal Time)
cuid: cm7iri2s6000k09jv6q4v67mh
slug: module-4-linux-fundamentals
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1740292326341/d7c2abbf-eb5f-4751-91a5-6f0593e8ba0f.png
tags: ubuntu, linux, basics, linux-commands, linux-fundamentals

---

# **➡️Command Syntax.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740292876466/7d2424fc-4505-4135-b7f2-da4c02950b40.png align="center")

# ➡️**Files and directory permissions(chmod).**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740293548340/766e143e-6a59-46ea-8886-37bc1e7d0a62.png align="center")

### **how to remove or add permission?**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740293785312/97859252-04e2-4f91-879d-a0efb4c2fffd.png align="center")

# ➡️**Permissions using numeric mode.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740294058991/f80c3a44-dbce-4b53-aa37-8689b3e17f1b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740294175452/af84da9b-9b66-411c-bcc6-311e41a538d8.png align="center")

# ➡️File Ownership Commands(chown, chgrp).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740295502395/593b751c-7254-4502-8aa0-7710ded924c3.png align="center")

# ➡️Access Control List (ACL).

**What is ACL?**  
\- ACL provides an additional, more flexible permission mechanism for file systems. It is designed to assist with UNIX file permissions. ACL allows you to give permissions for any user or group to any disc resource.

**Use of ACL:**  
\- Think of a scenario in which a particular user is not a member of group created by you but still you want to give some read or write access, how can you do it without making user a member of group, here comes in pictures Access Control Lists, ACL helps us to do this trick.  
\- Basically, ACLs are used to make a flexible permission mechanism in Linux.  
\- From Linux man pages, ACLs are used to define more fine-grained discretionary access rights for files and directories.  
\- **Commands to assign and remove ACL permissions are:**  
**setfacl** and **getfacl**

## **List of commands for setting up ACL.**

### **Display the ACL of a file or directory:**

getfacl filename

### **Add or modify ACL entries:**

**For specific user:**  
setfacl -m u:username:permissions filename

**For a specific group:**  
setfacl -m g:groupname:permissions filename

## Remove a specific ACL entry:

### For a user:

setfacl -x u:username filename

### For a group:

setfacl -x g:groupname filename

### **Remove all ACL entries from a file or directory:**

setfacl -b filename

# ➡️Help Commands.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740319117267/41f4fdb1-ca11-4535-a278-4a77f5b27cf0.png align="center")

# ➡️TAB Completion and Up Arrow Keys.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740319434072/8df88a76-f60e-4353-9226-63dc75af53de.png align="center")

# ➡️Adding Text to FIles.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740320802907/cec605dd-77d1-4287-968b-83117f7f90c5.png align="center")

# ➡️**Standard Output to a command.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740377728193/696193aa-cc04-4708-bd7f-52372a7b5dce.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740377908619/cfb2a387-2b1a-4eef-99e0-90b1acfdfe27.png align="center")

* `tee filename` → Writes output to file (overwrites existing content).
    
* `tee -a filename` → Writes output to file (appends to existing content).
    
* `cat filename` → Displays file content.
    

# ➡️**File Maintenance Commands.**

| Command | Description |
| --- | --- |
| `cp` | Copies files and directories |
| `rm` | Deletes files and directories (`rm -r` for directories) |
| `mv` | Moves or renames files and directories |
| `mkdir` | Creates a directory |
| `rmdir` | Removes an empty directory (`rm -r` for non-empty) |
| `chgrp` | Changes the group ownership of a file/directory |
| `chown` | Changes the owner and/or group of a file/directory |

# ➡️File Display Commands.

| Command | Description |
| --- | --- |
| `cat` | Displays the entire file content |
| `more` | Displays file content **page by page** (forward only) |
| `less` | Displays file content **page by page with scrolling** (forward and backward) |
| `head` | Shows the **first 10 lines** of a file (customizable) |
| `tail` | Shows the **last 10 lines** of a file (customizable, can track changes with `-f`) |

# ➡️Cut - text processors commands.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740379712500/9eeb8f7c-c0c4-4de8-8997-ddcf23dffa9f.png align="center")

# ➡️awk - text processors commands.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740381508950/a5c6f530-dff3-44a4-af2a-630890b4a83c.png align="center")

# ➡️**grep/egrep - text processors commands.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740382028815/121c1deb-0337-4eb1-a1a4-9fa832b7e14c.png align="center")

# ➡️sort/uniq - **text processors commands.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740382188870/f55b2b34-b88e-4005-9e1b-be910ce320e6.png align="center")

# ➡️wc - **text processors commands.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740382372132/dc1f8880-efda-46bf-ad86-babae1b4936f.png align="center")

# ➡️compress and un-compress.

| Command | Description |
| --- | --- |
| `tar -cvf archive.tar file_or_directory` | Create an uncompressed archive |
| `tar -xvf archive.tar` | Extract an uncompressed archive |
| `tar -czvf archive.tar.gz file_or_directory` | Create a compressed `.tar.gz` archive |
| `tar -xzvf archive.tar.gz` | Extract a `.tar.gz` archive |
| `tar -tvf archive.tar.gz` | List contents of a `.tar.gz` file |
| `gzip filename` | Compress a file (`filename` → `filename.gz`) |
| `gzip -d filename.gz` or `gunzip filename.gz` | Decompress a `.gz` file |

# ➡️Linux vs Windows Commands.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1740383576553/043d1633-2350-4021-a7a1-5a8be91bed5e.png align="center")

***(If you have any questions or face issues, feel free to drop a comment below or mail me at*** [***birendra2783@gmail.com***](mailto:birendra2783@gmail.com) ***or watsapp msg on +977 9821508997)***