<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This quick tutorial guides the installation of osTicket, the open-source help desk ticketing system.<br />

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
<img width="1777" alt="downloadosticket" src="https://user-images.githubusercontent.com/17282458/213872317-abc37d0e-97de-4260-9f16-0acc07765547.png">

</p>
<br />


<p>
2. Extract and move the 'upload' folder to c:\inetpub\wwwroot
</p>
<p>
<img width="1340" alt="extractandmoveupload" src="https://user-images.githubusercontent.com/17282458/213872341-0ff1aeeb-5f0c-4655-bdec-2ad3f694086c.png">
<img width="1211" alt="uploadfolder" src="https://user-images.githubusercontent.com/17282458/213872361-85271713-a4fe-4c3f-a89e-7578d0be8a33.png">


</p>
<br />


<p>
3.  Within the wwwroot directory, rename the 'upload' folder to 'osTicket' <br>
  - This folder hold web files that displays osTicket page in your browser.
</p>
<p>
<img width="1175" alt="renametoosticke" src="https://user-images.githubusercontent.com/17282458/213872370-129d1116-174c-45fe-8ddf-1b03169f35e0.png">
</p>
<br />


<p>
4. Restart IIS. <br>
</p>
<p>
<img width="1791" alt="restart-iis-installation" src="https://user-images.githubusercontent.com/17282458/213874127-e69e6451-ea08-4b69-95af-fbdfd6ac4501.png">
</p>
<br />


<p>
5. Within IIS browse the osTicket webpage <br> 
 Go to: <br>
 - Sites > Default > osTicket > Browse *:80 on right panel <br>
 And Voila! You should see osTicket on your browser!
</p>
<p>
<img src="https://i.ibb.co/g4jztSS/Screenshot-2023-01-18-at-2-25-57-PM.png" alt="Screenshot-2023-01-18-at-2-25-57-PM">

  <img width="324" alt="click-browse-80" src="https://user-images.githubusercontent.com/17282458/213873205-22c81b5c-9021-4e96-a691-0f9e53ceeb10.png">
  
</p

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
  <img width="810" alt="enablephpextension1" src="https://user-images.githubusercontent.com/17282458/213873683-614ae724-3386-4700-b7a3-19dc7c798824.png">
<img width="483" alt="enablephpextension2" src="https://user-images.githubusercontent.com/17282458/213873693-3cec8499-f729-40df-9ea9-d6da5a31e61f.png">
  <img width="1761" alt="phpextinstalled" src="https://user-images.githubusercontent.com/17282458/213874013-06381315-0e12-48f1-842c-dcbc5ea055b0.png">

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
- <strong>New Permissions</strong> then <strong>Everyone</strong> and allow <strong>Full Control</strong>
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
- Create a new session with database root and set a generic password: Password1. <br>
- Connect to the session. <br>
- Create a database named “osTicket”.
</p>
<p>
<a href="https://ibb.co/f2FB12d"><img src="https://i.ibb.co/9Ngz8NH/Screenshot-2023-01-18-at-2-32-44-PM.png" alt="HeidiSQLInstallation" border="0"></a>
<a href="https://ibb.co/0hKmYNr"><img src="https://i.ibb.co/nzB6Q2j/newsessioninroot.png" alt="newsessioninroot" border="0"></a>
<a href="https://ibb.co/1QLY1nT"><img src="https://i.ibb.co/F3Kk2Wz/Screenshot-2023-01-18-at-2-36-30-PM.png" alt="heidisqlnameosticket" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'></a><br />
</p>
<br />



<p>
11. Filling up the MySQL section and installing osTicket <br>
- MySQL Database: osTicket <br>
- MySQL Username: root <br>
- MySQL Password: Password1 <br>
- Click “Install Now!”
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
13. Set ost-config.php with "Read" only permissions. <br>
- Filepath: C:\inetpub\wwwroot\osTicket\include\ost-config.php <br>
  - Right click on file, go to <strong>Properties</strong>, then <strong>Security</strong>, check only the Read box
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
14. Browse as End Users and Help Desk Agent in osTicket:
- Enduser: http://localhost/osTicket/ 
- Help Desk Agent: http://localhost/osTicket/scp/login.php 
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<a href="https://github.com/aizhuxue007/osticket-postinstall">Go to Post Installations</a>
