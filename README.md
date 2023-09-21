<img width="790" alt="Screenshot 2023-09-21 164350" src="https://github.com/DJcaston76/post-install-config/assets/145403292/821fc1ef-6771-47fe-acf7-9e1ee6a155e2">

<h1>osTicket - Post-Install Configuration</h1>
This guide is a set up of the osTicket software 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machine
- Microsoft Remote Desktop
- Internet Information Services (IIS)
- osTicket Software

<h2>Operating System</h2>

- Windows 10, version 22H2

<h2>List of Prerequisites</h2>

- Setup & Configuration: [osTicket: Prerequisites and Installation](https://github.com/yeahglo/osticket-prereqs)
- Agent Login Page: http://localhost/osTicket/scp
- osTicket Documentation: https://docs.osticket.com/

<h2>Post-Install Configuration Objectives</h2>

- Define Roles, Departments, Teams and set permissions
- Create Agents and Users
- Create SLAs and Help Topics

<br/>

<img width="1280" alt="Screenshot 2023-09-21 163854" src="https://github.com/DJcaston76/post-install-config/assets/145403292/ca76f587-0802-434a-b34c-c4ab77d149d8">

**_Start by logging into the Agent Login Page for osTicket._** 

<br/>

**Step 1: Create a Role** - Roles determine levels of access.
- Navigage to Admin panel > Agents > Roles > Add New Role
- Name the role "Supreme Admin"
- Checkmark all permissions under Tickets, Tasks, and Knowledgebase

<br/>

<img width="1153" alt="Screenshot 2023-09-21 165015" src="https://github.com/DJcaston76/post-install-config/assets/145403292/b0d30ac9-27be-4884-a41c-c21358be3af2">

**_Create the Supreme Admin Role._**

<img width="1096" alt="Screenshot 2023-09-21 165241" src="https://github.com/DJcaston76/post-install-config/assets/145403292/c55c5075-08c9-41f2-9e4a-8009c192c916">

**_Turn on all of these permissions. There are plenty of permissions under Tickets, Tasks, and Knowledgebase._**

<br/>

**Step 2: Create a Department** - Departments determine ticket routing.
- Navigage to Admin panel > Agents > Roles > Add New Department
- Name the department "System Administrators"
- Leave the defaults settings for now

<br/>

<img width="1200" alt="Screenshot 2023-09-21 165528" src="https://github.com/DJcaston76/post-install-config/assets/145403292/057f4b49-d40e-49cc-999b-a0b3f1301541">

**_Use the default settings for the Systems Administrators Department._**

<br/>

**Step 3: Create a Team** - Teams allow you to pull agents for specific use cases.
- Navigage to Admin panel > Agents > Roles > Add New Team
- Create a "Level II Support" _(Note: You already have a Level I as a default.)_

<br/>

<img width="1203" alt="Screenshot 2023-09-21 165823" src="https://github.com/DJcaston76/post-install-config/assets/145403292/32daf82c-3821-4558-9694-b3f63fe3a34a">

**_More settings can be configured at the Team level, including assigning a team lead or adding members as you set up the team._**

<br/>

**Step 4: Allow anonymous users to create tickets** - Doing this ensures users, aka "ticket owners", can create tickets easily.
- Admin Panel > Settings > User Settings > uncheck “Require registration and login to create tickets”

<br/>

<img width="1194" alt="Screenshot 2023-09-21 170146" src="https://github.com/DJcaston76/post-install-config/assets/145403292/ccc9a66c-d002-4a43-90c4-1efebcd4d430">

**_Review the setting to allow anonymous users to create tickets._**

<br/>

**Step 5: Create an Agent** - Agents are help desk professionals who work the tickets.
- Navigate to Admin Panel > Agents > Add New Agent
- Name the agent "Josh Evans"
- Add Josh's department as System Administrators
- Assign the Supreme Admin role for him
- Assign him to the Level II Support Team
- Add Support under the Extended Access so he can view/edit tickets

<br/>

<img width="1105" alt="Screenshot 2023-09-21 170556" src="https://github.com/DJcaston76/post-install-config/assets/145403292/ff2621d0-ddc9-492c-a505-e74f7e34d4d3">

**_The agent profile has many options to set access and permissions._**

<br/>

<img width="1207" alt="Screenshot 2023-09-21 171143" src="https://github.com/DJcaston76/post-install-config/assets/145403292/6b693842-b54d-4cd9-a94e-6746fb3e4f14">

**_Under the agent profile, osTicket lets you set and change the password as long as you have the permissions to change this._**

<br/>

**Step 6: Create a User** - Users create support tickets to get assistance from agents.
- Navigate to Agent Panel > Users > Add User _(Note: You can also import users)_
- Name the User "Dallas Young" and add an email for them

<br/>

<img width="1201" alt="Screenshot 2023-09-21 171517" src="https://github.com/DJcaston76/post-install-config/assets/145403292/60c41454-0d9a-43ad-a927-c8a20baf60f5">

**_Users are the ticket owners. It's possible to create them one by one, but you can also import them in bulk._**

<br/>

**Step 7: Create an SLA** - Service Level Agreements (SLAs) define what kind of response time and priority level is warranted for each ticket.
- Navigate to Admin Panel > Manage > SLA > Add New SLA Plan
- Name the SLA Plan "SEV-G" and set it on a 24/7 schedule with a 1-hour grace period

<br/>

<img width="1208" alt="Screenshot 2023-09-21 171928" src="https://github.com/DJcaston76/post-install-config/assets/145403292/8a866a06-e50b-4e9c-aba2-948773466114">

**_SLAs can be set up to define what kind of timeline each ticket has in order to remain compliant with the service contract._**

<br/>

**Step 8: Create a Help Topic** - Help Topics allow users to set a category for their ticket.
- Navigate to Admin Panel > Manage > Help Topics > Add New Help Topic
- Name the Help Topic "Personal Computer Issues"

<br/>

<img width="1243" alt="Screen Shot 2023-07-13 at 9 38 00 AM" src="https://github.com/yeahglo/post-install-config/assets/91516100/01c09ec5-eec5-4ec2-94b6-9601455c9f40">

**_Help Topics will be visible to users to assign to individual tickets. You can customize further under the "New Tickets options" and "Forms" tabs._**

<h2>Next Steps</h2>

Continue to the third part to create and work a ticket.
[Ticket Lifecycle](https://github.com/yeahglo/ticket-lifecycle)
