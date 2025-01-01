---
title: "How to enable WSL in windows 11 home version 24H2(Quick and Easy Way).🚀"
datePublished: Wed Jan 01 2025 06:06:20 GMT+0000 (Coordinated Universal Time)
cuid: cm5dhuyro000009l1awh49o8d
slug: how-to-enable-wsl-in-windows-11-home-version-24h2quick-and-easy-way
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1735711471102/5027ec72-525d-499a-88c5-04dbdb5b5228.jpeg
tags: ubuntu, linux, wsl, windows-11, enable

---

**WSL (Windows Subsystem for Linux) is a compatibility layer that allows you to run Linux directly on Windows without the need for a virtual machine or dual boot. It seamlessly integrates Linux tools, commands, and distributions into your Windows environment, making it ideal for developers, system admins, and anyone working with open-source software. WSL 2, the latest version, uses a real Linux kernel, offering improved performance and full compatibility with Linux apps. It's a powerful tool for combining the best of Windows and Linux in one system.**

# ➡Requirements for WSL on Windows 11 Home:  

* **Operating System**: Windows 11 Home, version 22H2 or later (24H2 is supported).
    
* **Architecture**: 64-bit system with x64 or ARM64 processor.
    
* **Windows Build**: Build 22000 or later.
    
* **Virtualization Support**: Enabled in BIOS/UEFI.
    
    * Ensure features like **VT-x/AMD-V** (Intel/AMD virtualization) and **Hyper-V** are enabled in your BIOS/UEFI settings.  
          
          
        

# ➡1. Open **Windows Features**  

Press **Win + R**, type turn windows features on and off, and press Enter.  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdWE_KdoV4JcR5Wj492UJi3HCtq7k-WHQq1dt2mfQjo0vP0b0fuM8NrHoP2vySyGR8aVTr1iL5JJc4Y-WwREBRlBoid7DXvpVg3rofe7GuEAK5vLKjwDb-0u7H2ws3I4J9b1Uc4IA?key=IsJjjvIxA9_7wV314f6IQBZw align="left")

# ➡2. In the dialog box, enable the following features:

* **Windows Subsystem for Linux**
    
* **Virtual Machine Platform**
    
      
      
      
    **Click OK and restart your computer.**  
    
    ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd0BYUzqE4sLw7q5n_XbcUpwjx4fZVUcgTn2wNC0NQAwX-6rkJ-E5Ze0zQb4Ao1RHi0s5npSDThSCEYEd9Ec446JeMpgxxR7mYO0_7-A6WcFthi2r9zgLuQkm1nj439hl9_7Gw32g?key=IsJjjvIxA9_7wV314f6IQBZw align="left")
    
    ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcKy0Dgzx7X180PAvu9eA-U9Dj8rYah3PI9QucIPQcuOnnH3xg927Pt7KSpe7xPGuhtPHpr2YEYdNoMi1Xp0D7_n_TiXSsoOl6-eeM8GfzwbfwGhX1MdFo33MxcJ38eidHOo1VgaA?key=IsJjjvIxA9_7wV314f6IQBZw align="left")
    
    # ➡3. Install a Linux distribution (Ubuntu 22.04.5 LTS) from the **Microsoft Store**.  
    
    ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdaTVYvKPBtY1WeU6BXE6b8IIU7UUn22EzISj1R9lRRHQeSH7L3C_xY-UJOOkebOr8jt46y_U8Wp2d07GMmCQJ6FJq5-x_m-nHznY4tFpM5tkwSJyDe87KDaL3E18P_6uYNA5MSBw?key=IsJjjvIxA9_7wV314f6IQBZw align="left")
    

# ➡4. open command prompt and check wsl status.

command: wsl —status  
  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcWYCXQqvqFbDYjW2zHR2EuNaBwMuSe0rK7YxrHKCE8_HwmK7YEG9qukEo1Dsqd21xPMcVpyVQ2y69aam-__2Sk6mOlg4JpVBpt-QPhIGAFATDuWqHLpgNquJgxn_YHpSvFvOVq2g?key=IsJjjvIxA9_7wV314f6IQBZw align="left")

# ➡5. if not installed install it.  
  

command: wsl —install  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe_K6ywY0tlu2zMqq8BbhUjX008Rf8sv2moPiATvO8mT0jZAvZAi-Z802-z0CFFtnTiLgwz9_wDfv1cP0pEu0H729x7c7eEuqoKe7mWPiXjNx7pRdjwobn93SAEbxJOtPNkITNo?key=IsJjjvIxA9_7wV314f6IQBZw align="left")

# ➡6. After, installation setup username and password.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfPPe5Kq2__5eVpVUEhHz7zIdn9d-dsqRbzeq0hnPQ8k8KTvyyOKqOP7RsTElo9s361xsk4rnAgXkL07Fg8G5pFWE8pIbyi--4QhVxBEsIi5XniursZanAAnr9qe6Y2GCZJQGDC8A?key=IsJjjvIxA9_7wV314f6IQBZw align="left")

# ➡Conclusion:

Enabling Windows Subsystem for Linux (WSL) on Windows 11 Home is a straightforward process that unlocks the power of Linux directly within your Windows environment. Whether you're a developer, system administrator, or simply a tech enthusiast, WSL provides a versatile platform for running Linux tools and workflows without the need for a separate machine or virtual machine.

Now that you've successfully enabled WSL, you can explore the vast world of Linux. Install your favorite tools, run commands, or even host applications—all within a seamless, integrated environment.

*If you have any questions or face issues, feel free to drop a comment below or mail me at birendra2783@gmail.com! Happy coding! 🚀*