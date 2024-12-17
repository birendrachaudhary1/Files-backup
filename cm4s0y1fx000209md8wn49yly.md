---
title: "Git installation and configuration on Linux | GitHub | Central/remote repository | Git | basic knowledges | ubuntu"
datePublished: Tue Dec 17 2024 05:29:40 GMT+0000 (Coordinated Universal Time)
cuid: cm4s0y1fx000209md8wn49yly
slug: git-installation-and-configuration-on-linux-github-centralremote-repository-git-basic-knowledges-ubuntu
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1734413361721/3a9aafe3-48c6-4aaf-ac57-c329b956085a.jpeg
tags: cloud, ubuntu, linux, github, python, git, devops, computer

---

**#for ubuntu/Debian:**  
  
1\. ***update packages:***

* sudo apt update -y
    

2. ***install git:***
    

* sudo apt install git
    

3. ***verify installation:***
    

* git --version
    

---

**#after installing git**

***configure your username and email (used in commits):***

* git config --global user.name "Your-Name"
    
* git config --global user.email "[your.email@example.com](mailto:your.email@example.com)"
    

***Verify the configuration:***

* git config --global --list  
      
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734411865085/74cdc76d-5dbf-42d6-8313-b35d011ba7a0.png align="center")