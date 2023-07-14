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
<br/>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/6c31da46-d046-4e09-a9ac-9a2c8017d237" width="50%" alt="Turn Windows features on or off"/>
</p>
<p>
Once you are connected, go to Windows features and enable:
</p>

- <b>IIS Management Console</b> (Internet Information Services -> Web Management Tools -> <b>IIS management Console</b>)
- <b>All of "Common HTTP Features"</b> (Internet Information Services -> World Wide Web Services -> <b>Common HTTP Features</b>)
- <b>CGI</b> (Internet Information Services -> Application Development Features -> <b>CGI</b>)
<br />

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/eb43f21c-4791-48c3-beec-0cbd82ac7569" width="40%" alt="Windows Features"/>
</p>

<p>Next, we will download and install the following things from the internet:</p>

- PHP Manager for IIS
- IIS URL Rewrite Module
- Microsoft Visual C++ Redistributable x86
- MySQL (select typical setup. In configuration wizard (post-install), select standard configuration then create a password for the root account)
- PHP 7.3.8 (we'll just download this at this point)
- osTicket 1.15.8 (we'll just download this at this point)

<p>For the PHP install, make a folder called "PHP" directly on the C drive. Once done, unzip the contents of your downloaded PHP zip folder into the folder.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/09fb5fab-d385-4aab-be1d-f7d6806cdd54" width="40%" alt="C:\PHP folder"/>
</p>

<p>Open IIS as an Admin then go register PHP in PHP manager. The path of the file you're looking for is C:\PHP\php-cgi.exe. Reload the IIS server.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/91e0b876-a17b-4a07-b25c-321ef6659f0c" width="40%" alt="Windows Features"/>
</p>

<p>Unzip the osTicket folder you downloaded and copy the "upload" folder to C:\inetpub\wwwroot then rename "upload" to "osTicket".</p>

<p>The site should be running so go to IIS then under "Sites->Default Web Site" is an osTicket folder. Click on it then on the right side of IIS, click "Browse :*80" </p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/90a57c31-9337-4386-ad52-268e70e6cd16" width="20%" alt="Windows Features"/>
</p>
