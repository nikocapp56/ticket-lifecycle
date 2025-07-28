<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/> </p>

<h1>osTicket - Ticket Lifecycle</h1>
This guide outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket. This setup provides a clear view of how a real-life help desk operates and how different roles interact with tickets based on their respective responsibilities.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Prerequisites</h2>

- [osTicket - Prerequisites and Installation](https://github.com/nikocapp56/osticket-prereqs)
- [osTicket - Post-Installation Configuration](https://github.com/nikocapp56/post-install-config)

<h2>Ticket Lifecycle Steps</h2>

<h3> 0️⃣ Overview of Ticket Workflow and Role Interaction </h3>

- Create tickets as an end-user.
- Respond to tickets as a Help Desk Agent.
- Set priorities, assign SLAs, and observe ticket visibility limitations.
- Work tickets to resolution and review system behavior.


<h3> Ticket Scenario 1️⃣: Mobile/Online Banking System Down </h3>

Go to the End User Ticket Submission URL: http://localhost/osTicket

<img width="800" alt="1" src="https://github.com/user-attachments/assets/9467238b-a019-4b61-b1c0-3e18b6319aaf" />

Create a ticket as end-user, Karen.

<img width="1004" height="1242" alt="2" src="https://github.com/user-attachments/assets/db3649f5-9b0c-4be3-8b21-f4b47fb83006" />
</p>
Go to the Admin Login URL: http://localhost/osTicket/scp/login.php
</p>
Log in as Agent John.
</p>

<img width="800" alt="3" src="https://github.com/user-attachments/assets/dab71f0d-40b7-4101-bd40-78a475aad774" />
<img width="800" alt="4" src="https://github.com/user-attachments/assets/25faebb5-0dae-43eb-a67f-70a2724d5353" />

Open the ticket.

<img width="800" alt="5" src="https://github.com/user-attachments/assets/823eb4e8-f001-4323-9125-e9d542e0392c" />

Figure out how severe the issue is, then route it to the right team. Since the ticket is banking related, assign it to the Online Banking Team. 

<img width="800" alt="8" src="https://github.com/user-attachments/assets/deb5d8b7-6bbe-4869-ac1b-27e29a0f4cf6" />

Update the SLA Plan to Sev-A since this has a big impact on the business. 

<img width="800" alt="6" src="https://github.com/user-attachments/assets/ddef4ce3-f128-4129-a403-6db91cf43b28" />

Change the Help Topic to Business Critical Outage.

<img width="800"  alt="7" src="https://github.com/user-attachments/assets/6cd40287-e2a0-41dc-b988-c2f35fdde951" />

Log in as Jane since she is part of the Online Banking Team.

<img width="800" alt="8 5" src="https://github.com/user-attachments/assets/79b15abf-897c-443b-b418-2931b14ab4f7" />

Reply to the end-user with any updates.

<img width="800" alt="9" src="https://github.com/user-attachments/assets/5fb38508-bb0a-40f3-b042-d58866edb995" />

Once the issue is resolved or the root cause is identified, respond to the end-user with another update.

<img width="800" alt="10" src="https://github.com/user-attachments/assets/569f5ee6-386f-439c-b452-7e09f4345b98" />

Set the Status to Resolved.

<img width="574" alt="11" src="https://github.com/user-attachments/assets/3d899adc-e9dc-425e-ac3f-ac58dc31abab" />


<h3> Ticket Scenario 2️⃣: Accounting department needs Adobe upgrade (broken) </h3>

Go to the End User Ticket Submission URL: http://localhost/osTicket

<img width="800" alt="1" src="https://github.com/user-attachments/assets/9467238b-a019-4b61-b1c0-3e18b6319aaf" />

Create a ticket as end-user, Ken.

<img width="800" alt="12" src="https://github.com/user-attachments/assets/09cc81de-48c9-4f1e-85cb-19d3946fe786" />
</p>
Go to the Admin Login URL: http://localhost/osTicket/scp/login.php
</p>
Log in as Agent John.
</p>

<img width="800" alt="3" src="https://github.com/user-attachments/assets/dab71f0d-40b7-4101-bd40-78a475aad774" />
<img width="800" alt="13" src="https://github.com/user-attachments/assets/9cebaf3e-72d1-4baa-9af3-8ab4aa7e69e2" />

Open the ticket.

<img width="946" alt="14" src="https://github.com/user-attachments/assets/d0e45bd2-f669-4960-943f-9eb8d473ff2c" />

Figure out how severe the issue is, then route it to the right team. In this case, I can assign this ticket to myself, John.

<img width="800" alt="16" src="https://github.com/user-attachments/assets/8930f3f4-3915-4757-b6e7-785382555cf2" />

Update the SLA Plan to Sev-C since this has less impact. 

<img width="800" alt="15" src="https://github.com/user-attachments/assets/c30e4d5f-090f-41cc-827b-f5abfd9996b6" />

Reply to the end-user with any updates.

<img width="800" alt="17" src="https://github.com/user-attachments/assets/6cc8a5c1-47fe-4667-8114-c0499db685ef" />

Once the issue is resolved or the root cause is identified, respond to the end-user with another update.

<img width="800" alt="18" src="https://github.com/user-attachments/assets/e3f44f10-742c-40e1-a957-1ac97ec01f73" />

Set the Status to Resolved.

<img width="800" alt="19" src="https://github.com/user-attachments/assets/c37ecbc3-0a01-426c-ad44-a9a15124029f" />

<h3> Ticket Scenario 3️⃣: Mobile/Online Banking System Down </h3>

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


