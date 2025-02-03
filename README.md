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

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img width="354" alt="image" src="https://github.com/user-attachments/assets/24e2da6b-3031-446e-bb34-3c39d7993f79" />
<img width="354" alt="image" src="https://github.com/user-attachments/assets/d23cd52b-e23a-4f53-a17a-b4deb50829df" />
<img width="230" alt="image" src="https://github.com/user-attachments/assets/d68b7a97-3e41-447e-a292-d5084fa73043" />

</p>
<p>
First you must install the IIS (internet infomation service) by going to control panel and selecting uninstall programs. Then at your top left click turn windows features on or off. An box should appear, scroll down until you see internet infomation services. Click the box to fill it then click the plus next to the box to open more features, do the same to world wide web services and application development features. Then click the box next to CGI press ok then close
</p>
<br />

<p>
<img width="379" alt="image" src="https://github.com/user-attachments/assets/00820ffc-522a-43da-b9d2-0e7d3c82ef69" />
</p>
<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS.Then from the “osTicket-Installation-Files” folder install the Rewrite Module. Now from here you will create an directory name C:\PHP, to do this go to the bottem of the screen right click the file folder go to file explorer and in your C Drive create PHP folder. At this point unzip and extract the PHP file into the PHP folder that you just created. From the osticket-installation-Files folder install VC_redist x66.exe. Next from the osTicket-installation-files folder again install MYSQL 5.5.62 
  - Typical Setup
  - Launch Configuration Wizard (after install)
  - Standard Configuration
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS an Admin, then register PHPfrom within IIS (PHP Manager - C:\PHP\php-cgi.exe). Now you need to reload IIS (stop and start the server witnin the IIS). From here you must install osTicket v1.15.8, so from osTicket-installation-Files folder unzip "osTicket-v1.15.8.zip" and copy the upload folder into C:\inetpub\wwwroot within the C:\inetpub\wwwroot, Rename upload to osTicket. Reload IIS stop and start the server. Now in IIS go to sites-> Default-> osTicket -Onthe right , click Browse *:80 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you need to note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
MAKE SURE TO GET THIS RIGHT!

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

Continue Setting up osTicket in the browser click continue
Name Helpdesk
Default email (receives email from customers)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL
- Open Heidi SQL
- Create a new session, username/password
- Connect to the session
- Create a database called “osTicket”

Continue Setting up osTicket in the browser
- MySQL Database: osTicket
- MySQL Username: 
- MySQL Password: 
Click “Install Now!”

Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page
</p>
<br />
