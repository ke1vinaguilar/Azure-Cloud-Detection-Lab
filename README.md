<h1>Azure Cloud Detection Lab</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
In this lab we're going to walk through how to create am Active Directory home lab Environment using Oracle Virtual Box. Configuring and running this lab will definitely help develop your understanding of how active directory and windows networking works, so I'd highly recommnend running through it a couple times, ask questions where stuff is unclear, and eventually try to build it on your own without watching. Please let me know if you have any questions!
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10 </b> (21H2)
- <b>Servers 2019</b>

<h2>Diagram</h2>
<p align="center">
<img src="https://i.imgur.com/Jtqs9WI.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
 </p>

<h2>Program walk-through:</h2>

<p align="center">
Create your Azure account: <br />
<a href="https://azure.microsoft.com/en-us/free/">Azure</a>
<br />
<br />
Go to https://portal.azure.com/: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the search bar type in “resource groups” and under “Services” click on “Resource Groups”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click “Create”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
For “Resource group *” type in “labgroup” and for “Region *” select “(US) East US”: <br />
-Click on “Review + create” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Create”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
To create our VM type in “Virtual Machine” in the search bar and under services click on “Virtual Machine”: <br />
-Click on “+ Create” and select “Azure virtual machine” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
For “Resource group *” select “labgroup”: <br />
- For “Virtual machine name *” type in “labvm” <br />
- For “Region *” select “(US) East US” <br />
- For “Image *” select “Windows 10 Pro, version 21H2 – x64 Gen2” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Administrative account” for “Username *” and “Password *” use the following credential: <br />
- Username: labvm1 <br />
- Password: xxxxxxx <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under licensing click the box that says “I confirm I have an eligible Windows 10 license with multi-tenant hosting rights. *”: <br />
-Click on “Review + create” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Create”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Once deployment is complete, click on “Go to resource”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Settings” click on “Networking” the network security group should populate: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<br />
<br />
Implement “Just-In-Time” access to avoid brute force or password spray attack and only give access when needed and for authorized users: <br />
-In the search bar type in “Microsoft Defender for Cloud” and under “Services select “Microsoft Defender for Cloud” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Azure subscriptions”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Azure subscription 1”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Enable all”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Go back to the “Microsoft Defender for Cloud |Overview” and under “Cloud Security” click on “Workload protections”: <br />
*Overall security posture in Azure, whats covered/ whats not covered) <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Go back to the Virtual Machine: <br />
- Click on “labvm” <br />
- Under “Settings” click on “Connect" <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “To improve security, enable just-in-time access on this VM.”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on the “Enable just-in-time” button: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Networking” under “Settings”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
*New rules have been implied* <br />
<br />
<br />
Click on the “Connect” tab under “Settings”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Source IP” click on “My IP”: <br />
*The IP from the PC will be recorded and that’ll be the only IP address that will be allowed to connect upon requesting access* <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Request access”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
If you go back to “Networking” under “Settings” you’ll see that a new has been created which implements that only traffic from the PC’s IP address is allowed: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the search bar type in “log analytics workspace” and under “Services” click on “Log Analytics workspaces”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Create”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
For “Resource group *” select “labgroup”: <br />
- For “Name *” type in “labgroupvm” <br />
- For “Region *” select “East US” <br />
- Click on “Review + Create” <br />
-Click on “Create” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the search bar type in “sentinel” and under “Services” click on “Microsoft Sentinel”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Create”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “labgroupvm”: <br />
-Click “Add” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Configurations” click on “Data connectors”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the search bar type in “Windows”: <br />
- Click on “Windows Security Event via AMA” <br />
- Click on “Open connector page” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<br />
<br />
Click on “Create data collection rule”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
For “Rule Name *” type in “cloudvmdemo”: <br />
-For “Resource Group *” select “labgroup” <br />
-Click on “Next: Resources” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Add resource(s)”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click the box next to “labgroup” and click on “Apply”: <br />
- Click on “Next: Collect” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “All Security Events”: <br />
-Click on “Review + create” <br />
-Click on “Create” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the search bar type in “virtual machine” and under “Services” click on “Virtual machines”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “labvm”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Settings” click on “Connect”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Source IP” select “My IP” and click on “Request access”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Go back to the “Overview Tab”: <br />
- Copy the “Public IP address” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Open up “Remote Desktop Connection”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Paste the “Public IP address” and click “Connect”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Type the following credential in: <br />
Username: labvm1 <br />
Password: John619cenaa <br />
<br />
<br />
Click on the “Don’t ask me again for connections to this computer” box: <br />
-Click on “Yes” <br />
<br />
<br />
Select “No” to all privacy settings: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the Windows search bar type in “Event Viewer” and select it: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Windows Logs” and click on “Security” and all the security events will populate: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Go back to “Microsoft Sentinel”: <br />
- Click on “labgroupvm” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Logs” under “General”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Type in the query and click “Run”: <br />
SecurityEvent <br />
| where EventID == 4624 <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Specify fields that we want to populate
- Type in the query and click “Run”: <br />
SecurityEvent <br />
| where EventID == 4624 <br />
|project TimeGenerated, Computer, Account <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Configuration” click on “Analytics”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Rule templates” and in the search bar type in “windows”: <br />
- Scroll down and click on “Excessive Windows logon failures” <br />
-Click on “Create rule” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Next: Set rule logic”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Reference: https://attack.mitre.org/techniques/T1053/ <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
In the search bar of your VM type in “event viewer” and click on Event Viewer: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Windows Logs” and then click on “Security”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Change the security policy which is just configuration settings for the security (determine what is
logged and what isn’t) <br />
- In the search bar type in “local security policy and click on “Virtual Security Policy” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Advanced Audit Policy Configuration” and then click on “System Audit Policies – Local
Group”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Make sure the “Object Access” is on “Configured”’: <br />
-Click on “Object Access” then “Audit Other Object Access Events” <br />
- Click the “Configure the following audit events” box and select “Success” and “Failure” <br />
- Click “Apply” and then click “OK” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<br />
<br />
In the search bar type in “task scheduler” and click on “Task Scheduler”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Actions” click on “Create Task…”: <br />
- For “Name” type in “malicioustask” <br />
- Click on “Run only when user is logged on” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on the “Triggers” tab: <br />
-Click on “New” <br />
-For “Begin the task” select “On a schedule” <br />
-For “Start” select 03/18/2023 10:55:12 (1 minutes after actual current time) <br />
-Click on “OK” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on the “Actions” tab and click on “New”: <br />
-For “Action” select “Star a program” <br />
-For “Program/script” click on “Browse” and select “C:\Program Files\Internet Explorer\expore.exe” <br />
*When it’s time for the test to run internet explorer is going to open on the system* <br />
-Click on “OK” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Go to “Event Viewer” to see if the task has been logged: <br />
-Click on “Windows Logs” and then click on “Security” <br />
-Look for Event ID 4702 <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Go back to “Microsoft Sentinel” <br />
-Run the following query: <br />
SecurityEvent <br />
| where EventID == 4698 <br />
| parse EventData with * '<Data Name="SubjectUserName">' User '</Data>' * <br />
| parse EventData with * '<Data Name="TaskName">' NameofScheduledTask '</Data>' * <br />
| parse EventData with * '<Data Name="ClientProcessId">' ClientProcessID '</Data>' * <br />
| project Computer, TimeGenerated, ClientProcessID, NameofScheduledTask, User <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Configurations” click on “Analytics”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Create”: <br />
-Click on “Scheduled query rule” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
For “Name *” type in “Scheduled Task Creation” <br />
For “Description” type the following: “This alert fires when a scheduled task is created on a VM.” <br />
- For “Tactics and techniques” select “Persistence” and “11053 – Schedule Tasl/Job” <br />
- Click on “Next : Set rule logic” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
For “Rule query” paste the following query: <br />
SecurityEvent <br />
| where EventID == 4698 <br />
| parse EventData with * '<Data Name="SubjectUserName">' User '</Data>' * <br />
| parse EventData with * '<Data Name="TaskName">' NameofScheduledTask '</Data>' * <br />
| parse EventData with * '<Data Name="ClientProcessId">' ClientProcessID '</Data>' * <br />
| project Computer, TimeGenerated, ClientProcessID, NameofScheduledTask, User <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Alert enrichment” click on “Entity mapping”: <br />
- Click on “Add new entity” <br />
-For “entity type” select “Account” and for “Identifier” select “Name” and for “Value” select “User” <br />
-For “entity type” select “Process” and for “Identifier” select “ProcessId” and for “Value" select “ClientProcessID” <br />
-For “entity type” select “Malware” and for “Identifier” select “Name” and for “Value select
“NameofScheduledTask” <br />
-For “entity type” select “Host” and for “Identifier” select “HostName” and for “Value select “Computer” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “query scheduling”: <br />
-For “Runs query every *” select “5 Minutes” <br />
-For “Lookup data from the last *” select “5 minutes” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Alert threshold”: <br />
-For “Generate alert when number of query results” select “Is greater than 0” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Event grouping” select “Trigger an alert for each event”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
- Click on “Next : Incident settings (Preview) <br />
-Click on “Next : Automated response” <br />
-Click on “Next: Review” <br />
-Click on “Create" <br />
<br />
<br />
In the VM open “Task Scheduler” and under “Action” click on “Create Task…”: <br />
<br />
<br />
For “Name” type in “task2”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on the “Triggers” tab and click on “New…”: <br />
-For “Begin the task” select “On a schedule” <br />
-Select “One time” <br />
-For “Start” select 03/18/2023 4:13:27 (1 minutes after actual current time) <br />
-Click on “OK” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on the “Actions” tab and click on “New” <br />
-For “Action” select “Star a program” <br />
-For “Program/script” click on “Browse” and select “C:\Program\Files\Internet\Explorer\expore.exe” <br />
*When it’s time for the test to run internet explorer is going to open on the system* <br />
-Click on “OK” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Under “Threat Management” click on “Incidents”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Scheduled Task Creation”: <br />
-Click on “Unassigned” and assign the task to myself <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Change the “Status” to “Active”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “View full details”: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
Click on “Status” and change it to “Closed”: <br />
- For “Select classification” click on “False Positive – incorrect alert logic” <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/> <br />
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
