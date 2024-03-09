<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<!---<h2>Video Demonstration</h2>

 ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) --->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install / Enable IIS in Windows
- Download / Install PHP Manager for IIS
- Download / Install the Rewrite Module 
- Create the directory C:\PHP
- Download / Unzip PHP 7.3.8
- Download / Install VC_redist.x86.exe.
- Download / Install MySQL 5.5.62

<h2>Installation Steps</h2>

<p>
We will configure and activate Internet Information Services (IIS), a robust web server platform that enables a computer to host websites. Given that OsTicket operates through a web interface, it's essential to establish and fine-tune IIS settings to ensure the seamless operation of OsTicket<br/> 
 
Initiate the process by right-clicking the Start menu, selecting 'Run', and then entering 'control' to access the Control Panel. Navigate to 'Programs' and select 'Turn Windows features on or off'. Within the list, locate 'Internet Information Services > World Wide Web Services > Application Development Features'. Here, ensure to enable 'CGI' along with all of the 'Common HTTP Features' to properly configure the server environment. Select 'Ok' to initiate installation.
</p>
<p>
<img src="https://i.imgur.com/OxWAXSI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
To verify the successful installation of IIS, open your web browser and enter '127.0.0.1' into the address bar. This IP address is known as the 'localhost' and is used to refer to the computer you're currently using. If IIS has been installed and configured correctly, you should be greeted with the default IIS welcome page. This step is crucial as it confirms that your system is properly set up to host web applications</p>
<p>
<img src="https://i.imgur.com/bn3eMwO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<p>
<img src="https://i.imgur.com/BIBNx8G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<p>
<img src="https://i.imgur.com/MojMcEE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create the directory C:\PHP
</p>
<p>
<img src="https://i.imgur.com/0F9SS1a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip). Extract all</p>
<p>
<img src="https://i.imgur.com/vXEcmob.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Unzip the contents into C:\PHP</p>
<p>
<img src="https://i.imgur.com/vVyAPL7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Download and install VC_redist.x86.exe.
</p>
<p>
<img src="https://i.imgur.com/CrdtBtx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Choose a Typical Setup.
</p>
<p>
<img src="https://i.imgur.com/M9opU8P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Choose a Standard Configuration and Install as Windows Service</p>
<p>
<img src="https://i.imgur.com/N5n9W93.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Set your password</p>
<p>
<img src="https://i.imgur.com/nEoJbvK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>Finish
</p>
<p>
<img src="https://i.imgur.com/ZDXYRrn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Open IIS as an Admin
</p>
<p>
<img src="https://i.imgur.com/Ufbhfay.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
In IIS go to PHP Manager. You will see an alert that says "PHP is not enabled. Register new PHP version to enable PHP via FastCGI". Click on Register new PHP version.
Search files and go to C: > PHP > php.cgi</p>
<p>
<img src="https://i.imgur.com/GQiCl2C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Stop and Start the server</p>
<p>
<img src="https://i.imgur.com/2OGb66D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Install osTicket v1.15.8. Next extract and copy “upload” folder to c:\inetpub\wwwroot
</p>
<p>
<img src="https://i.imgur.com/6dhjmSn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/ePEcOFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
</p>
<p>
<img src="https://i.imgur.com/UNa9ilP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Stop and Start the server
</p>
<p>
<img src="https://i.imgur.com/2OGb66D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go to sites -> Default -> osTicket and then on the right, click “Browse *:80”
</p>
<p>
<img src="https://i.imgur.com/SmnEbS4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Clicking "Browse *:80" will take us to the OsTicket Installer page</p>
<p>
<img src="https://i.imgur.com/qkOyY68.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go back to IIS, sites -> Default -> osTicket
<br />Double-click PHP Manager
<br />Click “Enable or disable an extension”
<br />Enable: php_imap.dll
<br />Enable: php_intl.dll
<br />Enable: php_opcache.dll
</p>
<p>
<img src="https://i.imgur.com/YfEM2IX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Refresh the osTicket site in your browser, observe the changes
</p>
<p>
<img src="https://i.imgur.com/eLsB2z1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Rename: ost-config.php<br />
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php<br />
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<p>
<img src="https://i.imgur.com/EJ9xThR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/Dh3Ht79.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Assign Permissions: ost-config.php<br />
Right Click ost-config.php > Security > Advanced > Disable inheritance > Remove All</p>
<p>
<img src="https://i.imgur.com/77xA0ZO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Add and assign New Permissions > Everyone 
</p>
<p>
<img src="https://i.imgur.com/wuV1SG2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Check all Basic Permissions
</p>
<p>
<img src="https://i.imgur.com/pcdaUNz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Apply and ok the new permissions</p>
<p>
<img src="https://i.imgur.com/u8dfePc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Continue Setting up osTicket in the browser (click Continue)
</p>
<p>
<img src="https://i.imgur.com/NgnKYro.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Name the Helpdesk<br />
Default email (receives email from customers) and setup the admin user
</p>
<p>
<img src="https://i.imgur.com/iY8r81o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>We will fill out this section after installing HeidiSQL</p>
</p>
<p>
<img src="https://i.imgur.com/UjGKuId.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>download and install HeidiSQL.</p>
<p>
<img src="https://i.imgur.com/CE8T33M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>Open Heidi SQL
<p>
<img src="https://i.imgur.com/iPeq7hA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>Create a new session and set the root password. Finish by clicking open
</p>
<p>
<img src="https://i.imgur.com/yxklJrv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>Create a database called “osTicket”
</p>
<p>
<img src="https://i.imgur.com/vBasAeP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/EvuDpoM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Continue Setting up osticket in the browser <br />
MySQL Database: osTicket <br />
MySQL Username: root <br />
MySQL Password: Password1 <br />
Click “Install Now”
</p>
<p>
<img src="https://i.imgur.com/P6pcsNu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Congratulations! OsTicket has been installed<br />
</p>
<p>
<img src="https://i.imgur.com/NeOuu0Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Clean up <br /> 
Delete: C:\inetpub\wwwroot\osTicket\setup
</p>
<p>
<img src="https://i.imgur.com/Otb5XZR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<p>
<img src="https://i.imgur.com/ivK5wtD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Browse to your help desk login page: http://localhost/osTicket/scp/login.php
</p>
<p>
<img src="https://i.imgur.com/mVIqDbk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/UDawVdl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


