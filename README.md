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

<h2>Deployment and Configuration Steps</h2>

<h3> Open a VM using Windows 2022 </h3>

<p>
 <h4> Step 1: Create VMs </h4>
  - From my Azure Subscription, I created a Resource Group. Then create a VM (Virtual Machine) with at least one VM running Windows 2022. 
  
  - I created 1 Vm running Window 2022 for the Main Domain and 1 VM running Windows 10 to connect to the Domain and test ipconfig /all to ensure that both IP Address matches with the private server. Once I was completed Log into BOTH Windows and navigated to Windows 2022.

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

<p> <img width="600" alt="Image" src="https://github.com/user-attachments/assets/5f300f6b-cdba-49c0-870e-6866cbedbb9a"
</p>
<p>
Before installing the Active Directory feature make sure to check the box for automatic restart after installation is completed. If the VM doesn't restart then manuelly restart the VM as shown below:
</p>

<p> <img width="600" alt="Image" src="https://github.com/user-attachments/assets/9dad16dc-e234-4b54-b605-14d11b51ecc0" </p>
<br />
<p>
After logging back into the VM (Win 2022) on the Server Manager there will be a white flag with an Alert on it. Click on the "Promote this server into a Domain Controller".
</p>
<P> <img width="600" alt="Image" src="https://github.com/user-attachments/assets/d61ba61b-9d32-4111-a48d-92e0c362fc53" </P>
<br />

<p>
 I Added a New Forest because we didn't have any pre-extisting ones that I could've added a Controller or another Domain to. Then named the Domain and provide a password (Copy password into a Notepad/text.file) We could select older version depending on the VM model the company is using but the standard is what's recommend (win 2016v).

 Note: A Forest can hold multiple Domains in it's infrastructure.
</p>

<p> <img width="600" alt="Image" src="https://github.com/user-attachments/assets/49fbdcc9-7876-4a07-8e46-b96d96e1bf6b" </p>

<P> <h4> Continue on... </h4></P>

<p> <img width="600" alt="Image" src="https://github.com/user-attachments/assets/0ae447f3-516d-430e-80a9-90077f3f5a45"
</p>
<p>
Lastly after all the installation has been completed, I restarted the VM (win 2022). Congrats! Active Dictory should be successfully installed. 

- Now I remotely Logged back into VM but using the Domain name I named it "\" username for VM (win 2022) and Password I set for the Domain, just as shown in the example below. 
</p>
<br />
<p>
<img width="898" alt="Image" src="https://github.com/user-attachments/assets/c67306f7-236a-4a78-a45d-0cf5643c7b42" />
</p>

<p> 
<h4> Create a Domain Admin user within the domain </h4>
—
Find Active Directory Users and Computers (ADUC) within the Windows Menu, I got to create an Organizational Unit (OU) called “_EMPLOYEES” and another called “_ADMINS”

 Create a new employee named “Jane Doe” (same password) with the username of “jane_admin” / Cyberlab123!
Add jane_admin to the “Domain Admins” Security Group
Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”
User jane_admin as your admin account from now on
</p>
