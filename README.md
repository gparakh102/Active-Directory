<h1>Basic Home Lab Running Active Directory</h1>

<h2>Description</h2>
This repository contains steps on how i set up a basic home lab running Active Directory using Oracle Virtual Box by following a tutorial by Josh Madakor
Configuring and running this lab helped develop my understanding of how active directory and windows networking works in corporate environments, so l'd highly recommend running through it a couple times.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Virtal Box</b>
- <b>Windows 10</b>
- <b>Windows Server 2019</b>

<h2>Practical lab walk-through:</h2>

<p>
Architecture Diagram : <br/>
<img src="https://i.postimg.cc/hj3VsxHm/1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 1: Download and install Oracle VirtualBox from the official website.<br/>
<a href="https://www.virtualbox.org/">Oracle Virtual Box</a><br/><br/>
Step 2: Download the Windows 10 and Server 2019 ISO files.<br/>
<a href="https://www.microsoft.com/en-us/software-download/windows10ISO"> Windows 10 iso </a>

<a href="https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019"> Windows Server 2019 </a><br/><br/>
Step 3: Create a new virtual machine by clicking on "New" in VirtualBox, naming it "Domain Controller," and selecting the "Windows Server 2019" ISO file as the boot media.
<img src="https://i.postimg.cc/PqSDfYf7/2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/0ydm3hTP/3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Configure the virtual machine by giving it two network adapters: one for connecting to the internet and the other for the internal network.
 <br/>
<img src="https://i.postimg.cc/3w8pHnhp/4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/HsMb0r3J/5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 5: Install Server 2019 on the virtual machine.<br/><br/>

<b>In the Client System (Win 10 VM):</b><br/>
 
Click on the “ network and internet ” settings go to “network connections”
<br/>
<img src="https://i.postimg.cc/3Nsm5hrJ/6.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
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
