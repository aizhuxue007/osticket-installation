<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This quick tutorial guides the installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (2 vCPUs)

<h2>List of Downloads</h2>

- [osTicket v1.15.8](https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=share_link)
- [HeidiSQL](https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit?usp=share_link)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Install osTickets 1.15.8<br>
- Make sure the version is exactly the same, so that all the dependencies are compatible. <br>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Extract and copy the 'upload' folder to c:\inetpub\wwwroot
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Rename 'upload' folder to 'osTicket' within c:\inetpub\wwwroot <br>
  - This folder hold web files that displays osTicket in your browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. Refresh IIS <br>
  - Within IIS, press the restart icon 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Within IIS, click: 
 -> Sites <br> 
 -> Default <br>
 -> osTicket <br>
 -> Click “Browse *:80” <br>
 Voila! You should see osTicket on your browser!

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. Enable PHP extensions <br>
Go back to IIS, sites -> Default -> osTicket <br>
Double-click PHP Manager <br>
Click “Enable or disable an extension” <br>
Enable: php_imap.dll <br>
Enable: php_intl.dll <br>
Enable: php_opcache.dll <br>
Refresh the webpage, notice that we are closer to installation!
</p>
<br />



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  7. Rename C:\inetpub\wwwroot\osTicket\include\<strong>ost-sampleconfig.php</strong> to C:\inetpub\wwwroot\osTicket\include\<strong>ost-config.php</strong>
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Left click ost-config.php <br>
-> Properties <br>
-> Disable inheritance -> Remove All <br>
-> New Permissions -> Everyone -> All

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. In the browser, click 'continue' to set up osTicket <br>
- Note that the Default email receives email from endusers.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. Download and install HeidiSQL. <br>
- HeidiSQL is an interface between osTicket and MySQL <br>
- Create a new session, root/Password1 <br>
- Connect to the session <br>
- Create a database called “osTicket”
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. Setting up MySQL in osticket and installing <br>
MySQL Database: osTicket <br>
MySQL Username: root <br>
MySQL Password: Password1 <br>
Click “Install Now!”
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Check for no errors after installing then, browse to your help desk login page: http://localhost/osTicket/scp/login.php

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Browse as End Users in osTicket:
http://localhost/osTicket/ 
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Delete: C:\inetpub\wwwroot\osTicket\setup <br>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />
