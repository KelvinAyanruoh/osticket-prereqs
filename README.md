<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable the IIS web server with CGI (World Wide Web Services -> Application Development Features -> [X] CGI)
- Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) 
- Install the Rewrite Module (rewrite_amd64_en-US.msi)
- Create the directory C:\PHP
- unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
- From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
- From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

  

<h2>Installation Steps</h2>

<p>
<img width="1174" height="1059" alt="image" src="https://github.com/user-attachments/assets/1be6c422-a439-4251-9073-1794ba062469" />

</p>
<p>
After installing the rewrite AMD, create the directory C:\PHP, unzip, and copy the php folder into the C:\PHP” folder

<br />

<p>
<img width="1248" height="438" alt="image" src="https://github.com/user-attachments/assets/48dfe2c5-09f7-4262-849c-25f785b30f83" />

</p>
<p>
Now we install VC_redist.x86.exe. and MySQL 5.5.62 (mysql-5.5.62-win32.msi) and set up MySQL

- Typical Setup ->
- Launch Configuration Wizard (after install) ->
- Standard Configuration ->
  
</p>
<br />

<p>
<img width="1163" height="546" alt="image" src="https://github.com/user-attachments/assets/7bd893e7-9b74-47b2-8c36-2875a922a3bd" />

<img width="1234" height="580" alt="image" src="https://github.com/user-attachments/assets/1ba98594-04b8-46e6-a022-2de3602c9ba1" />


</p>
<p>
Open IIS as an Admin

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

Reload IIS (Open IIS, Stop and Start the server)
<img width="1285" height="985" alt="image" src="https://github.com/user-attachments/assets/5d8464f0-97b1-49c5-9796-74d8cba5ac94" />
<img width="1032" height="509" alt="image" src="https://github.com/user-attachments/assets/c8a59df9-54ac-4fa3-842d-cc426d5a7dc4" />


</p>
<br />

<h2>INSTALL OSTICKET </h2>


</p>
<p>
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
Reload IIS (Open IIS, Stop and Start the server)

<img width="1215" height="1205" alt="image" src="https://github.com/user-attachments/assets/e7f8e01a-0560-468a-a089-fec1c82e37e1" />

</p>
<p>

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
<img width="1300" height="1210" alt="image" src="https://github.com/user-attachments/assets/ee953948-ee4c-46a3-9e46-3ffd5ff1b63f" />
<img width="940" height="617" alt="image" src="https://github.com/user-attachments/assets/26008801-9990-48f1-83a8-6ee787e8fee6" />



- Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

- Assign Permissions: ost-config.php
- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All




