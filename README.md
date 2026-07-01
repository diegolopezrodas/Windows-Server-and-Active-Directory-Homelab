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
*Creating Password Policy GPO*

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Password%20Policy%20GPO%20Pt.%201.png)
*Accessing Password Policy GPO Settings*

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Password%20Policy%20GPO%20Pt.%202.png)
*Editing Password Policy GPO*

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Restrict%20Control%20Panel%20GPO.png)
*Editing Restrict Control Panel GPO*

![](/assets/Vid2_GP%20Create%20and%20Set%20Up/Editing%20Account%20Lockout%20Policy%20GPO.png)
*Editing Account Lockout Policy GPO*

## [Group Policy Management: Applying and Testing](https://youtu.be/RrRsoRGaKLM?si=pKbCQYkpY39lB5qu)

![](/assets/Vid3_GP%20Apply%20and%20Test/ipconfig%20Windows%20Server%202022.png)
*Executing `ipconfig` in terminal on Windows Server*

![](/assets/Vid3_GP%20Apply%20and%20Test/Using%20ipconfig%20to%20config%20static%20IPv4%20addr.png)
*Using information from `ipconfig` to statically configure Windows Server IPv4 address*

![](/assets/Vid3_GP%20Apply%20and%20Test/Turning%20off%20IPv6%20protocol%20on%20Windows%20Server%202022.png)
*Turning off IPv6 protocol on Windows Server*

![](/assets/Vid3_GP%20Apply%20and%20Test/nslookup%20of%20local%20domain%20on%20Windows%20Enterprise%20verifying%20IPv4%20addr.png)
*Executing `nslookup` in terminal on Windows Enterprise VM to confirm changes*

![](/assets/Vid3_GP%20Apply%20and%20Test/Changing%20Windows%20Enterprise%20System%20Properties%20to%20make%20it%20member%20of%20local%20domain%20Pt.%201.png)
*Changing Windows Enterprise VM (`COMP01`)properties to become member of SHIELD.local*

![](/assets/Vid3_GP%20Apply%20and%20Test/Changing%20Windows%20Enterprise%20System%20Properties%20to%20make%20it%20member%20of%20local%20domain%20Pt.%202.png)
*Confirming changes to VM made*

![](/assets/Vid3_GP%20Apply%20and%20Test/Showing%20Sign-In%20screen%20of%20Windows%20Enterprise%20Pt.%201.png)
*Showing Sign-in screen on Windows Enterprise VM*

![](/assets/Vid3_GP%20Apply%20and%20Test/Showing%20Sign-In%20screen%20of%20Windows%20Enterprise%20Pt.%202.png)
*Showing Sign-in screen with `\.` in the `Username` field*

![](/assets/Vid3_GP%20Apply%20and%20Test/Linking%20GPOs%20to%20%20Asia-Users%20OU.png)
*Linking GPOs to `Asia/Users` OU*

![](/assets/Vid3_GP%20Apply%20and%20Test/Linking%20GPOs%20to%20%20Asia-Computers%20OU.png)
*Linking GPOs to `Asia/Computers` OU*

![](/assets/Vid3_GP%20Apply%20and%20Test/Showing%20Windows%20Enterprise%20COMP01%20in%20local%20domain.png)
*Displaying `COMP01` VM name in `Computers` OU*

![](/assets/Vid3_GP%20Apply%20and%20Test/Moving%20Windows%20Enterprise%20COMP01%20to%20USA-Computers.png)
*Moving `COMP01` VM to `USA/Computers` OU*

![](/assets/Vid3_GP%20Apply%20and%20Test/Showing%20Windows%20Enterprise%20COMP01%20in%20USA-Computers.png)
*Displaying `COMP01` successfully moved to `USA/Computers` OU*

## [File Services: Setting Up Networking Sharing](https://youtu.be/OBnuOOWdEmc?si=c08fU7ObyZ7u6J5D)

![](/assets/Vid4_Files%20Services/Created%20SHARED%20folder%20and%20adding%20Domain%20Users%20into%20Share%20Permissions.png)
*Created `SHARED` folder in Windows Server and modified Share Permissions to add Domain Users*

![](/assets/Vid4_Files%20Services/Domain%20Users%20have%20Read%20Only%20permissions%20on%20SHARED%20folder.png)
*Giving Domain Users only read privileges to `SHARED` folder*

![](/assets/Vid4_Files%20Services/Editing%20Drive%20Mapping%20GPO%20to%20have%20Windows%20Server%20Host%20Name%20&%20Path%20to%20File.png)
*Creating Drive Mapping GPO with Windows Server name and path to folder: `\\WIN-GK52R0DH6LO\SHARED`*

