# Network Security Groups (NSGs) and Inspecting Network Protocols
<p align="center">
<img src="https://imgur.com/rWWmatS.png" alt="windows logo"/>
</p>

This tutorial outlines network security groups (NSGs) and inspecting network protocols.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Setup resources in Microsoft Azure (Azure) by:
    - Creating a Domain Controller (DC) Windows Server 2022 (Virtual Machine - VM) and naming it, “DC-1.”
    - Creating a Client VM (Windows 10) and naming it, “Client-1,” using the same Resource Group and Virtual Network (Vnet) as DC-1. 
- Ensure connectivity between the Client-1 and DC-1.
- Install Active Directory (AD)
- Create an Administrator and Normal User Account in Active Directory.
- Join Client-1 to your domain.
    - For example: mydomain.com
- Setup Remote Desktop for non-administrative users within Client-1.
- Create additional users and attempt to log into Client-1 as one of the users.


<h2>Setting Up Network Security Groups (NSGs) and Inspecting Network Protocol Steps</h2>

- Create sample file shares with various permissions. *PICTURE NOT INCLUDED*

<p>
Connect/log into DC-1 as your domain admin account (mydomain.com\[insert administrator username]). 84 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Connect/log into Client-1 as a normal user (mydomain\[insert the username of a randomly generated user of your choice]. 
  
<p>
Within Active Directory Users and Computers, click on mydomain.com’s drop down menu. Select “_EMPLOYEES” from mydomain.com’s drop down menu. Then, choose a user. 85 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Login 
  
<p>
Login as the user you have selected. 86 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- On DC-1, in the C:\ drive, create 4 folders: “read-access,” “write-access,” “no-access,” and “accounting.” *PICTURE NOT INCLUDED*
  
<p>
DC-1, in the C:\ drive, folder: read-access 87 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
  
<p>
DC-1, in the C:\ drive, folder: write-access 88 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
  
<p>
DC-1, in the C:\ drive, folder: no-access 89 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
  
<p>
DC-1, in the C:\ drive, folder: accounting 90 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Properties
  
<p>
Right click on the “read-access” folder. Select Properties from the drop down menu. 91 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button. 92 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Domain Users
  
<p>
Type “Domain Users” in the search box. 93 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Add
  
<p>
Click the Add button. 94 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Permission Level
  
<p>
The Permission Level will default to “Read,” so click the Share button. 95 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Done
  
<p>
Click the Done button. 96 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Close
  
<p>
Click the Close button. 97 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Properties
  
<p>
Right click on the “write-access” folder. Select Properties from the drop down menu. 98 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button. 99 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Domain Users
  
<p>
Type “Domain Users” in the search box. 100 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Add
  
<p>
Click the Add button. 101 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option. 102 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Share 
  
<p>
Click the Share button. 103 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Done
  
<p>
Click the Done button. 104 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Close
  
<p>
Click the Close button. 105 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Properties
  
<p>
Right click on the “no-access” folder. Select Properties from the drop down menu. 106 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button. 107 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Domain Admins
  
<p>
Type “Domain Admins” in the search box. 108 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Add
  
<p>
Click the Add button. 109 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option. 110 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Share
  
<p>
Click the Share button. 111 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Done
  
<p>
Click the Done button. 112 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Close
  
<p>
Click the Close button. 113 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Attempt to access file shares as a normal user.
  
<p>
In Client-1, open File Explorer. 114 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

<p>
Within the search bar type, “\\dc-1. Then, click “Enter” 115 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
  
<p>
Try to access the folders you just created. Which folders can you access? Which folders can you create stuff in? 116 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Example
  
<p>
For example, in the “write-access” folder you should be able to create a file within this folder. 117 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Active Directory Users and Computers
  
<p>
Within Active Directory Users and Computers, the mydomain.com option should be visible. 118 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- New
  
<p>
Right click on mydomain.com and select New from the drop down menu. 119 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Organizational Unit
  
<p>
Then, click on the Organizational Unit option. 120 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Security Groups
  
<p>
Type “_SECURITY_GROUPS” in the name box. Then, click the OK button. 121 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- mydomain.com
  
<p>
Right click on “mydomain.com” within Active Directory Users and Computers. 122 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Refresh
  
<p>
Within mydomain.com’s drop down menu select the Refresh. 123 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Security Groups
  
<p>
Right click on _SECURITY_GROUPS. 124 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- New
  
<p>
Select “New” from _SECURITY_GROUPS’ drop down menu. 125 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Group
  
<p>
Click on Group. 126 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Accountants
  
<p>
Add “ACCOUNTANTS” to the Group Name section. The Group Type is defaulted to “Security Group.” Then, click the OK button. 127 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Create an “ACCOUNTANTS” Security Group, assign permissions, and test access. 

- Properties
  
<p>
In Windows (C:) right click the “accounting” folder. Then, select Properties from the drop down menu. 128 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button. 129 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- ACCOUNTANTS
  
<p>
Type “ACCOUNTANTS” in the search box. 130 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Add
  
<p>
Click the Add button. 131 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option. 132 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Share 
  
<p>
Click the Share button. 133 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Done
  
<p>
Click the Done button. <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Close
  
<p>
Click the Close button. <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Accounting Folder
  
<p>
Go back to Client-1 and as the randomly generated user of your choice, try to access the accounting folder. *PICTURE UNAVAILABLE* <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- dc-1
  
<p>
Within File Explorer type “\\dc-1” to access the shared items. 136 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

<p>
Double click on the “accounting” folder. It should fail. 137 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Log out of Client-1 as the randomly generated user that you selected. *PICTURE UNAVAILABLE*

- DC-1
In DC-1, make [a randomly generated user of your choice] a member of the “ACCOUNTANTS” Security Group. 138

- Security Groups
  
<p>
Within “_SECURITY_GROUPS” click on ACCOUNTANTS. 139 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Members
  
<p>
Select the Members tab. 140 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Add
  
<p>
Click the Add button. 141 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Object Names
  
<p>
Enter the username of a randomly generated user of your choice. Click the Check Names and OK buttons, respectively. 142 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Apply and OK
  
<p>
Click the Apply and OK buttons, respectively. 143 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Sign back in
  
<p>
Go back to Client-1 as the randomly generated user that you previously selected. 144 <img 

- Accounting
  
<p>
Try to access the “accounting” share in File Explorer via \\DC-1\. Does it work now? 145 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
  
<p>
The accounting folder should now be accessible to the randomly generated user that you selected. 146 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Header
  
<p>
Text and place photo here <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Header
  
<p>
Text and place photo here <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
