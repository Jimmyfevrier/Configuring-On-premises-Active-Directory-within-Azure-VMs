<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://youtu.be/yQtI8JdbNqM?si=SO6NRrMEad5Z1f2d)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Open a VM using Windows 2022
- Installaltion
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<h3> Open a VM using Windows 2022 </h3>

<p>
 <h4> Step 1: Create VMs </h4>
  - From my Azure Subscription, I created a Resource Group. Then create a VM (Virtual Machine) with at least one VM running Windows 2022. 
  
  - I created 1 Vm running Window 2022 and 1 VM running Windows 10. Once I was completed Log into BOTH Windows and navigated to Windows 2022.

    Note: will need at least one more VM to connect to the VM running Window 2022 (at as Domain).

<h4> Step 2: Remote Access Vms </h4>

- I remote access the VMs on my Macbook Pro using the Microsoft Remote Desktop App.
</p>
<p> <img width="609" alt="Image" src="https://github.com/user-attachments/assets/7322975d-7869-4ed5-8009-aac685afdc2e" /> 


Note: Remember to save all passwords in a notepad or text.file </p>

<p> <h2> Installaltion </h2></p>

<p> 
 From the Server Manager I click on the Manage tool to Add Roles and Features and begone to install  the Active Directory features as shown below. 
 </p>

<p><img src="https://github.com/user-attachments/assets/5f300f6b-cdba-49c0-870e-6866cbedbb9a"
</p>
<p>
Before installing the Active Directory feature make sure to check the box for automatic restart after installation is completed. If the VM doesn't restart then manuelly restart the VM as shown below:
</p>

<p> <img src="https://github.com/user-attachments/assets/9dad16dc-e234-4b54-b605-14d11b51ecc0" </p>
<br />
<p>
After logging back into the VM (Win 2022) on the Server Manager there will be a white flag with an Alert on it. Click on the "Promote this server into a Domain Controller".
</p>
<P> <img width="456" alt="Image" src="https://github.com/user-attachments/assets/d61ba61b-9d32-4111-a48d-92e0c362fc53" </P>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png](https://github.com/user-attachments/assets/69e8a42c-efae-4da2-afc6-caa8571b02bd)" height="60%" width="60%" alt="Disk Sanitization Steps"
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
