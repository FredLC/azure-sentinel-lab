<h1>Microsoft Azure Sentinel Live Cyberattacks Lab</h1>

<h2>Description</h2>
This lab was built as a honeypot to attract cyber criminals all across the world to analzye their geolocation data and attack patterns. I created a Windows 10 virtual machine in Microsoft Azure that was purposefully made vulnerable i.e no firewall and no Windows Defender. I set up Azure Sentinel (a SIEM) to monitor live attacks (essentially RDP brute-force attempts). I used a custom PowerShell script to gather failed login attempts geo data and a custom KQL query in Log Analytics Workspace to analayze the information and plot it on a world map.
<br />

<h2>Technologies and Environments Used: </h2>

- <b>Azure Sentinel</b>
- <b>Azure Log Analytics Workspace</b>
- <b>PowerShell</b>
- <b>Kusto Query Language (KQL)</b>
- <b>Windows 10</b>

<h2>Lab walk-through:</h2>

<p align="center">
Windows 10 VM settings after creation in Azure Virtual Machines Portal: <br/>
<img src="https://i.imgur.com/X04vdZJ.png" height="80%" width="80%" alt="vm settings"/>
<br />
<br />
As this is a honeypot, I created an inbound rule to allow any traffic on all ports:  <br/>
<img src="https://i.imgur.com/7pPTeR1.png" height="80%" width="80%" alt="cloud firewall"/>
<br />
<br />
Completely disabled Windows Defender Firewall: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="disabled windows defender firewall"/>
<br />
<br />
Created a Log Analytics Workspace and connected the Windows VM:  <br/>
<img src="https://i.imgur.com/Ty0wdQ0.png" height="80%" width="80%" alt="log analytics workspace vm connection"/>
<br />
<br />
Integrated Microsoft Defender for Cloud:  <br/>
<img src="https://i.imgur.com/wpV6rQi.png" height="80%" width="80%" alt="microsoft defender for cloud"/>
<br />
<br />
Added Microsoft Sentinel SIEM to workspace:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="added sentinel"/>
<br />
<br />
SIEM settings:  <br/>
<img src="https://i.imgur.com/Lg1KInI.png" height="80%" width="80%" alt="siem settings"/>
<br />
<br />
I ran a PowerShell script that extracts IP geo location from Windows Event Viewer failed RDP logs. After a few hours, brute-force attempts started coming:  <br/>
<img src="https://i.imgur.com/UuF3rzl.png" height="80%" width="80%" alt="failed rdp"/>
<br />
<br />
Basic query to check if security events are correctly logged:  <br/>
<img src="https://i.imgur.com/jAJrxNg.png" height="80%" width="80%" alt="basic query"/>
<br />
<br />
Querying for event id 4625 which is failed logon:  <br/>
<img src="https://i.imgur.com/7qhlpFK.png" height="80%" width="80%" alt="query event id 4625"/>
<br />
<br />
Created custom log for failed RDP login with geo data:  <br/>
<img src="https://i.imgur.com/NCIZBCf.png" height="80%" width="80%" alt="custom log"/>
<br />
<br />
Parsing fields:  <br/>
<img src="https://i.imgur.com/Yco29cP.png" height="80%" width="80%" alt="parsing fields"/>
<br />
<br />
Final KQL query:  <br/>
<img src="https://i.imgur.com/8z9v2XN.png" height="80%" width="80%" alt="final query"/>
<br />
<br />
Plotted the data on world map using previous query:  <br/>
<img src="https://i.imgur.com/MUpaPNO.png" height="80%" width="80%" alt="world map"/>
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
