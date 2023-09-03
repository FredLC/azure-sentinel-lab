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
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
