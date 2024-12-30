---
title: "🎯How to setup two server  for high-traffic WordPress website.✔👁| news portal sites."
datePublished: Sun Dec 22 2024 04:15:32 GMT+0000 (Coordinated Universal Time)
cuid: cm4z3hyv200010ala1uab8lsy
slug: how-to-setup-two-server-for-high-traffic-wordpress-website-news-portal-sites
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1734673351623/bcc56f2b-ad41-43b2-9a7e-42c934da5035.jpeg
tags: cloud, linux, aws, wordpress, server, database, configuration, cloud-platforms

---

We have to setup two server one for database and one for WordPress file.

#database server setup.

step 1: Buy an instance from any cloud platform based on the required storage and other specifications.  
step 2: Set up the database server:  
**\- #install MySQL**

**commands:** sudo apt update && upgrade -y  
sudo apt install mysql-server  
sudo mysql\_secure\_installation **#' set or change the root password for the MYSQL server'**

\- **#Configure MySQL**

**commands:** #Edit the configuration file `/etc/mysql/my.cnf` for MySQL  
\[mysqld\]  
bind-address = 0.0.0.0

sudo systemctl restart mysql

**#Create Database and User**

sudo mysql -u root -p  
CREATE DATABASE wordpress\_db;  
CREATE USER 'wp\_user'@'%' IDENTIFIED BY 'your\_password';  
GRANT ALL PRIVILEGES ON wordpress\_db.\* TO 'wp\_user'@'%';  
FLUSH PRIVILEGES;  
EXIT;

**#Configure Firewall**

**command:** sudo ufw allow 3306

# **#wordpress file server setup:**

\- Buy another instance from the same cloud platform used for the database server.

commands: sudo apt update && upgrade -y

**#configure cyberpannel and install wordpress.**  
Follow the instructions in this guide:  
[https://biren.hashnode.dev/cyberpanel-installation-in-linux-ubuntu-openlitespeed-wordpress-intsall-how-it-works-with-wordpress-site](https://biren.hashnode.dev/cyberpanel-installation-in-linux-ubuntu-openlitespeed-wordpress-intsall-how-it-works-with-wordpress-site)

**#configure wp-config.php file** (edit)  
define('DB\_HOST', 'database\_server\_ip');

**#manage all required permission**  
\- Directories should have `755` permissions.  
\- Files should have `644` permissions.

\[note: If you encounter any issues or problems, feel free to contact me at [**birendra2783@gmail.com**](mailto:birendra2783@gmail.com) or **+977 9821508997**.\]