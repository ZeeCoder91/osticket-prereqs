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
To verify the successful installation of IIS, open your web browser and enter '127.0.0.1' into the address bar. This IP address is known as the 'localhost' and is used to refer to the computer you're currently using. If IIS has been installed and configured correctly, you should be greeted with the default IIS welcome page. This step is crucial as it confirms that your system is properly set up to host web applications.</p>
<p>
<img src="https://i.imgur.com/bn3eMwO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Proceed by Locating and downloading the 'PHP Manager for IIS' installer, specifically version 1.5.0 (PHPManagerForIIS_V1.5.0.msi). This tool is instrumental for seamlessly integrating PHP into your IIS environment, enabling dynamic content generation. Once downloaded, execute the installer to integrate PHP Manager into your IIS setup, thereby preparing your system for robust web development tasks involving PHP.</p>
<p>
<img src="https://i.imgur.com/BIBNx8G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the Installation Files, download and install 'rewrite_amd64_en-US.msi' to enable URL rewriting, improving website navigation and SEO.</p>
<p>
<img src="https://i.imgur.com/MojMcEE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
For optimal organization and accessibility, create a directory at C:\PHP to house PHP version 7.3.8. Specifically, use the non-thread safe version for Windows (php-7.3.8-nts-Win32-VC15-x86.zip) because when configuring PHP for use with IIS, the NTS version is preferred for its compatibility with FastCGI, improved performance, and more efficient resource management. This ensures that web applications run smoothly, with optimal response times and reliability. This dedicated folder streamlines PHP management and configuration within your environment.</p>
<p>
<img src="https://i.imgur.com/0F9SS1a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Download the PHP 7.3.8 package (php-7.3.8-nts-Win32-VC15-x86.zip) and proceed to extract all contents.</p>
<p>
<img src="https://i.imgur.com/vXEcmob.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Extract the contents of the downloaded file into the C:\PHP directory.</p>
<p>
<img src="https://i.imgur.com/vVyAPL7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
For ensuring compatibility and optimal performance of PHP on Windows, it is imperative to download and install 'VC_redist.x86.exe'. This step involves installing the Visual C++ Redistributable for Visual Studio 2015, a package of DLL (Dynamic Link Library) files required by PHP and other applications to run smoothly. These libraries are essential runtime components supporting the execution of C++ applications built with Visual Studio 2015. Installing this package guarantees that your system is equipped with all necessary components to efficiently run PHP, thereby preventing potential issues related to missing libraries.
</p>
<p>
<img src="https://i.imgur.com/CrdtBtx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Download and execute the installation of MySQL version 5.5.62 using the file 'mysql-5.5.62-win32.msi'. Opt for a 'Typical Setup' during installation to efficiently establish a dependable database management system, ensuring broad compatibility and strong performance.</p>
<p>
<img src="https://i.imgur.com/M9opU8P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Select 'Standard Configuration' and opt to install as a Windows Service. This streamlined approach simplifies the setup process, ensuring MySQL runs automatically and reliably in the background as a service, providing stability and ease of management for your database system.</p>
<p>
<img src="https://i.imgur.com/N5n9W93.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Enter the root password.</p>
<p>
<img src="https://i.imgur.com/nEoJbvK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>Complete the MySQL installation process.
</p>
<p>
<img src="https://i.imgur.com/ZDXYRrn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Launch IIS with Administrator privileges.</p>
<p>
<img src="https://i.imgur.com/Ufbhfay.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
In PHP Manager, when prompted with 'PHP is not enabled. Register new PHP version to enable PHP via FastCGI,' click 'Register new PHP version.' Then, in the C:\PHP directory, select 'php.cgi.' This step is key for enabling PHP script processing through FastCGI in IIS, essential for dynamic content delivery.</p>
<p>
<img src="https://i.imgur.com/GQiCl2C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
In PHP Manager, simply click to 'Stop' and then 'Start' the server. This action refreshes the server settings, applying any new configurations and ensuring PHP is properly integrated and operational within IIS.</p>
<p>
<img src="https://i.imgur.com/2OGb66D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
"Install osTicket version 1.15.8, then extract the package and copy the 'upload' folder to c:\inetpub\wwwroot. This step places osTicket's necessary files in the web server's root directory, preparing it for configuration and use."
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
In the c:\inetpub\wwwroot directory, rename the 'upload' folder to 'osTicket'. This adjustment organizes your installation, clearly identifying osTicket's application files within your web server's root directory.</p>
<p>
<img src="https://i.imgur.com/UNa9ilP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Stop and Start the server. To refresh the server settings and apply the new configurations.
</p>
<p>
<img src="https://i.imgur.com/2OGb66D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Navigate to 'Sites' -> 'Default Web Site' -> 'osTicket' in IIS. Then, on the right panel, click on 'Browse *:80'. This action initiates a browser session to access your osTicket installation via the default HTTP port, allowing you to verify the application's deployment and accessibility.</p>
<p>
<img src="https://i.imgur.com/SmnEbS4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
By clicking "Browse *:80," you will be directed to the osTicket Installer page. This step effectively launches your web browser to display the setup interface for osTicket, indicating that the application is accessible and ready for installation and configuration on your server.</p>
<p>
<img src="https://i.imgur.com/qkOyY68.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
In PHP Manager, follow these steps to enable specific DLLs (Dynamic Link Libraries):
<br />1. Navigate to the "PHP Extensions" section.
<br />2. Find and enable php_imap.dll, php_intl.dll, and php_opcache.dll by checking their corresponding boxes.
<br />3. Apply the changes. 
</p>

