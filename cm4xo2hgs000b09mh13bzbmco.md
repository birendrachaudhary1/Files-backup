---
title: "🎯How to solve slowness seen on the website🚀 | troubleshoot | load average | Log | problem | wp cli | plugins.✔"
datePublished: Sat Dec 21 2024 04:15:49 GMT+0000 (Coordinated Universal Time)
cuid: cm4xo2hgs000b09mh13bzbmco
slug: how-to-solve-slowness-seen-on-the-website-troubleshoot-load-average-log-problem-wp-cli-plugins
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1734672006319/ba583a94-047f-4aef-9362-5cd99452d3f6.jpeg
tags: linux, wordpress, redis, database, plugins, load-balancing, troubleshoot, slowness

---

# Description: Clients reported experiencing slow performance on the website. Pages were taking longer time to load than usual.  
  
  
#one of the method

* **we optimized the database**: cmd - wp db optimize --allow-root
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734670878734/7d3e7987-34ee-420c-a807-0240ba5dc2a5.png align="center")
    
    * **Redis cache**: redis cache connected from wp-admin panel. This should decrease hits to the DB. (from wordpress user and password)
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734671001996/bc544fcb-8a56-450d-8d66-8cdb60096793.png align="center")
        
        * Timeout seen on the site:
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734671213079/77a29e14-a308-498c-bb7c-7c430f80b8b1.png align="center")
            
            **Contributing Factors: -** Most of the memory usage seen from mysql.
            
            \- Swapfile for 2G is already seen allocated.
            
            \- Redis server also seen started here.