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

- Header
  
<p>
Text and place photo here <img src="https://i.imgur.com/DJmEXEB.png">
</p>
<p>
