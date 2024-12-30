---
title: "🎯 How to install Cyberpanel in linux | ubuntu | openlitespeed | wordpress intsall | how it works with wordpress site👁."
datePublished: Wed Dec 18 2024 04:15:51 GMT+0000 (Coordinated Universal Time)
cuid: cm4tdqy9d000009jo7qfuhz1k
slug: how-to-install-cyberpanel-in-linux-ubuntu-openlitespeed-wordpress-intsall-how-it-works-with-wordpress-site
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1734425343283/755482f8-7b7a-4361-90e6-d91f70ba6502.jpeg
tags: ubuntu, linux, wordpress, architecture, devops, wordpressinstallation, cyberpanel

---

* CyberPanel is a web hosting control panel.
    
* CyberPanel typically uses LiteSpeed Web Server as the default web server.
    
* port no. 8090.
    
* it is a open source control panel for cloud hosting.( [https://github.com/usmannasir/cyberpanel](https://github.com/usmannasir/cyberpanel) )
    
    # **#cyberpanel installation**  
    **Requirements-**
    
    * Server with installation of **Ubuntu 18.04, Ubuntu 20.04, AlmaLinux 8, Ubuntu 22.04**, **CloudLinux8**.
        
    * **1024MB RAM, or higher**
        
    * **10GB Disk Space**
        

**1.** **Connect to the server via ssh.**  
ssh username@@[IP](@aboveip)

  
**2\. Update server Packages.**  
sudo apt update  
sudo apt upgrade

  
**3.** **Run the Installation.**  
`sh <(curl` [`https://cyberpanel.net/install.sh`](https://cyberpanel.net/install.sh) `|| wget -O -` [`https://cyberpanel.net/install.sh)`](https://cyberpanel.net/install.sh\)￼4)

[  
**4**](https://cyberpanel.net/install.sh\)￼4)**. Select the version of LiteSpeed.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424367440/b0f92020-cc95-4364-b45b-32e5095d76ae.png align="center")

  
– **Remote MySQL (default N):**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424462893/b30a886c-a9bd-4665-b7b5-4bb48f7860aa.png align="center")

  
– **CyberPanel Version (default Latest Version):**  
press Enter to install the latest version.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424497109/f6492cd4-0e33-46bd-99f1-28235c36bb78.png align="center")

  
– **Password (default “1234567”):**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424526501/09589f33-a0a9-4156-9b26-b278c086bce6.png align="center")

  
– **Memcached (default Y):**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424555915/388a618f-6852-412b-abc3-f5c86bfd06e6.png align="center")

  
– **Redis (default Y):**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424578097/fa2850d8-e184-4fa2-8e69-653d63e3aeb7.png align="center")

  
– **Watchdog (default Yes)**:  
A kernel watchdog is used to monitor if a system is running. It is supposed to automatically reboot hanged systems due to unrecoverable software errors.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424615185/3e2e2ace-c078-4a23-9bce-486fe77d10df.png align="center")

  
\[note: The installation process will initiate automatically and is expected to be complete within 5-10 minutes\]  
  
**\-After the installation.**

**\-Go to web browser URL-** 192.x.x.1:8090  
enter the default username-admin and password-1234567

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424656286/6255ccdc-7384-43ef-9408-2cdcdf0589b5.png align="center")

  
**\-Dashboard will look like this.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424682048/e99b4494-8904-486b-97f8-a06cb28e5024.png align="center")

  
\- it provides graphical interface to create, configure, and manage websites, domains, email accounts, databases, and more, all from a single interface.

**\-we can install wordpress through cyberpanael.**  
\--Go to the website in which you want to install.  
\--Then, click on the manage.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424870896/900c112a-cd6c-45df-a2ad-bc5eeb8a73f9.png align="center")

\--after that scroll down and you will get Wp + LSCache.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424902365/91911107-c9d7-4702-9eb0-2a07ba1345fa.png align="center")

  
**How it works with wordpress site, cloudflare, cloud VPS, database, web server, PhP, MySql.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734424935327/53e96faf-7989-485b-aafd-ca071ada13d1.png align="center")