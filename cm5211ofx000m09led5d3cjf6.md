---
title: "how to install and configure uptime kuma with docker.🚀"
datePublished: Tue Dec 24 2024 05:30:12 GMT+0000 (Coordinated Universal Time)
cuid: cm5211ofx000m09led5d3cjf6
slug: how-to-install-and-configure-uptime-kuma-with-docker
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1735018007305/1c5e07e7-18b7-48d7-9bb7-09791e20db50.jpeg
tags: dns, ubuntu, linux, docker, https, devops, monitoring-tool, linuxsystemadministration, uptime-kuma

---

Uptime Kuma is a tool you can host yourself to monitor the health of different services, like websites, servers, or databases. It supports checks for things like HTTP, HTTPS, DNS, PING, TCP, and SQL. If something goes down, it can send alerts via Email, Telegram, Discord, Microsoft Teams, and more.

You can run Uptime Kuma in a Docker container, which makes it lightweight, fast, and easy to set up. I'll guide you on how to build and configure it in Docker.  

How to install Docker (if it’s not already installed).

* Update your system: sudo apt update
    

* Install Docker: sudo apt install -y [docker.io](http://docker.io)
    
* Start Docker: sudo systemctl start docker
    
* Enable Docker to start on boot: sudo systemctl enable docker
    
* Check Docker version: docker --version
    
* Test Docker: sudo docker run hello-world
    

**STEP-1: Open the terminal on your server where Docker is installed:**  
command: docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1735016744620/d1d57b96-0210-4c00-91be-79133e3a0460.png align="center")

**STEP-2: Run this command to check if Uptime Kuma is running on port 3001:**  
command: docker ps

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1735017585672/c74686ea-97f7-440c-8320-54effe9cc3c1.png align="center")

**STEP-3: Open a web browser on the same device where Docker is installed and go to:**  
command: http://your\_ip-address:3001

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1735017700192/e2ed6a91-9a86-40e1-89ba-660a918614f6.png align="center")

\[note: If you encounter any issues or problems, feel free to contact me at [**birendra2783@gmail.com**](mailto:birendra2783@gmail.com) or **+977 9821508997**.\]