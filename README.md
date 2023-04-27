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
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
: <br />
<img src="https://i.imgur.com/5bVPho9.png" height="80%" width="80%" alt="Azure Cloud Detection Lab Steps"/>
<br />
<br />
