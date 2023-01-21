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
  <img width="1777" alt="browse80webpage" src="https://user-images.githubusercontent.com/17282458/213874299-fbcaf0f8-44a2-4453-91e4-0fa1a742e5b2.png">

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
<p><img width="1334" alt="renameosconfig" src="https://user-images.githubusercontent.com/17282458/213874767-3e12202c-20b4-43b3-b385-7dc85cca0eca.png">

  
</p>
<br />



<p>
8. Right click ost-config.php <br>
- Properties > Security > Advanced<br>
- Disable inheritance and Remove All <br>
- New Permissions then Everyone and allow Full Control
- Hit OK!
</p>
<p><img width="1124" alt="ostconfig-properties" src="https://user-images.githubusercontent.com/17282458/213874804-7a949dbc-bbec-4a38-bc64-5da71fd68700.png">
<img width="730" alt="addeveryonepermission" src="https://user-images.githubusercontent.com/17282458/213874821-a0894c3b-ef26-482d-a5b4-26cf3da70c94.png">
<img width="497" alt="enableallpermissions" src="https://user-images.githubusercontent.com/17282458/213874838-50cd9a13-65f4-49a6-9dd9-55feb73486bd.png">
</p>
<br />



<p>
9. In the browser, 'continue' setting up osTickets <br>
  - Fill out information up until the mySQL section.
</p>
<p>
<img width="1060" alt="osticket-form" src="https://user-images.githubusercontent.com/17282458/213874939-ab9bbda8-8475-4097-9a4d-9e2ffabd6e65.png">

</p>
<br />



<p>
10. Download and install HeidiSQL. <br>
- HeidiSQL interfaces between osTicket and MySQL. <br>
- Create a new session with database root and set a generic password: Password1. <br>
- Connect to the session. <br>
- Create a database named “osTicket”.
</p>
<p><img width="967" alt="heidi-installation" src="https://user-images.githubusercontent.com/17282458/213875363-203a8cff-4b4e-47b2-bcf5-cfcb268fd510.png">
<img width="737" alt="heidi-new-session" src="https://user-images.githubusercontent.com/17282458/213875426-344175ff-eec2-41e1-9e0e-ee4a4833b83f.png">
  <img width="985" alt="Screenshot 2023-01-18 at 2 36 30 PM" src="https://user-images.githubusercontent.com/17282458/213875456-e6177ca8-8303-4cfc-bb0a-9369cc8716b1.png">
<img width="1003" alt="heidisqldone" src="https://user-images.githubusercontent.com/17282458/213875441-1d19572d-c9c0-4de8-99ce-bf4ecfe70a8b.png">
</a><br />
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
  <img width="1044" alt="installnow" src="https://user-images.githubusercontent.com/17282458/213875470-a6f0fc35-e5c1-4932-b3d2-cc9623e02666.png">

</p>
<br />



<p>
12. Check for no errors after installing! <br>
  Congratulations, you are almost done!
</p>
<p><img width="1698" alt="Screenshot 2023-01-18 at 2 38 09 PM" src="https://user-images.githubusercontent.com/17282458/213875481-4d2c62c4-d475-4784-b2c0-0704f31042d0.png">
</p>

<p>
  The next steps are cleanup for optimization and security reasons. <br>
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
