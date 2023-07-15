<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Create a role for "Supreme Admin"
- Create a system adminstrator department
- Create a level 1 and level 2 support teams
- Create new agents
- Create new users
- Configure multiple SLA (service level agreement)
- Configure multiple "Help Topics"

<h2>Configuration Steps</h2>


<p>
Login into the admin account you created at installation of osTicket. <a href ="http://localhost/osTicket/scp/login.php">The link to the helpdesk.</a>
</p>
<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/5041dc8a-b910-4c2c-a748-074bf1f4f401" width="40%"/>
</p>

<p>Go to Admin Panel then under Agents->Roles and add a new role. Name it "Supreme Admin" and tick <b>all</b> permissions for it and save.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/ac21be53-2fb7-4417-b64d-1fe20d00e5ad" width="40%"/>
</p>

<p>
Next, under Agents->Departments and click "Add New Department". We will name this department "System Adminstrators" and click add.
</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/ef234e06-37e4-4764-8f5e-f5ee071b3427" width="40%"/>
</p>

<p>
Teams allows you to bring people from multiple department to work together on specific tickets or help topics. So we will create support teams. Under Agents->Teams, click "Add New Team". Name it "Level II Support" and click "Create team". Level I Support is already created.
</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/f0a3d622-e4bf-45b1-93e9-3503ccfadd22" width="40%"/>
</p>

<p>You can have the option to require an account to make a ticket(in terms of the end user). Under Settings->Users, the option is called "Registration Required" and you enable or disable the ability to do so. We'll just leave it unchecked.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/9715133c-b2c1-480b-b142-37953f91d597" width="40%"/>
</p>

<p>Next, we will create a new agent. Agents are the people who work on the tickets. Under Agents->Agents, click on "Add Agent" and put in the full name and email of the agent. Then give the agent an username and password. Uncheck to reset the password when the agent logs in next time for this demonstration. In the access part, we'll make this agent an System Adminstrator so they belong to the System Adminstrator department. Click create.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/d9e2eabb-16f8-479e-a85e-d23538fa92f2" width="40%"/>
</p>
<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/83c1fafd-b7fd-463b-88e2-34d9ca01a49f" width="40%"/>
</p>

<p>Now we will create the end users of the help desk. Under Users->User Directory, click "Add User". then put in the full name and email address of the user. Click create. </p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/265e1e8d-a71f-4d8a-82dc-5fc1d766cc64" width="40%"/>
</p>

<p>SLAs (servive level agreements) specify the severity of a ticket and how much time an agent is expected to work on it and when. Under Manage->SLA, we will add 3 SLAs: Sev-A, Sev-B, and Sev-C. Click on "Add New SLA Plan", put in the name then give each Sev their appropriate grace period and duration. So Sev-A will be 1 hour, 24/7. Sev-B will be 4 hours, 24/7. Sev-C will be 8 hours, business hours.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/2ba6521c-9d46-417c-b5c7-61ffbe3139aa" width="40%"/>
</p>

<p>Help Topics are what end users use to generalize what their issues are about. For example, if an user needs a password reset, then they will pick "Password Reset" and put in more details in the description. Under Manage->Help Topics, we will create:</p>

- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset

<p>When creating them, you can select the priority and what department will handle those specific tickets.</p>

<p>
<img src="https://github.com/jckaizen/osTicket-cycles/assets/57122203/675bac14-e6a2-41a4-919a-4371b8edfc3d" width="40%"/>
</p>

<p>A lot more things can be setup in the Admin Panel (autoresponders, templates, etc), but these are just the basics to starting a help desk system.</p>
