<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>High-level Steps</h2>

- Step 1: Configure Roles
- Step 2: Configure Departments
- Step 3: Configure Teams
- Step 4: Configure Agents
- Step 5: Configure Users
- Step 6: Configure Service Level Agreement (SLA)
- Step 7: Configure Help Topics

<h2>Configuration Steps</h2>

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/8392a3b2-600a-4dca-ab1c-36cfb6139540">
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/588e80ac-f228-4f0b-960b-72eca709cc30">
</p>
<p>
1. Configure Roles: Continuing from the Pre-Installation osTicket lab, login to your osTicket using the User Admin credentials. *Take note that in the top right corner of the screen, you have an option to move from 'Admin Panel' to 'Agent Panel'. We'll start in the 'Admin Panel' meaning the 'Agent Panel' hyperlink will be visible.* Moving forward, following this string of actions: select 'Agents' tab > select 'Roles' tab (underneath) > click 'Add New Role' button > enter name as 'Supreme Admin'> click on 'Permissions' tab > under 'Tickets' tab, check all boxes > do the same for 'Tasks' tab and 'Knowledgebase' tab > click 'Add Role'.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/113b3d22-8851-4944-83a8-5bcedc201ebf">
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/a3e641e6-e0e7-4a8e-a9d2-15db0922f3e0">
</p>
<p>
2. Configure Departments: Using a similar string of actions, create a new department named 'Sytem Administrators'. Starting from the top: 'Agents' tab > select 'Departments' tab (underneath) > click 'Add New Department' > enter name as "System Administrators' > click 'Create Dept'. *We'll keep the default settings.*
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/ffcddc26-de64-43f8-b92b-466a184133b3">
</p>
<p>
3. Configure Teams: Next we will create a new team named 'Level II Support'. Teams can be compiled of Agents from multiple departments. Just like Roles and Departments, begin with the 'Agents' tab > select 'Teams' tab (underneath) > click 'Add New Team' button > enter name as 'Level II Support' > click 'Create Team'. *We'll keep the default settings as well.*
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/e9270fe9-9744-4949-9f75-d6d95374ad7e">
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/4363b505-4a8b-4843-af34-5be0ad429d8e">
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/94066453-85b9-4f8d-b59a-c72e994eb3c3">
</p>
<p>
4. Configure Agents: This portion we will create 2 new Agents (helpdesk workers) by the name of Jane Doe and John Doe. Begin at the top: 'Agents' tab > click 'Agents' tab (underneath) > click 'Add New Agent' button > fill-in the appropriate fields (i.e. Name, Email Address, Username and Set Password) on the 'Account' page. *Remember to keep track of the credentials entered so you can later login as each agent.* Moving along, click on 'Access' tab > assign Jane to 'System Administrators' department and assign her as a 'Supreme Admin' role > skip 'Permissions' tab and go to 'Teams' tab > assign Jane to 'Level II Support' > click 'Create'. Lastly, add John Doe as an Agent by following the same steps, except assign John different roles/settings so you can observe the difference between both Agents' access and permissions.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/1b01ddc2-e460-4bc0-a252-90eae679ba63">
</p>
<p>
5. Configure Users: For this section, we'll create 2 new users, i.e Karen and Ken. Begin with switching to the 'Agent Panel' located in the top right corner. Click on the 'Users' tab and click 'Add New User'. Fill-in the required fields: Email Address and Full Name. 
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/60098dcc-0e55-4a2d-8f67-d6efd322b354">
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/fbf94c77-d568-4f00-8cf4-639cab2a2d02">
</p>
<p>
6. Configure SLA: For the next step, switch back to the 'Admin Panel' > select 'Manage' tab > click 'SLA' tab (underneath) > 'Add New SLA Plan'. We'll create 3 new SLA plans with the following settings: SEV-A (Grace Period: 1 hour, Schedule: 24/7), sev-b: (Grace Period: 4 hours, Schedule: 24/7) SEV-C: (Grace Period: 8 hours Schedule: Business Hours)
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/post-install-config/assets/144288806/4552c905-9244-40a7-9145-50e7535e4d1c">
</p>
<p>
7. Configure Help Topics: For this last section, we will add a few common help desk topics in addition to the default options provided in osTicket. Starting from the top: 'Manage' tab > 'Help Topics' tab (underneath) > click on 'Add New Help Topic' button. We'll create 4 more topics named: 'Business Critical Outage', 'Personal Computer Issues', 'Equiptment Request' and 'Password Reset'. 
</p>
<br />

<h2>osTicket Configurations Complete </h2>

Now that the configurations are all set, we'll be able to utilize osTicket as a proper ticketing system. In the next lab, we'll practice creating tickets as Users (Karen and Ken) and resolving help desk tickets as Agents (Jane and John)