<p>This process activates the IMAP, Internationalization, and Opcode Cache extensions, enhancing PHP functionality.</p>
<p>
<img src="https://i.imgur.com/YfEM2IX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Reload the osTicket site in your browser to observe any updates or changes that have taken effect.</p>
<p>
<img src="https://i.imgur.com/eLsB2z1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Rename the file from 'ost-sampleconfig.php' to 'ost-config.php' located at C:\inetpub\wwwroot\osTicket\include. This step transitions the osTicket configuration file from a sample template to its active form, enabling further customization and setup.
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
Set permissions for 'ost-config.php' by right-clicking on the file and navigating to Security > Advanced > Disable inheritance, then select 'Remove All.' This action secures the configuration file by customizing its permission settings, ensuring that only authorized users and processes have access, which is a crucial step in protecting sensitive information within the osTicket system.</p>
<p>
<img src="https://i.imgur.com/77xA0ZO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Assign 'New Permissions' to 'Everyone' to ensure broad access while maintaining security.</p>
<p>
<img src="https://i.imgur.com/wuV1SG2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Ensure all Basic Permissions are selected.</p>
<p>
<img src="https://i.imgur.com/pcdaUNz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
"Click 'Apply' to confirm, then 'OK' to set the new permissions.</p>
<p>
<img src="https://i.imgur.com/u8dfePc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
In your browser, proceed with setting up osTicket by clicking 'Continue'.
</p>
<p>
<img src="https://i.imgur.com/NgnKYro.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
For osTicket setup, name your Helpdesk, specify the Default email (for receiving customer emails), and create the admin user account.
</p>
<p>
<img src="https://i.imgur.com/iY8r81o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>After installing HeidiSQL, proceed to fill in the database details in the osTicket installer.</p>
</p>
<p>
<img src="https://i.imgur.com/UjGKuId.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>"Download and install HeidiSQL. This step equips your system with a powerful database management tool, enabling efficient handling and administration of your databases, a necessary component for managing the backend of applications like osTicket.</p>
<p>
<img src="https://i.imgur.com/CE8T33M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>"Launch HeidiSQL.
<p>
<img src="https://i.imgur.com/iPeq7hA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>Create a new session and enter the root password. Conclude by clicking 'Open'.
</p>
<p>
<img src="https://i.imgur.com/yxklJrv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>In HeidiSQL, create a database named 'osTicket'.
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
Proceed with the osTicket setup in your browser.<br />
MySQL Database: osTicket <br />
MySQL Username: root <br />
MySQL Password: ******** <br />
Click “Install Now”
</p>
<p>
<img src="https://i.imgur.com/P6pcsNu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Congratulations! OsTicket has been installed.<br />
</p>
<p>
<img src="https://i.imgur.com/NeOuu0Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Complete the cleanup process by deleting the 'C:\inetpub\wwwroot\osTicket\setup' folder. This step is important to remove installation files and secure your osTicket application."
</p>
<p>
<img src="https://i.imgur.com/Otb5XZR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Adjust the permissions of 'C:\inetpub\wwwroot\osTicket\include\ost-config.php' to 'Read-only.' This measure enhances security by preventing unauthorized modifications to the configuration file.</p>
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


