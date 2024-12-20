---
title: "❎Disk space full issue 🚀| wordpress site | php | Linux | wordpress admin |"
datePublished: Fri Dec 20 2024 04:15:26 GMT+0000 (Coordinated Universal Time)
cuid: cm4w8m4y3000l09mk2nftebwt
slug: disk-space-full-issue-wordpress-site-php-linux-wordpress-admin
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1734501002410/830ef62a-bc56-4b59-baf1-f9fe9f7105e0.jpeg
tags: digitalocean, cloud, linux, aws, wordpress, php, troubleshooting, troubleshoot, disk-space, mount, disk-management, wordpress-site

---

# **Users were unable to upload contents from the admin panel.**

### Event Description and solution:

* Informed that the site-admin were unable to upload photos from the admin-panel.
    
* The website was being browsed well
    
* Identified the disk full issue on the [lokpath.com](http://lokpath.com) [server](http://lokpath.com/).
    
* Added 15 GB storage from digitalocean volume.
    
* Stopped all the services using the volume
    
    i.e
    
    * lshttpd (litespeed)
        
    * lscpd (cyberpanel)
        
* Running the file system check but was not successful, showed the disk was being used.  
    \- e2fsck -f /dev/disk/by-id/scsi-0DO\_Volume\_lokpathcpvolume
    
* Restarted the server once
    
* Started the process again serially:  
    stopped all the services
    
    * unmounted the volume
        
    * `umount /home`
        
    * ext4 file system check
        
    * e2fsck -f /dev/disk/by-id/scsi-0DO\_Volume\_lokpathcpvolume
        
* expand the partition
    
    * resize2fs /dev/disk/by-id/scsi-0DO\_Volume\_lokpathcpvolume
        
* Confirmed that it was working with df -h
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1734501359139/b981717e-7be7-4ea1-a64d-de820c45eb00.png align="center")
    

\[*note: if you can’t understand or need any help you can mail me at birendra2783@gmail.com*\]