![](/assets/Vid4_Files%20Services/Establish%20Quota%20on%20SHARED%20folder.png)
*Establishing Quota on `SHARED` folder*

![](/assets/Vid4_Files%20Services/Creating%20a%20File%20Screen%20on%20SHARED%20folder.png)
*Establishing File Screen on `SHARED` folder*

![](/assets/Vid4_Files%20Services/Accessing%20SHARED%20folder%20on%20Windows%20Enterprise%20COMP01.png)
*Accessing `SHARED` folder on Windows Enterprise VM*

## [Testing Windows File Sharing](https://youtu.be/pmDH4DH_3Ik?si=QR7Ev9Duo_iJHXIu)

![](/assets/Vid5_Windows%20File%20Sharing/SHARED%20folder%20Shared%20Permissions.png)
*Displaying Domain Admins share permissions on `SHARED` folder*

![](/assets/Vid5_Windows%20File%20Sharing/SHARED%20folder%20Security%20Permissions%20Domain%20Users.png)
*Displaying Domain Users security permissions on `SHARED` folder*

![](/assets/Vid5_Windows%20File%20Sharing/SHARED%20folder%20Security%20Permissions%20Domain%20Adminstrators.png)
*Displaying Domain Admins security permissions on `SHARED` folder*

![](/assets/Vid5_Windows%20File%20Sharing/Adding%20Admin%20Doc%20to%20SHARED%20folder%20using%20Windows%20Server.png)
*Creating `ADMIN DOC` file in `SHARED` folder on Windows Server side*

![](/assets/Vid5_Windows%20File%20Sharing/Accessing%20Admin%20Doc%20on%20SHARED%20folder%20using%20Windows%20Enterprise%20COMP01.png)
*Accessing `ADMIN DOC` file in `SHARED` folder on Windows Enterprise side*

![](/assets/Vid5_Windows%20File%20Sharing/Modified%20Admin%20Doc%20on%20SHARED%20folder%20using%20Windows%20Enterprise%20COMP01.png)
*Modifying `ADMIN DOC` file in `SHARED` folder on Windows Enterprise side*

![](/assets/Vid5_Windows%20File%20Sharing/Accesing%20modified%20Admin%20Doc%20on%20SHARED%20folder%20using%20Windows%20Server.png)
*Accessing `ADMIN DOC` file in `SHARED` folder on Windows Server side*

## [Access-Based Enumeration](https://youtu.be/WuUBQthpVIM?si=aASc3joLr0XRENgB)

![](/assets/Vid6_ABE/Making%20IT%20folder%20in%20SHARED%20folder%20with%20%20Share%20permissions%20for%20IT%20group.png)
*Creating `IT` folder in `SHARED` folder and adding shared permissions to IT groups*

![](/assets/Vid6_ABE/Adding%20Security%20permissions%20for%20IT%20group%20on%20IT%20folder%20in%20SHARED%20folder.png)
*Adding security permissions for IT groups to `IT` folder*

![](/assets/Vid6_ABE/Same%20steps%20from%20IT%20but%20for%20HR.png)
*Creating `IT DOC` in `IT` folder*

![](/assets/Vid6_ABE/Same%20steps%20from%20IT%20but%20for%20HR.png)
*Completing same steps for HR groups*

![](/assets/Vid6_ABE/Accessing%20IT%20Doc%20on%20Windows%20Enterprise%20COMP01%20on%20IT%20group.png)
*Accessing `IT DOC` on Windows Enterprise while signed in to IT group account*

![](/assets/Vid6_ABE/Failing%20to%20accessing%20HR%20Doc%20on%20Windows%20Enterprise%20COMP01%20on%20IT%20group.png)
*Failure to access `HR DOC` on Windows Enterprise while signed in to IT group account*

![](/assets/Vid6_ABE/Enabling%20ABE%20on%20SHARED%20folder%20to%20hide%20HR%20folder%20to%20non%20HR%20groups.png)
*Enabling ABE on `SHARED` folder*

![](/assets/Vid6_ABE/Viewing%20only%20HR%20folder%20on%20Windows%20Enterprise%20COMP01%20on%20HR%20group.png)
*Viewing ONLY `HR` folder on Windows Enterprise while signed in to HR group account*

![](/assets/Vid6_ABE/Accessing%20HR%20doc%20on%20Windows%20Enterprise%20COMP01%20on%20HR%20group.png)
*Accessing `HR DOC` file on Windows Enterprise while signed in to HR group account*