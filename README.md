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

- Create sample file shares with various permissions.

<p>
Connect/log into DC-1 as your domain admin account (mydomain.com\[insert administrator username]). <img src="https://imgur.com/Q156ssu.png">
</p>
<p>

- Connect/log into Client-1 as a normal user (mydomain\[insert the username of a randomly generated user of your choice]. 
  
<p>
Within Active Directory Users and Computers, click on mydomain.com’s drop down menu. Select “_EMPLOYEES” from mydomain.com’s drop down menu. Then, choose a user. <img src="https://imgur.com/LymBYkP">
</p>
<p>

- Login 
  
<p>
Login as the user you have selected. <img src="https://imgur.com/j5IBzhx.png">
</p>
<p>

- On DC-1, in the C:\ drive, create 4 folders: “read-access,” “write-access,” “no-access,” and “accounting.”
  
<p>
DC-1, in the C:\ drive, folder: read-access <img src="https://imgur.com/zXQ5bnV.png">
</p>
<p>
  
<p>
DC-1, in the C:\ drive, folder: write-access <img src="https://imgur.com/lpEQ1A2.png">
</p>
<p>
  
<p>
DC-1, in the C:\ drive, folder: no-access <img src="https://imgur.com/dLBJNRb.png">
</p>
<p>
  
<p>
DC-1, in the C:\ drive, folder: accounting <img src="https://imgur.com/nPTyejh.png">
</p>
<p>

- Properties
  
<p>
Right click on the “read-access” folder. Select Properties from the drop down menu. <img src="https://imgur.com/b22rg0u.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button. <img src="https://imgur.com/ztKAdCS.png">
</p>
<p>

- Domain Users
  
<p>
Type “Domain Users” in the search box. <img src="https://imgur.com/QrpgvxW.png">
</p>
<p>

- Add
  
<p>
Click the Add button. <img src="https://imgur.com/URg45Gl.png">
</p>
<p>

- Permission Level
  
<p>
The Permission Level will default to “Read,” so click the Share button. <img src="https://imgur.com/CB0ZeFK.png">
</p>
<p>

- Done
  
<p>
Click the Done button. <img src="https://imgur.com/G2TzJVo.png">
</p>
<p>

- Close
  
<p>
Click the Close button. <img src="https://imgur.com/yyo9fU2.png">
</p>
<p>

- Properties
  
<p>
Right click on the “write-access” folder. Select Properties from the drop down menu. <img src="https://imgur.com/JEk0QLv.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button. <img src="https://imgur.com/vaR0uOY.png">
</p>
<p>

- Domain Users
  
<p>
Type “Domain Users” in the search box. <img src="https://imgur.com/JcNloB2.png">
</p>
<p>

- Add
  
<p>
Click the Add button. <img src="https://imgur.com/E35BboL.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option.<img src="https://imgur.com/0xAccju.png">
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
In DC-1, make the randomly generated user that you selected a member of the “ACCOUNTANTS” Security Group. *PICTURE UNAVAILABLE*

- Security Groups
  
<p>
Within “_SECURITY_GROUPS” click on ACCOUNTANTS. 138 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Members
  
<p>
Select the Members tab. 139 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Add
  
<p>
Click the Add button. 140 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Object Names
  
<p>
Enter the username of a randomly generated user of your choice. Click the Check Names and OK buttons, respectively. 141 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Apply and OK
  
<p>
Click the Apply and OK buttons, respectively. 142 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>

- Sign back in
  
<p>
Go back to Client-1 as the randomly generated user that you previously selected. 143 <img 

- Accounting
  
<p>
Try to access the “accounting” share in File Explorer via \\DC-1\. Does it work now? 144 <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
  
<p>
The accounting folder should now be accessible to the previously generated user that you selected. 145 <img src="https://i.imgur.com/DJmEXEB.png">
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
