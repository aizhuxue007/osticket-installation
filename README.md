<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This quick tutorial guides the installation of the open-source help desk ticketing system osTicket.<br />

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
1. Download and Install osTickets 1.15.8<br>
- Make sure the version is exactly the same, so that all the dependencies are compatible. <br>
</p>
<p>
<a href="https://ibb.co/Km3bTJ1"><img src="https://i.ibb.co/TrFY9sC/downloadosticket.png" alt="downloadosticket" border="0"></a>
</p>
<br />


<p>
2. Extract and move the 'upload' folder to c:\inetpub\wwwroot
</p>
<p>
<a href="https://ibb.co/GkxrYTD"><img src="https://i.ibb.co/vmwMyYW/extractandmoveupload.png" alt="extractandmoveupload" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
  <a href="https://ibb.co/WfWCQpx"><img src="https://i.ibb.co/GRvmX3x/uploadfolder.png" alt="uploadfolder" border="0"></a>
</p>
<br />


<p>
3.  Within the wwwroot directory, rename the 'upload' folder to 'osTicket' <br>
  - This folder hold web files that displays osTicket page in your browser.
</p>
<p>
\<a href="https://ibb.co/SBssj5K"><img src="https://i.ibb.co/1Tvvg79/renametoosticke.png" alt="renametoosticke" border="0"></a>
</p>
<br />


<p>
4. Restart IIS. <br>
</p>
<p>
<a href="https://ibb.co/p3VM0n7"><img src="https://i.ibb.co/8jvfKXC/restart-IISpreinstall.png" alt="restart-IISpreinstall" border="0"></a>
</p>
<br />


<p>
5. Within IIS browse the osTicket webpage <br> 
 Go to: <br>
 - Sites <br> 
 - Default <br>
 - osTicket <br>
 - Browse *:80 on right panel <br>
 And Voila! You should see osTicket on your browser!
</p>
<p>
<img src="https://i.ibb.co/g4jztSS/Screenshot-2023-01-18-at-2-25-57-PM.png" alt="Screenshot-2023-01-18-at-2-25-57-PM">
<a href="https://ibb.co/jbvhxrZ"><img src="https://i.ibb.co/jbvhxrZ/click-browse-80.png" width="300" alt="click-browse-80" border="0" /></a>
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
<a href="https://ibb.co/0X73n5h"><img src="https://i.ibb.co/8BCVmk6/enablephpextension1.png" alt="enablephpextension1" border="0"></a>
<img src="https://i.ibb.co/pxpypJF/enablephpextension2.png" width="500" alt="enablephpextension2" border="0">
</p>
<br />




<p>
  7. Rename <strong>ost-sampleconfig.php</strong> to <strong>ost-config.php</strong>. <br>
  - File is located in C:\inetpub\wwwroot\osTicket\include\<strong>ost-sampleconfig.php</strong> 
</p>
<p>
<a href="https://ibb.co/JsP4JQ3"><img src="https://i.ibb.co/tJ5trXL/renametoostconfig1.png" alt="renametoostconfig1" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
</p>
<br />



<p>
8. Right click ost-config.php <br>
- Properties <br>
- <strong>Disable inheritance</strong> and <strong>Remove All</strong> <br>
- <strong>New Permissions</strong> then <strong>Everyone</strong> and allow <strong>All permissions</strong>
</p>
<p>
<a href="https://ibb.co/2t5qYMM"><img src="https://i.ibb.co/d27BJpp/ost-config-renamed-1.png" alt="ost-config-renamed-1" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
<a href="https://ibb.co/nc6jQCf"><img src="https://i.ibb.co/9TcWyt2/ost-config-permi.png" alt="ost-config-permi" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
<a href="https://ibb.co/7ncbjW4"><img src="https://i.ibb.co/2v25WtN/addeveryonepermission.png" alt="addeveryonepermission" border="0"></a>
<a href="https://ibb.co/mX8mLfb"><img src="https://i.ibb.co/9VtJFQc/enableallpermissions.png" alt="enableallpermissions" border="0"></a>
</p>
<br />



<p>
9. In the browser, 'continue' setting up osTickets <br>
  - Fill out information up until the mySQL section.
</p>
<p>
<a href="https://ibb.co/Gp0FG3P"><img src="https://i.ibb.co/7CXbBNy/Screenshot-2023-01-18-at-2-32-04-PM.png" alt="osTicketSetupform" border="0"></a>
</p>
<br />



<p>
10. Download and install HeidiSQL. <br>
- HeidiSQL interfaces between osTicket and MySQL. <br>
- Create a new session, root/Password1 <br>
- Connect to the session <br>
- Create a database called “osTicket”
</p>
<p>
<a href="https://ibb.co/f2FB12d"><img src="https://i.ibb.co/9Ngz8NH/Screenshot-2023-01-18-at-2-32-44-PM.png" alt="HeidiSQLInstallation" border="0"></a>
<a href="https://ibb.co/0hKmYNr"><img src="https://i.ibb.co/nzB6Q2j/newsessioninroot.png" alt="newsessioninroot" border="0"></a>
<a href="https://ibb.co/1QLY1nT"><img src="https://i.ibb.co/F3Kk2Wz/Screenshot-2023-01-18-at-2-36-30-PM.png" alt="heidisqlnameosticket" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
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
<a href="https://ibb.co/FV3v8m9"><img src="https://i.ibb.co/vYq5LVb/Screenshot-2023-01-18-at-2-37-26-PM.png" alt="fillmysqlsection" border="0"></a>
<a href="https://ibb.co/tp8m7h6"><img src="https://i.ibb.co/KxF0MGg/installnow.png" alt="installnow" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
</p>
<br />



<p>
12. Check for no errors after installing! <br>
  Congratulations, you are almost done!
</p>
<p>

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
