<h1>Active Directory Home Lab</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Project consists of a configuring a Domain Controller (Server 19) utilizing two NIC (intranet and internet) and implementing Domain / AD DS, RAS / NAT, and DHCP. 

Use Powershell Script to generate 1k users with desired preconfiuration. 

Utilized VM Virtual Box for both Domain Controller. 

<br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 
- <b>Windows Server 2019 </b>

<h2>Network Overview:</h2>

<p align="center">
Network Overview: <br/>
<img src="https://imgur.com/Tgc1mZD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<h2>Lab walk-through:</h2>

<p align="center">
Configure both DC VM and Client VM : <br/>
<img src="https://i.imgur.com/6VZywTG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Domain Controller: Identify and label internal/external facing NICs.<br/>
<img src="https://imgur.com/K6GAPlm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
The internal NIC will be assigned an APIPA IP Address, while external will have one similar to the host network.<br/> 
<br />
<br />
Configure Internal NIC TCP/IPv4 protocol: <br/>
<img src="https://imgur.com/7zvTxK8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up for AD DS :  <br/>
<img src="https://imgur.com/YDmKRaC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After Deployment Configuration:  <br/>
<img src="https://imgur.com/ldHa0Iz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create Organization Unit to place Admin Account:  <br/>
<img src="https://imgur.com/8FHwE9Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create Admin Account within OU (Domain Admin):  <br/>
<img src="https://imgur.com/jmqOuAx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up Remote Access w/ Routing: <br/>
<img src="https://imgur.com/JLPVeYg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure NAT with External Facing NIC: <br/>
<img src="https://imgur.com/hdfhaYv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Start DHCP Service: <br/>
<img src="https://imgur.com/CsVRlBV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure DHCP settings including scope: <br/>
<img src="https://imgur.com/N8ovtyV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Build & Run Python Script to Configure 1,000 account w/ desired default configurations: <br/>
<img src="https://imgur.com/fmIBhci.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br/>
All of these created accounts will be able to login via Client1 or any other client connected to the DC <br/>
<br />
<br />
Setup VM for Client1, ensure NIC is attached to internal network: <br/>
<img src="https://imgur.com/CL3NE44.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure Client1 to be a member of the DC: <br/>
<img src="https://imgur.com/CbzHPWf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br/>
Any of the 1000 users created w/ the PS script will be able to login via Client1, and access services offered by DC <br/>
<br />
<br />
Finally, back on our DC, we can see the leased address from Client1: <br/>
<img src="https://imgur.com/zkFIsQP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
