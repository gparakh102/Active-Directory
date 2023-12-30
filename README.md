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
<img src="https://i.postimg.cc/hj3VsxHm/1.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 1: Download and install Oracle VirtualBox from the official website.<br/>
<a href="https://www.virtualbox.org/">Oracle Virtual Box</a><br/><br/>
Step 2: Download the Windows 10 and Server 2019 ISO files.<br/>
<a href="https://www.microsoft.com/en-us/software-download/windows10ISO"> Windows 10 iso </a>

<a href="https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019"> Windows Server 2019 </a><br/><br/>
Step 3: Create a new virtual machine by clicking on "New" in VirtualBox, naming it "Domain Controller," and selecting the "Windows Server 2019" ISO file as the boot media.<br/>
<img src="https://i.postimg.cc/PqSDfYf7/2.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/0ydm3hTP/3.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Configure the virtual machine by giving it two network adapters: one for connecting to the internet and the other for the internal network.
 <br/>
<img src="https://i.postimg.cc/3w8pHnhp/4.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/HsMb0r3J/5.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
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
<img src="https://i.postimg.cc/zG1KxqPx/7.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 3: Change the names of the below adapters to _INTERNET and X_INTERNAL_X to differentiate between the Main controller and client<br/>
<img src="https://i.postimg.cc/prhz6rH6/8.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Click on the Internal network properties, and go to Internet protocol version 4 to change the IP address and add loopback address as shown below:<br/>
<img src="https://i.postimg.cc/h4697L8W/9.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/1tTNwSqc/10.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
Step 5: Rename the PC to DC for convenience. Click on System<br/>
<img src="https://i.postimg.cc/cH6nvCrL/11.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/ZndvLQPk/12.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />

<b>Installing AD/DS</b><br/><br/><br/>
 
Step 1: Open "Server Manager"
<br/>
<img src="https://i.postimg.cc/K4hkp5Q1/13.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 2: Click "Add roles and features"<br/>
<img src="https://i.postimg.cc/h4fw9RwJ/14.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 3: This is the first screen, and you must click Next to proceed<br/>
<img src="https://i.postimg.cc/VsphgHQK/15.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step 4: Click Next until this window where you must install the AD comes up<br/>
Now, Add features > next > next > next > install
<img src="https://i.postimg.cc/13Zjhnz6/17.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/N0sCF3mj/18.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/YSdnWdzf/19.png" height="70%" width="70%" alt="Disk Sanitization Steps"/> <br/>
Done, close
<br/>
<br/>
Step 5: Click on the exclamation mark at the top and then "Promote this server to a domain controller" <br/>
<img src="https://i.postimg.cc/wjcb6qtr/20.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/sX1n95nF/21.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/pT7s0y7m/22.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/x8ztBnDt/23.png" height="70%" width="70%" alt="Disk Sanitization Steps"/><br/><br/>
Next > Next > Install<br/>
<img src="https://i.postimg.cc/Df9CLJLD/24.png" height="70%" width="80%" alt="Disk Sanitization Steps"/><br/><br/>
At the end of the installation, you will automatically be signed out
<img src="https://i.postimg.cc/2jbc1Fbh/25.png" height="70%" width="70%" alt="Disk Sanitization Steps"/><br/><br />
Now, mydomain/admin is visible when attempting to login
<img src="https://i.postimg.cc/R0pdFNvg/26.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br/>
<br/>

<br/>
<b>Creating own Admin account instead of dedicated admin account</b>
<br/>
<br/>
<br/>
Step 1: Click on "Active Directory Users and Computers" as in picture"
<img src="https://i.postimg.cc/JzqKfpvV/27.png" height="60%" width="60%" alt="Disk Sanitization Steps"/><br /><br />
Step 2: Next you will find yourself on this screen where you can see the AD domain that was created. <br /> Create a new organizational unit as in picture.
<img src="https://i.postimg.cc/g2dNtCMH/28.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/Fs0TZrxK/29.png" height="70%" width="70%" alt="Disk Sanitization Steps"/><br/><br/>
Step 3: We are creating a new user now, which will be an administrator.
<img src="https://i.postimg.cc/43xwszRK/30.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/jd4QRD0x/31.png" height="60%" width="60%" alt="Disk Sanitization Steps"/><br /><br />
Next <br/>
<img src="https://i.postimg.cc/rwh1t7w7/32.png" height="70%" width="70%" alt="Disk Sanitization Steps"/><br/>
Next > Finish <br/><br/>
Step 4: Now, after this user was created, we are going to make it an administrator.
<img src="https://i.postimg.cc/g0nvy4wj/33.png" height="70%" width="70%" alt="Disk Sanitization Steps"/><br /><br />
Ok > Apply > Ok <br />
<img src="https://i.postimg.cc/rsLxkkfR/34.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.postimg.cc/W3ZgC3wP/35.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br/><br/>
After this is done, Sign out of the account and sign in as the user just created.<br />
<img src="https://i.postimg.cc/VvBMsVhG/36.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
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
