# Network Security Groups NSGs and Inspecting Network Protocols
<p align="center">
<img src="https://imgur.com/rWWmatS.png" alt="windows logo"/>
</p>

This tutorial outlines the osTicket: post-installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Setup resources in Microsoft Azure (Azure) by:
Creating a Domain Controller (DC) Windows Server 2022 (Virtual Machine - VM) and naming it, “DC-1.”
Creating a Client VM (Windows 10) and naming it, “Client-1,” using the same Resource Group and Virtual Network (Vnet) as DC-1. 
- Ensure connectivity between the Client-1 and DC-1.
- Install Active Directory (AD)
- Create an Administrator and Normal User Account in Active Directory.
- Join Client-1 to your domain.
For example: mydomain.com
- Setup Remote Desktop for non-administrative users within Client-1.
- Create additional users and attempt to log into Client-1 as one of the users.


<h2>Post-Installation Steps</h2>

