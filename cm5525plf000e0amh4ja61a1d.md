---
title: "🎯How to transfer database  from one server to another of WordPress site with script.🚀"
datePublished: Thu Dec 26 2024 08:24:38 GMT+0000 (Coordinated Universal Time)
cuid: cm5525plf000e0amh4ja61a1d
slug: how-to-transfer-database-from-one-server-to-another-of-wordpress-site-with-script
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1735196288141/85ba0e9d-0505-48af-b008-6d8be159f0da.jpeg
tags: wordpress, php, databases, database, migrate, linux-ubuntu-aws-devops-automation

---

# **STEP 1:**

[**Script.sh**](http://Script.sh)  
  
#!/bin/bash

#Database credentials

DB\_NAME=''  
DB\_USER=''  
DB\_PASSWORD=''  
DB\_HOST='[localhost](http://localhost)'

#Backup file name with date

BACKUP\_FILE="${DB\_NAME}*$(date +'%Y%m%d*%H%M%S').sql"

#Perform the database dump

mysqldump --user=$DB\_USER --password=$DB\_PASSWORD --host=$DB\_HOST $DB\_NAME &gt; $BACKUP\_FILE

#Check if the command was successful

if \[ $? -eq 0 \]; then  
echo "Database backup successful: $BACKUP\_FILE"  
else  
echo "Error creating database backup"  
fi

# STEP 2:

  
\-gzip database\_name.sql

# **STEP 3:**

  
**#To the Destination server**  
\-scp database\_name.sql.gz user@destination\_server:/path/to/destination

# **STEP 4 :**

  
**#unzip**  
\---gunzip database\_name.sql.gz

# **STEP 5:**

  
**#Import**  
\-mysql -u username -p new\_database\_name &lt; /path/to/destination/database\_name.sql

***(NOte: Fix the permission after everything)***