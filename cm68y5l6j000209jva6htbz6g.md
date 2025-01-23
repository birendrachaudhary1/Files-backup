---
title: "How to install Prometheus  on linux.🎯"
datePublished: Thu Jan 23 2025 06:23:21 GMT+0000 (Coordinated Universal Time)
cuid: cm68y5l6j000209jva6htbz6g
slug: how-to-install-prometheus-on-linux
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1737612117778/1a586418-3c76-4a28-9521-6d8be5bd80d2.jpeg
tags: ubuntu, linux, monitoring, prometheus, installation

---

Prometheus is an open-source monitoring and alerting toolkit designed for collecting and analyzing metrics as time-series data. It uses a pull-based model to scrape metrics, supports dynamic service discovery, and offers a flexible query language (PromQL). Commonly used in cloud-native environments, it integrates well with tools like Grafana for visualization and Alertmanager for notifications. Prometheus is scalable, reliable, and ideal for monitoring modern, distributed systems.

## ➡**Download the prometheus zip-file.**

command: wget [https://github.com/prometheus/prometheus/releases/download/v2.35.0/prometheus-2.35.0.linux-amd64.tar.gz](https://github.com/prometheus/prometheus/releases/download/v2.35.0/prometheus-2.35.0.linux-amd64.tar.gz)

## ➡**unzip prometheus zip-file.**

**command:** tar -xvfz prometheus-2.35.0.linux-amd64.tar.gz

## ➡**Go to that directory.**

**command:** cd prometheus-2.35.0.linux-amd64

## ➡**run**

./prometheus --config.file=prometheus.yml

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737612565319/5758114b-d6cd-448e-9da2-8eccefda470e.png align="center")

## ➡**Stop the running Prometheus process that we left running, and copy the new files to bin folder in prometheus.**

**command:** cp -r . /usr/local/bin/prometheus/

## ➡**Create a file called prometheus.service.**

command: vim /etc/systemd/system/prometheus.service

## ➡**Add this script on that prometheus.service and save.**

\[Unit\]  
Description=Prometheus Service  
After=[network.target](http://network.target)

\[Service\]  
Type=simple  
ExecStart=/usr/local/bin/prometheus/prometheus --config.file=/usr/local/bin/prometheus/prometheus.yml

\[Install\]  
WantedBy=[multi-user.target](http://multi-user.target)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737612792086/fe454a7d-e326-4e2f-8403-dd2e68876225.png align="center")

## ➡**Now, check the status.**

command: sudo service prometheus start  
sudo service prometheus status

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737612926598/b8701f01-c058-4670-91ee-0736ed04f091.png align="center")

## ➡**Go to the web browser.**

ip\_adress:9090 eg-192.x.x.x:9090

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737613008006/4d767859-eae4-4c73-ac42-ac48f1ef120f.png align="center")

*(note-if you are facing a problem you have to open the port.)*

## ➡**Allowing incoming TCP connections on port 9090.**

command: sudo iptables -A INPUT -p tcp --dport 9090 -j ACCEPT

## ➡**Restart the prometheus.**

command: sudo systemctl restart prometheus

## ➡Conclusion:

Installing Prometheus on a Linux system involves downloading the Prometheus binary, setting it up as a service for easy management, and ensuring network access to its web interface. By following the steps provided, you can successfully deploy Prometheus and start monitoring your system or application metrics. If any issues arise, such as port access problems, they can be resolved by configuring firewall rules. This setup ensures Prometheus runs seamlessly as a service and is accessible via the browser for real-time monitoring.

*If you have any questions or face issues, feel free to drop a comment below or mail me at* [***birendra2783@gmail.com***](mailto:birendra2783@gmail.com)*!*