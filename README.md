<h1>Azure Sentinal SEIM Honeypot</h1>

 

<h2>Description</h2>
This project combines Azure Sentinel, a cloud-native SIEM, with a live honeypot Virtual Machine to monitor RDP brute force attacks globally. A custom PowerShell script fetches attacker geolocation data using an API call and plotted on Azure Sentinel Map for visualization
<br />


<h2>Utilities Used</h2>

- <b>Azure Virtual Machine</b> 
- <b>Azure Sentinal</b>
- <b>Powershell</b>
- <b>ipgeolocation</b>


<h2>Environments Used </h2>

- <b>Windows 10</b> 

<h2>Azure Sentinal Honeypot walk through</h2>

<p align="center">
Set up a Azure acount and create a virtual machine to be the honepot: <br/>
<img src="https://imgur.com/EXd85G4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure the firewall to allow all in:  <br/>
<img src="https://imgur.com/hyxYeuN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a Log Analytics workspace : <br/>
<img src="https://imgur.com/EV0la3X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect Log Analytics to the virtual machine:  <br/>
<img src="https://imgur.com/PK3h74l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enable the ability to gather logs from the virtual machine to the work analytics workspace by turning defender on:  <br/>
<img src="https://imgur.com/gtlEgCi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure data collection to collect all events:  <br/>
<img src="https://imgur.com/gU2amQb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add Sentinal to workspace:  <br/>
<img src="https://imgur.com/r2OcECO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download remote desktop and log into the virtual machine with remote desktop :  <br/>
<img src="https://imgur.com/KwyJGov.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://imgur.com/FuohKH3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Turn off Windows Firewall on the virtual machine:  <br/>
<img src="https://imgur.com/JaIS1qJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Get ipgeolocation.io API key:  <br/>
<img src="https://imgur.com/26Wv8MW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run script to gather geo data from attackers:  <br/>
<img src="https://imgur.com/H9BAUQ4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a custom table in log analytics workspace to bring in our custom log:  <br/>
<img src="https://imgur.com/RLn2pdZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create custom fields and extract fields from custom log data:  <br/>
<img src="https://imgur.com/Purq0aA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Test extracts:  <br/>
<img src="https://imgur.com/eeuBW29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a new workbook and set up a map in sentinal with latitude and longitude. Set map size with the evet count and heat map setting:  <br/>
<img src="https://imgur.com/ks4Ercy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Monitor map of attacks:  <br/>
<img src="https://imgur.com/O8A2E4J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sentinal SEIM overview of events:  <br/>
<img src="https://imgur.com/t4VXkRs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
