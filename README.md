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

<b>In the Client System (Win 10 VM):</b><br/><br/><br/>
 
Step 1: Click on the “ network & internet settings"
<br/>
<img src="https://i.postimg.cc/3Nsm5hrJ/6.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 2: Now click on "Change adapter options"<br/>
<img src="https://i.postimg.cc/zG1KxqPx/7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 3: Change the names of the below adapters to _INTERNET and X_INTERNAL_X to differentiate between the Main controller and client<br/>
<img src="https://i.postimg.cc/prhz6rH6/8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Click on the Internal network properties, and go to Internet protocol version 4 to change the IP address and add loopback address as shown below:<br/>
<img src="https://i.postimg.cc/h4697L8W/9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/1tTNwSqc/10.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
Step 5: Rename the PC to DC for convenience. Click on System<br/>
<img src="https://i.postimg.cc/cH6nvCrL/11.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/ZndvLQPk/12.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<b>Installing AD/DS</b><br/><br/><br/>
 
Step 1: Open "Server Manager"
<br/>
<img src="https://i.postimg.cc/K4hkp5Q1/13.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 2: Click "Add roles and features"<br/>
<img src="https://i.postimg.cc/h4fw9RwJ/14.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 3: This is the first screen, and you must click Next to proceed<br/>
<img src="https://i.postimg.cc/VsphgHQK/15.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Click Next until the window where you must install the AD comes up<br/>
<img src="https://i.postimg.cc/TYb44qTf/16.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Add feat > next > next > next > install
<img src="https://i.postimg.cc/13Zjhnz6/17.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>















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

<b>In the Client System (Win 10 VM):</b><br/><br/><br/>
 
Step 1: Click on the “ network & internet settings"
<br/>
<img src="https://i.postimg.cc/3Nsm5hrJ/6.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 2: Now click on "Change adapter options"<br/>
<img src="https://i.postimg.cc/zG1KxqPx/7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 3: Change the names of the below adapters to _INTERNET and X_INTERNAL_X to differentiate between the Main controller and client<br/>
<img src="https://i.postimg.cc/prhz6rH6/8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Click on the Internal network properties, and go to Internet protocol version 4 to change the IP address and add loopback address as shown below:<br/>
<img src="https://i.postimg.cc/h4697L8W/9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/1tTNwSqc/10.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
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
