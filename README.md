<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




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
- 1. We  download the osTicket-Installation-Files.zip and unzip it onto your desktop. and this webserver will server our osticketing system   
<img width="875" height="550" alt="image" src="https://github.com/user-attachments/assets/68823c6f-699b-463d-a5a3-e507aec4c677" />


- 2. To proceed with the installation, we need to enable the IIS web server to support CGI. (IIS is Microsoft's web server used to host websites and web apps on Windows.)

      -(World Wide Web Services -> Application Development Features -> [X] CGI)
     <img width="1048" height="528" alt="image" src="https://github.com/user-attachments/assets/bbf21219-868f-47d9-97d0-dc341569c68b" />

- How do we know the IIS Web server is running? We would use a loopback IP address.

- Open a web page, put in the Loopback IP address, and it brings up a default web page of IIS. making our machine a web server
  <img width="938" height="518" alt="image" src="https://github.com/user-attachments/assets/fdc1c445-06bb-4830-9411-f3bc54887b39" />

- 3. Install PHP Manager for IIS from the Ostiket folder. PHP allows the web server to run PHP scripts, which are the backbone of many web applications and OS ticket runs on PHP
     <img width="698" height="437" alt="image" src="https://github.com/user-attachments/assets/04e250be-697f-407d-b377-5d532806e81f" />

- 4. Install the Rewrite Module from the same folder

        - This module is for the IIS web server that enables powerful and flexible rules 
        -  and it ensures the admin and helpdesk portal routing works properly

    
<img width="901" height="476" alt="image" src="https://github.com/user-attachments/assets/14f73313-1e9f-4116-b712-eefc51aa5b0f" />


 - 5. Next, we create a Directory for PHP in our C drive,
      
        <img width="910" height="446" alt="image" src="https://github.com/user-attachments/assets/46304e57-2459-4bf2-8db8-e85c5d80138b" />


        -  and then unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
     
        -  This will allow IIS to run PHP code
          <img width="903" height="492" alt="image" src="https://github.com/user-attachments/assets/e070d9d7-a0f8-482d-8795-19023a9dab92" />



  - 6. Now we install VC_redist.x86.exe. from the osticket folder(It is required to make PHP work on Windows, and since osTicket is built with PHP, it is a critical dependency for a successful osTicket installation on IIS.
  

    <img width="808" height="414" alt="image" src="https://github.com/user-attachments/assets/91703a66-42f4-4035-b744-fe9675cc1ff2" />


   - 7. and MySQL 5.5.62 (mysql-5.5.62-win32.msi) and set up MySQL
        MySQL is a database that Osteckit uses to store all our data 
        <img width="857" height="420" alt="image" src="https://github.com/user-attachments/assets/f248c343-2b40-4e36-a6f3-4ea99e2cfea4" />
- Typical Setup ->

<img width="504" height="389" alt="image" src="https://github.com/user-attachments/assets/cfb386c1-b75b-41cf-a260-e7e8a873f8a4" />


- Launch Configuration Wizard (after install) ->

- input username and password credentials
- <img width="340" height="258" alt="image" src="https://github.com/user-attachments/assets/7f34954a-faec-4bf7-a4a0-3f505e9a8fac" />


- Standard Configuration ->



  <img width="572" height="377" alt="image" src="https://github.com/user-attachments/assets/215e086b-b824-456b-a0e5-981b04aa84b1" />




</p>
<br />

- 8. After installing MySQL, we are going to configure PHP


     -Open IIS
     - Double click on PHP
    
       <img width="581" height="284" alt="image" src="https://github.com/user-attachments/assets/1506ca7b-623b-4201-bcd2-5099d4a25fd7" />

     -Then we are going to register PHP from within the IIS manager, making our web server aware of where PHP IS

  <img width="629" height="536" alt="image" src="https://github.com/user-attachments/assets/538f7e5e-0c86-4e4e-bfbe-71bfd0091023" />

- Browse to locate PHP CGI in our C drive

  <img width="754" height="513" alt="image" src="https://github.com/user-attachments/assets/944a87c7-7ad7-4e3c-9060-d2fa98e5e994" />


  

  


- Reload IIS (Open IIS, Stop, and Start the server)

<img width="991" height="330" alt="image" src="https://github.com/user-attachments/assets/6db9a0a8-a24c-448f-a5d0-ca4dcf1884ae" />



- 9. </p>Install ostall ticket
<p>

-From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, rename “upload” to “osTicket”



<img width="551" height="340" alt="image" src="https://github.com/user-attachments/assets/d805abe4-d8aa-4294-890c-f8a5ad477d0a" />




<img width="792" height="427" alt="image" src="https://github.com/user-attachments/assets/882d1f87-33ae-4f22-a6c6-452c44455734" />




- 10.** Stop and Reset IIS**
 



   <img width="567" height="398" alt="image" src="https://github.com/user-attachments/assets/6bbb9eb3-5561-4668-9338-c02d24e855b6" />




- 11. Load the Os ticket site

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
<img width="1329" height="645" alt="image" src="https://github.com/user-attachments/assets/b435fd0f-6e25-4fa5-8ea6-c4d1d6b078f0" />






Note that some extensions are not enabled on the image at the right 
- Go back to IIS, sites -> Default -> osTicket

- Double-click PHP Manager
  <img width="581" height="284" alt="image" src="https://github.com/user-attachments/assets/3224b042-9925-4f5f-8898-bedd5b3281aa" />



  
  
- Click “Enable or disable an extension.”

 <img width="762" height="563" alt="image" src="https://github.com/user-attachments/assets/578037e7-77bf-4ca0-9918-b6dc23c39565" />

- Enable: php_imap.dll

  <img width="404" height="292" alt="image" src="https://github.com/user-attachments/assets/b5718075-6346-4d66-aafd-0b57b7c9094a" />

- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browser, and observe the changes

<img width="940" height="617" alt="image" src="https://github.com/user-attachments/assets/45f0e7f5-7117-45bb-8e4b-b98b0b6b4ec8" />






- ## Next, we are going to rename: ost sampleconfig. php to ost-config.php in our C drive




- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

  <img width="594" height="618" alt="image" src="https://github.com/user-attachments/assets/59996350-dc55-4c22-9a33-51d18c1f9684" />

- Assign Permissions: ost-config.php
- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All


<img width="663" height="355" alt="image" src="https://github.com/user-attachments/assets/d01c01b0-d789-42b8-b855-1f65d016a43e" />



<h2>Continue Setting up osTicket in the browser
 </h2>

- ## (click Continue)

  <img width="889" height="584" alt="image" src="https://github.com/user-attachments/assets/b52da41a-ccb1-47b3-86e5-13670ce78a16" />


  
- ##  Name Helpdesk
-Default email (receives email from customers)

<img width="904" height="902" alt="image" src="https://github.com/user-attachments/assets/cb289a5d-7cdd-4656-86a1-3018ab63d5ec" />




- ## Before we continue with our installation of Osticket and database settings, we need to create a database specific to os Osticket and use that credential to log in.  We initially created our database application, but we are not yet logged in.
- For that, we need to go back to our  OSTicket folder
- From the “osTicket-Installation-Files” folder, install HeidiSQL.

- Note: Heidi is the database management system used to visually manage our data in the database

  <img width="441" height="384" alt="image" src="https://github.com/user-attachments/assets/99c39e4b-a313-46df-9d7d-d4b810f8fb27" />


- ## Open Heidi SQL


<img width="834" height="525" alt="image" src="https://github.com/user-attachments/assets/bcc845a9-d0f7-4a18-aaa0-c022f2691105" />


- ## Create a new session, with user name and password root/root

<img width="655" height="513" alt="image" src="https://github.com/user-attachments/assets/30bbc6a0-62cc-4fac-82fa-566a9ff954d3" />


- ## Connect to the session

<img width="973" height="585" alt="image" src="https://github.com/user-attachments/assets/79e84917-da01-43cd-9152-a43b23efcb63" />


- ## As Connection is good, then we create a database called “osTicket”

<img width="648" height="548" alt="image" src="https://github.com/user-attachments/assets/1714d711-1a0a-4c13-b508-ebc7c0be6886" />



<img width="1072" height="679" alt="image" src="https://github.com/user-attachments/assets/2ffcec44-dd6f-4578-a60d-d43e8ae49795" />

<h2> Continue Setting up osTicket in the browser<h2>

  
  


## We have created our database, now we will go back to our installation of Osticket,
and add the credentials we used in connecting to our session.
- Click “Install Now!”
  



<img width="853" height="1247" alt="image" src="https://github.com/user-attachments/assets/3ace9a67-30bc-4362-9a29-8b165728b1bc" />

- ## The installation is successful.
<img width="774" height="607" alt="image" src="https://github.com/user-attachments/assets/18c99249-5152-475a-a25a-d3d6c607a543" />


# Go back to Heidi and the refresh 

<img width="1004" height="663" alt="image" src="https://github.com/user-attachments/assets/e6ca1603-726e-4603-9c3a-00c8836499d5" />

 ## Observe all the tables that Osticket will use to store all our data.










