---
title: "📉How to install grafana on linux and  how to setup with prometheus (whole setup).🚀"
datePublished: Sat Jan 25 2025 19:15:45 GMT+0000 (Coordinated Universal Time)
cuid: cm6ckmlm8000g0al614628gyh
slug: how-to-install-grafana-on-linux-and-how-to-setup-with-prometheus-whole-setup
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1737621957871/64aae97a-a392-4408-831c-417e81d48f51.jpeg
tags: ubuntu, linux, monitoring, prometheus, grafana, alerting, nodeexporter

---

Grafana, paired with Prometheus and Node Exporter, is a powerful monitoring stack for system and application metrics. Prometheus collects metrics from Node Exporter, which provides system stats like CPU, memory, and disk usage. Grafana connects to Prometheus as a data source, offering a user-friendly interface to visualize and analyze these metrics.

This setup is ideal for real-time monitoring, performance analysis, and troubleshooting. With customizable dashboards and alerting capabilities, it helps ensure system reliability and efficiency, making it a go-to solution for DevOps and IT teams.

## ➡**update packages.**

command= sudo apt-get install -y apt-transport-https  
command= sudo apt-get install -y software-properties-common wget  
command= wget -q -O - [https://packages.grafana.com/gpg.key](https://packages.grafana.com/gpg.key) | sudo apt-key add -

## ➡**Add stable repository of Grafana.**

command= echo "deb [https://packages.grafana.com/enterprise/deb](https://packages.grafana.com/enterprise/deb) [stable main" | sudo tee -a /etc/apt/sources](https://packages.grafana.com/enterprise/deb).list.d/grafana.list

## ➡**Update repository and Install Grafana.**

command=sudo apt-get update  
command=sudo apt-get install grafana-enterprise

## ➡**Start the Grafana Server.**

command=sudo systemctl daemon-reload  
command=sudo systemctl start grafana-server  
command=sudo systemctl status grafana-server

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622183979/afcc26e8-bda1-4739-a72c-e16a125cc9e0.png align="center")

## ➡**While rebooting the server to auto restart grafana.**

command=sudo systemctl enable grafana-server.service

## ➡**To open pot no. 3000**

command= sudo iptables -A INPUT -p tcp --dport 3000 -j ACCEPT

## ➡Go to the browser

ip\_address:3000

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622331595/e0c01aa5-eb47-4fec-904a-2c882f9cc77a.png align="center")

## ➡To visualize metrics, you need to add a data source first. Click Add data source and select Prometheus.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622626039/cd94e0cf-d3c4-42b8-9d2a-383b53df614d.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622647465/3805cc4e-21b6-4d58-a98d-2761adc4a14a.png align="center")

For the URL, enter [localhost:9090](http://localhost:9090) [and click Save](http://localhost:9090/) and test. You can see Data source is working. Click on Save and Test.

## ➡Click on Import Dashboard paste th[is code 1860 a](http://localhost:9090/)nd click on load

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622703845/53b87c85-48af-4b54-82e8-786326318b01.png align="center")

## ➡Select the Datasource and click on Import

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622743886/240796dc-e616-42fd-a251-0ea431c48798.png align="center")

## ➡You will see this output

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622779683/781fe74d-6c1d-41df-a101-1f246e3cb2eb.png align="center")

## ➡**For node exporter target we have to add job inside /usr/local/bin/prometheus/prometheus.yml.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622397170/746ac259-ce1b-49d5-9f89-ee46cb19aafb.png align="center")

## ➡**Now, it will work in prometheus dashboard and grafana dashboard, the data will be availabale.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737622452454/9ebd0ab3-a8a6-46e2-ba5c-62c9cf33eb71.png align="center")

## ➡Conclusion:

The Grafana, Prometheus, and Node Exporter stack is now fully set up on Linux. Grafana provides insightful visualizations of metrics scraped by Prometheus from Node Exporter. This comprehensive setup ensures efficient monitoring of your system's performance.

*If you have any questions or face issues, feel free to drop a comment below or mail me at* [***birendra2783@gmail.com***](mailto:birendra2783@gmail.com)*!*