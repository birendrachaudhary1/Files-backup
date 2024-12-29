---
title: "How to solve malicious injection occurred in  database for WordPress site. 🚀"
datePublished: Fri Dec 27 2024 05:57:38 GMT+0000 (Coordinated Universal Time)
cuid: cm56ccimo000x09mndy59desw
slug: how-to-solve-malicious-injection-occurred-in-database-for-wordpress-site
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1735278646580/897d2621-946a-4479-85cf-4eb8cb174841.jpeg
tags: ubuntu, linux, wordpress, mysql, database, troubleshoot

---

* **Description:** A malicious SQL injection attack was identified in the database . The attacker exploited a vulnerability in the application, which allowed unauthorized access to the database.
    
* **Impact:** Downtime error.  
      
      
    Event Description:
    
      
    
    1
    
    Informed from the client the site is too slow.
    
    2
    
    The website was browsed slow.
    
    3
    
    Firstly, I checked the server load, and it was above 2.30. However, the other website on the server is loading quickly and performing well.
    
    4 
    
    Then, I checked the plugins and the entire WordPress core files, and everything was fine. I also updated all the plugins and the WordPress core.  
    But the problem not solved.  
    
    5
    
    After that, I checked the database and found a malicious table.  
    
    6
    
    The scanning from the Wordfence UI couldn't complete. After that, I tried running the scan from the CLI, but I still couldn't get it to work.
    
    7
    
    Then, we deleted the tables directly from the phpMyAdmin database. After that, the site was damaged because of the scripts and links inside the theme.
    
    8
    
    Then, we decided to move to another server. After cleaning up the tables, we transferred the data to the new server, and managed the scripts and links for the themes.
    
    9
    
    We changed all the passwords for the WordPress users and the database.
    
    10
    
    now, its working fine.
    

\[note: If you encounter any issues or problems, feel free to contact me at [**birendra2783@gmail.com**](mailto:birendra2783@gmail.com) [or **+977 9821508997**.\]](mailto:birendra2783@gmail.com)