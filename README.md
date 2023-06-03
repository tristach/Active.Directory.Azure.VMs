# Active.Directory.Azure.VMs

<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Azure Setup: Create two VMs.  One with Windows server "AD", one Windows 10 "Client-1".  Adjust the firewall on AD and test for connectivity.
- Install Active Directory:  Create new Active Directory Domain Services on DC, create new forest, promote to DC, create new user, login again as new user.
- Create New Accounts and Users in AD:  Create three new OUs: ADMINS, EMPLOYEES and CLIENTS.  Add a new employee to the security group.
- Join Windows 10 to Domain:  Go to Azure and set Windows and set Client-1 to DC's private IP address.  Check DC for confirmation.
- Setup Remote Desktop for Non-Administrative Users: Log into Client-1 as new employee.  Allow "domain users" access.  
- Create New User and Log Into Client 1:  Log into DC with new employee.  Use PowerShell to create new employees.  Log into Client-1 with new user.  

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/kyTDfkX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Adjusted firewall on DC-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/0vFTJN7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Can now ping DC-1 as firewall has been adjusted.
</p>
<br />

<p>
<img src="https://i.imgur.com/UfQtSbh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create an AD with wizard on DC-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/MLA0gGp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Promote to domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/GS7Foju.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created three new OUs in ADUC.  Have created generic employee John Snow and made member of admins group.
</p>
<br />

<p>
<img src="https://i.imgur.com/rtmGnJA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
John Snow is now able to login to DC.
</p>
<br />

<p>
<img src="https://i.imgur.com/CnadiTs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Changed Client-1's network to private IP of DC through Azure.
</p>
<br />

<p>
<img src="https://i.imgur.com/bFNbuGb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Joined Client-1 to domain and gave John Snow ability to log into Client-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/VP5lYzr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Adjusted permissions so all domain users can now access Client-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/Sa6vawk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Confirmed on DC, Johns Snow and all domain users l users now able to access Client-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/1Mq8AUb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ran a program in PowershellISE to create random user names.
</p>
<br />

<p>
<img src="https://i.imgur.com/LFBhrEb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Hundreds of random user names created (and one I made manually named Harry Potter).
</p>
<br />

<p>
<img src="https://i.imgur.com/l10J4mS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Client-1 command line shows user Harry Potter can now access Client-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
