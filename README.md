<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)



<h2>Deployment and Configuration Steps</h2>

<p>
<img src=https://i.imgur.com/EmwVawG.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create the Domain Controller VM (Windows Server 2022) named “DC-1”
 and Create the Client VM (Windows 10) named “Client1
</p>
<br />

<p>
<img src="https://i.imgur.com/m8bCVjo.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ensure Connectivity between the client and Domain Controller
Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping -t <ip address> (perpetual ping)
</p>
<br />

<p>
<img src="https://i.imgur.com/Vp22QNM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Login to DC-1 and install Active Directory Domain Services

</p>
<br />


<p>
<img src="https://i.imgur.com/YZMbndN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Promote as a DC: Setup a new forest as mydomain.com 
Restart and then log back into DC-1 as user: mydomain.com\user123
</p>
<br />


<p>
<img src="https://i.imgur.com/ZseP5OQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create an Admin and Normal User Account in Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES” then
Create a new OU named “_ADMINS".


</p>
<br />


<p>
<img src="https://i.imgur.com/5JTb1og.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Add jane_admin to the “Domain Admins” Security Group

</p>
<br />

<p>
<img src="https://i.imgur.com/vbdVYQy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Login to DC-1 as jane_admin
Open PowerShell_ise as an administrator
Create a new File and paste the contents of the script into it.
 Run the script and observe the accounts being created
<br />

This concludes the tutorial.
