# Windows Server and Active Directory Homelab Project

### This file is the documentation of a Windows Server Homelab project conducted on virtual machines

> This is a personal project I conducted to test my knowledge of active directory I obtained from activities on TryHackMe. Additionally, this project was conducted using the East Charmer's [guide/playlist](https://youtube.com/playlist?list=PLAdEnQWAAbfXMY2D4HVZOe-ChfTKmaJfQ&si=cPAYy-zloqei4_JK) on Youtube so that I can learn on Active Directory is set up and used in a professional setting. With this project I had 3 main goals in mind:

* Emulate Windows Server 2022 using UTM 
* Virtualize Windows Enterprise using UTM
* Connect Windows Enterprise VM to Windows Server and apply policies to it

## Table of Contents

The following sections will be titled similarily after East Charmer's videos, as certain screenshots that were taken correspond with content and guide specific to a video's instructions. In addition, the titles of the sections will have a hyperlink directly to the video. 

* [Installing and Configuring Active Directory on Windows 2022](https://youtu.be/GsmJowwIh8Q?si=09GuUybAoTqry6xl)
* [Group Policy Management: Creating and Setting](https://youtu.be/6F7-tV4lYFw?si=9k7aKIGb0RejCtZg)
* [Group Policy Management: Applying and Testing](https://youtu.be/RrRsoRGaKLM?si=pKbCQYkpY39lB5qu)
* [File Services: Setting Up Networking Sharing](https://youtu.be/OBnuOOWdEmc?si=c08fU7ObyZ7u6J5D)
* [Testing Windows File Sharing](https://youtu.be/pmDH4DH_3Ik?si=QR7Ev9Duo_iJHXIu)
* [Access-Based Enumeration](https://youtu.be/WuUBQthpVIM?si=aASc3joLr0XRENgB)

## [Installing and Configuring Active Directory on Windows Server 2022](https://youtu.be/GsmJowwIh8Q?si=09GuUybAoTqry6xl)

This section will be short as configuring the virtual machines will depend on your host machine's components, and how many resources you wish to dedicate to your VMs. Additionally, installing the ISO images are readily available on Microsoft's website with proper documentation and steps how to install and step up before creating your organization units.

![Windows Server 2022](/assets/Vid1_Config%20AD/Windows%20Server%202022%20.png)
*Windows Server 2022 Emulation Configuration Settings*

![Windows Enterprise](/assets/Vid1_Config%20AD/Windows%20Enterprise.png)
*Windows Enterprise VM Configuration Settings*

![](/assets/Vid1_Config%20AD/AD%20Setting%20Up%20OUs%20and%20Groups:Users.png)
*Creating Security Group `Accounting - Europe` for `Europe/Users` OU*

## [Group Policy Management: Creating and Setting](https://youtu.be/6F7-tV4lYFw?si=9k7aKIGb0RejCtZg)

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Creating%20Password%20Policy%20GPO.png)

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Account%20Lockout%20Policy%20GPO.png)

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Password%20Policy%20GPO%20Pt.%201.png)

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Password%20Policy%20GPO%20Pt.%202.png)

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Restrict%20Control%20Panel%20GPO.png)

## [Group Policy Management: Applying and Testing](https://youtu.be/RrRsoRGaKLM?si=pKbCQYkpY39lB5qu)

![](/assets/Vid3_GP%20Apply%20and%20Test/Changing%20Windows%20Enterprise%20System%20Properties%20to%20make%20it%20member%20of%20local%20domain%20Pt.%201.png)

![](/assets/Vid3_GP%20Apply%20and%20Test/Changing%20Windows%20Enterprise%20System%20Properties%20to%20make%20it%20member%20of%20local%20domain%20Pt.%202.png)

![](/assets/Vid3_GP%20Apply%20and%20Test/ipconfig%20Windows%20Server%202022.png)

## [File Services: Setting Up Networking Sharing](https://youtu.be/OBnuOOWdEmc?si=c08fU7ObyZ7u6J5D)

## [Testing Windows File Sharing](https://youtu.be/pmDH4DH_3Ik?si=QR7Ev9Duo_iJHXIu)

## [Access-Based Enumeration](https://youtu.be/WuUBQthpVIM?si=aASc3joLr0XRENgB)