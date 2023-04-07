# Network Security Groups (NSGs) and Inspecting Network Protocols
<p align="center">
<img src="https://imgur.com/rWWmatS.png" alt="windows logo"/>
</p>

This tutorial outlines network security groups (NSGs) and inspecting network protocols.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory
- Network Security Groups

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
Connect/log into DC-1 as your domain admin account (mydomain.com\[insert administrator username]).<img src="https://imgur.com/Q156ssu.png">
</p>
<p>

- Connect/log into Client-1 as a normal user (mydomain\[insert the username of a randomly generated user of your choice]. 
  
<p>
Within Active Directory Users and Computers, click on mydomain.com’s drop down menu. Select “_EMPLOYEES” from mydomain.com’s drop down menu. Then, choose a user to login as.<img src="https://imgur.com/91jcX5T.png">
</p>
<p>

- Login 
  
<p>
<img src="https://imgur.com/j5IBzhx.png">
</p>
<p>

- Create Four Folders: Read-Access, Write-Access, No-Access, and Accounting
  
<p>
First, in DC-1, in the C:\ drive, create folder: "read-access." <img src="https://imgur.com/zXQ5bnV.png">
</p>
<p>
  
<p>
Then, in DC-1, in the C:\ drive, create folder: "write-access." <img src="https://imgur.com/lpEQ1A2.png">
</p>
<p>
  
<p>
Next, in DC-1, in the C:\ drive, create folder: "no-access." <img src="https://imgur.com/dLBJNRb.png">
</p>
<p>
  
<p>
Followed by, in DC-1, in the C:\ drive, create folder: "accounting." <img src="https://imgur.com/nPTyejh.png">
</p>
<p>

- Properties
  
<p>
Right click on the “read-access” folder. Select Properties from the drop down menu.<img src="https://imgur.com/b22rg0u.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Sharing button.<img src="https://imgur.com/ztKAdCS.png">
</p>
<p>

- Domain Users
  
<p>
Type “domain users” in the search box. Then, click the Add button. <img src="https://imgur.com/QrpgvxW.png">
</p>
<p>

- Permission Level
  
<p>
The Permission Level will default to “Read,” so click the Share button.<img src="https://imgur.com/CB0ZeFK.png">
</p>
<p>

- Done
  
<p>
Then, click the Done button. <img src="https://imgur.com/G2TzJVo.png">
</p>
<p>

- Close
  
<p>
Afterward, click the Close button to close the Properties window. <img src="https://imgur.com/yyo9fU2.png">
</p>
<p>

- Properties
  
<p>
Right click on the “write-access” folder. Select Properties from the drop down menu.<img src="https://imgur.com/JEk0QLv.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Share button to share the folder.<img src="https://imgur.com/vaR0uOY.png">
</p>
<p>

- Domain Users
  
<p>
Type “domain users” in the search box. Then, click on the Add button. <img src="https://imgur.com/JcNloB2.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option. Next, click the Share button. <img src="https://imgur.com/0xAccju.png">
</p>
<p>

- Done
  
<p>
Then, click the Done button. <img src="https://imgur.com/2Bb6R93.png">
</p>
<p>

- Close
  
<p>
Afterward, click the Close button to close the Properties window. <img src="https://imgur.com/az75AR9.png">
</p>
<p>

- Properties
  
<p>
Right click on the “no-access” folder. Select Properties from the drop down menu.<img src="https://imgur.com/pd7u5qi.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Share button to share the folder. <img src="https://imgur.com/xGL0ni0.png">
</p>
<p>

- Domain Admins
  
<p>
Type “domain admins” in the search box. Then, click the Add button. <img src="https://imgur.com/AP9ekue.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option. Then, click the Share button. <img src="https://imgur.com/j4QxUmG.png">
</p>
<p>

- Done
  
<p>
Next, click the Done button. <img src="https://imgur.com/RsE8SLx.png">
</p>
<p>

- Close
  
<p>
Afterward, click the Close button to close the Properties window. <img src="https://imgur.com/M1H5AvY.png">
</p>
<p>

- Attempt to access file shares as a normal user.
  
<p>
In Client-1, open File Explorer.<img src="https://imgur.com/mhuwMDU.png">
</p>
<p>

<p>
Within the search bar type, “\\dc-1. Then, click “Enter”<img src="https://imgur.com/0K75mEL.png">
</p>
<p>
  
<p>
Try to access the folders you just created. Which folders can you access? Which folders can you create stuff in?<img src="https://imgur.com/UPEjlpO.png">
</p>
<p>

- Example
  
<p>
For example, in the “write-access” folder you should be able to create a file within this folder.<img src="https://imgur.com/TB0wYuA.png">
</p>
<p>

- Active Directory Users and Computers
  
<p>
Within Active Directory Users and Computers, the mydomain.com option should be visible.<img src="https://imgur.com/91jcX5T.png">
</p>
<p>

- New
  
<p>
Right click on mydomain.com and select New from the drop down menu.<img src="https://imgur.com/IuDYW7A.png">
</p>
<p>

- Organizational Unit
  
<p>
Then, click on the Organizational Unit option.<img src="https://imgur.com/UdES8Ak.png">
</p>
<p>

- Security Groups
  
<p>
Type “_SECURITY_GROUPS” in the name box. Then, click the OK button.<img src="https://imgur.com/032kPU9.png">
</p>
<p>

- mydomain.com
  
<p>
Right click on “mydomain.com” within Active Directory Users and Computers.<img src="https://imgur.com/Wz618Zx.png">
</p>
<p>

- Refresh
  
<p>
Within mydomain.com’s drop down menu select the Refresh option.<img src="https://imgur.com/K9f10ad.png">
</p>
<p>

- Security Groups
  
<p>
Right click on _SECURITY_GROUPS.<img src="https://imgur.com/sr4hdL5.png">
</p>
<p>

- New
  
<p>
Select “New” from _SECURITY_GROUPS’ drop down menu.<img src="https://imgur.com/utamT8S.png">
</p>
<p>

- Group
  
<p>
Click on Group.<img src="https://imgur.com/TyKztys.png">
</p>
<p>

- Accountants
  
<p>
Add “ACCOUNTANTS” to the Group Name section. 
<p>
The Group Type is defaulted to “Security Group,” so click on the OK button. <img src="https://imgur.com/SDbIDqC.png">
</p>
<p>

- Create an “ACCOUNTANTS” Security Group, Assign Permissions, and Test Access 

- Properties
  
<p>
In Windows (C:) right click the “accounting” folder. Then, select Properties from the drop down menu.<img src="https://imgur.com/3sgE1Zt.png">
</p>
<p>

- Sharing
  
<p>
Select the Sharing tab. Then, click on the Share button to share the folder. <img src="https://imgur.com/KJt65yx.png">
</p>
<p>

- ACCOUNTANTS
  
<p>
Type “ACCOUNTANTS” in the search box. Then, Click the Add button. <img src="https://imgur.com/8Zf7pSI.png">
</p>
<p>

- Permission Level
  
<p>
Within the Permission Level section select the “Read/Write,” option. Then, click the Share button. <img src="https://imgur.com/4ylrOta.png">
</p>
<p>

- Done
  
<p>
Next, click the Done button. <img src="https://imgur.com/3HPK96n.png">
</p>
<p>

- Close
  
<p>
Afterward, click the Close button to close the Properties window. <img src="https://imgur.com/zgo4N2D.png">
</p>
<p>

- Accounting Folder
  
<p>
Go back to Client-1 and as the randomly generated user of your choice and try to access the accounting folder.
</p>
<p>

- DC-1
  
<p>
Within File Explorer type “\\dc-1” to access the shared items.<img src="https://imgur.com/qJE3RE6.png">
</p>
<p>

<p>
Double click on the “accounting” folder. It should fail.<img src="https://imgur.com/pYq8v6f.png">
</p>
<p>

- Log out of Client-1 as the randomly generated user that you selected.

- DC-1

<p>
In DC-1, make the randomly generated user that you selected a member of the “ACCOUNTANTS” Security Group.
</p>
<p>
    
- Security Groups
  
<p>
Within “_SECURITY_GROUPS” click on ACCOUNTANTS.<img src="https://imgur.com/1oZQeqO.png">
</p>
<p>

- Members
  
<p>
Then, select the Members tab, followed by the Add button to add a member.<img src="https://imgur.com/auFkf8h.png">
</p>
<p>

- Object Names
  
<p>
Next, type in the username of the randomly generated user that you selected. Then, continue by clicking on the Check Names and OK buttons, respectively. <img src="https://imgur.com/KlpbfMw.png">
</p>
<p>

- Apply and OK
  
<p>
Afterward, click on the Apply and OK buttons, respectively. <img src="https://imgur.com/Frl7Dzj.png">
</p>
<p>

- Sign Back In
  
<p>
Go back to Client-1 as the randomly generated user that you previously selected.<img src="https://imgur.com/IUME0Yy.png">

- Accounting
  
<p>
Try to access the “accounting” share folder in File Explorer via \\dc-1\. Does it work now?<img src="https://imgur.com/hSyLLZd.png">
</p>
<p>
  
<p>
The accounting folder should now be accessible to the previously generated user that you selected.<img src="https://imgur.com/3rFI9Av.png">
</p>
<p>
