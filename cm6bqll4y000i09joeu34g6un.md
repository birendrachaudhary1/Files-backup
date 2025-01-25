---
title: "How to add another server on node-exporter and prometheus and Structure.🚀"
datePublished: Sat Jan 25 2025 05:15:09 GMT+0000 (Coordinated Universal Time)
cuid: cm6bqll4y000i09joeu34g6un
slug: how-to-add-another-server-on-node-exporter-and-prometheus-and-structure
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1737615210889/99b2defb-0cc4-4706-a89a-081695cfa141.jpeg
tags: ubuntu, linux, monitoring, prometheus, grafana, nodeexporter

---

Prometheus acts as the **server**, scraping and storing metrics from **Node Exporter**, the **client**, which collects system-level metrics (CPU, memory, disk, etc.) and exposes them at [`http://server_ip:9100/metrics`](http://server_ip:9100/metrics). Prometheus is configured to scrape this endpoint, storing the data in its time-series database. You can visualize the metrics using Prometheus' UI or integrate it with Grafana for advanced dashboards.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737614783311/d3ab3bbc-968a-4c48-a31d-5acb3c38f8ff.png align="center")

## ➡How to add another server:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737614834545/68329a81-a180-4273-b565-519403005e79.png align="center")

## ➡**Inside prometheus directory exporter-config.yml file add ip\_address.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1737614905785/b07d2549-ab50-4f56-9135-95b98d7515fe.png align="center")

### *On Next blog: How to install Grafana and how to connect with prometheus and node-exporter.*

*If you have any questions or face issues, feel free to drop a comment below or mail me at* [***birendra2783@gmail.com***](mailto:birendra2783@gmail.com)*!*