<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/> </p>

<h1>osTicket - Ticket Lifecycle</h1>
This guide demonstrates how to install and configure the open-source ticketing system osTicket (v1.15.8) on a Windows machine using IIS, PHP, and MySQL.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Prerequisites</h2>
Before starting, ensure the following environment is in place:

  - Azure Resource Group (example: osTicketRG)
  - Azure Virtual Machine (example: osticketVM)
    - Operating System: Windows 10 Pro, version 22H2 - x64 Gen2
    - Size: 4 vCPUs
  - Remote Desktop Access enabled (for connecting to the VM)
  - [osTicket Installation Files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

<h2>Installation Steps</h2>

<h3>0️⃣ Overview of osTicket Installation </h3>

- Enable Internet Information Services
- Install Web Platform Installer
- Install MySQL and Set Up Useranme and Password
- Install C++ Redistributable
- Congure Permissions and Install osTicket

🔐 Login URLs
Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php

End User Ticket Submission Page:
http://localhost/osTicket

📝 Ticketing Workflow Overview
Create tickets as an end-user.

Respond to tickets as a Help Desk Agent.

Set priorities, assign SLAs, and observe ticket visibility limitations.

Work tickets to resolution and review system behavior.

🔧 Initial Setup
✅ Change:
SysAdmins Department → Make it a Top-Level Department

❌ Delete:
Maintenance Department → Delete completely (do not archive)

🧪 Ticket Scenarios
📌 Ticket 1: Mobile/Online Banking System Down
Create as: End-user
Subject: Entire mobile/online banking system is down

Handle as: Agent John

Observe ticket properties: Priority, Department, SLA, Assigned To

Set:

SLA: Sev-A (1 hour, 24/7)

Department: Online Banking

Try to view/edit again as John. Can you?

Resolve as: Agent Jane

📌 Ticket 2: Adobe Upgrade Needed
Create as: End-user
Subject: Accounting department needs Adobe upgrade (broken)

Handle as: Agent John

Observe ticket properties

Set:

SLA: Sev-B (4 hours, 24/7)

Department: Support

Resolve the ticket as John

📌 Ticket 3: CFO’s Laptop Not Turning On
Create as: End-user
Subject: CFO’s laptop will no longer turn on

Handle as: Agent John

Observe ticket properties

Set:

SLA: Sev-B (4 hours, 24/7)

Department: Support

Resolve the ticket as John

🚨 Escalation Behavior
Set Sev-A (SysAdmins ticket) last.

Ticket becomes inaccessible to agent without permission.

Switch to Admin Panel → Assign View access to SysAdmins role.

Return to Agent Panel → Observe escalated ticket (now viewable, but not editable).

📬 Ticketing System Behavior
Most ticketing systems, including osTicket, support email notifications:

When a ticket is created or updated, the end user receives an email copy.

End users can reply via email, and their response gets attached to the ticket.

🧑‍💻 Real-World Ticket Intake
Tickets can come from:

Web forms

Email

Phone calls

Chat apps

In-person requests

💡 Even if you fix something on the spot, create a ticket. This helps with:

Tracking

Accountability

Metrics reporting

SLA compliance

🔁 Final Thoughts and Practice
Explore email configuration for better ticketing workflow.

Re-do the lab multiple times until it becomes second nature.

Mastery builds technical intuition—a core part of your technical skills pillar.

<h3>1️⃣ Install/Enable Internet Information Services (IIS) with CGI </h3>



<h3> 2️⃣ Install PHP Manager for IIS </h3>



<h3> 3️⃣ Install IIS Rewrite Module </h3>



<h3> 4️⃣ Setup PHP </h3>



<h3> 5️⃣ Install additional prerequisites within osTicket installation Files </h3>



<h3> 6️⃣ Configure PHP in IIS </h3>



<h3> 7️⃣ Install osTicket </h3>



<h3> 8️⃣ Enable required PHP extensions </h3>



<h3> 9️⃣ Configure osTicket </h3>



<h3> 🔟 Setup the database </h3>



<h3> 1️⃣1️⃣ Finalize and cleanup </h3>


