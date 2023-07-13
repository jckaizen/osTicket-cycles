<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP 7.3.8
- HeidiSQL 12.3.0
- MySQL 5.5.62
- PHPManagerForIIS 1.5.0
- IIS URL Rewrite Module 2.0
- Microsoft Visual C++ Redistributable x86 (2015-2022)

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/0addb192-9abb-46ab-89c0-c19efefc9a77" width="40%" alt="Creation of Azure VM"/>
</p>
<p>
Create a simple Windows 10 VM in Azure to install osTicket (also create a new resource group while making the VM). Two CPU cores are sufficient for tutorial. Make sure to write down your username and password for this VM.
</p>
<br/>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/7e00876c-413d-4a1e-ab66-3065a0ecd823" width="60%" alt="Remminna Remote Desktop"/>
</p>
<p>
Next, we will remote into the VM using RDP (remote desktop protocol). Since I'm using Linux, I will use Remmina for my remote desktop client. If you're on Windows, you can just use the built-in remote desktop application. MacOS will need a third-party client just like Linux.
</p>
<p>
  Create a new RDP connection and plug in the public IP of your VM (you can obtain this by going to the main page of your VM in Azure and copy it) and the username and password when you created first created your VM.
</p>
- <br />

<p>
- <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
- <br />
