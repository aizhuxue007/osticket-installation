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
1. Install osTickets 1.15.8<br>
- Make sure the version is exactly the same, so that all the dependencies are compatible. <br>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
2. Extract and move the 'upload' folder to c:\inetpub\wwwroot
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
3.  Within the wwwroot directory, rename the 'upload' folder to 'osTicket' <br>
  - This folder hold web files that displays osTicket page in your browser.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
4. Restart IIS. <br>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
5. Within IIS browse the osTicket webpage <br> 
 Click on: 
 -> Sites <br> 
 -> Default <br>
 -> osTicket <br>
 -> Browse *:80 on right panel <br>
 Voila! You should see osTicket on your browser!
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
6. Enable PHP extensions <br>
<!-- Go back to IIS, sites -> Default -> osTicket <br> -->
Back in IIS, double-click on PHP Manager then go to “Enable or disable an extension” <br>
Enable: <br>
&emsp;php_imap.dll <br>
&emsp;php_intl.dll <br>
&emsp;php_opcache.dll <br>
Refresh the webpage, PHP extensions are now completed!
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />




<p>
  7. Rename <strong>ost-sampleconfig.php</strong> to <strong>ost-config.php</strong>. <br>
  - File is located in C:\inetpub\wwwroot\osTicket\include\<strong>ost-sampleconfig.php</strong> 
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
8. Right click ost-config.php <br>
- Properties <br>
- Disable inheritance -> Remove All <br>
- New Permissions -> Everyone -> All permissions
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
9. In the browser, 'continue' setting up osTickets <br>
- Note that the Default email is for receiving email from endusers.

</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
10. Download and install HeidiSQL. <br>
- HeidiSQL is an interface between osTicket and MySQL <br>
- Create a new session, root/Password1 <br>
- Connect to the session <br>
- Create a database called “osTicket”
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
11. Setting up MySQL in osticket and installing <br>
MySQL Database: osTicket <br>
MySQL Username: root <br>
MySQL Password: Password1 <br>
Click “Install Now!”
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
12. Check for no errors after installing! <br>
  Congratulations, you are almost done!!
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Set "Read" only permissions for ost-config.php file. <br>
- Filepath: C:\inetpub\wwwroot\osTicket\include\ost-config.php <br>
- Right click on file
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Delete folder: C:\inetpub\wwwroot\osTicket\setup <br>

</p>
<br />
<p>
15. Browse as End Users in osTicket:
http://localhost/osTicket/ 
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

</p>
<br />
<p>
16. Helpdesk login page: http://localhost/osTicket/scp/login.php 
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<a href="https://github.com/aizhuxue007/osticket-postinstall">Go to Post Installations</a>
