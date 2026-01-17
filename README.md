<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Web Server IIS(Internet Information Services)
- PHP Manager for IIS
- URL Rewrite Module
- Database (MySQL 5.5)
- Configuration File
- OAuth2 Plugin

<h2>Phase 1: Azure VM Provisioning</h2>
</p>

<h3>Step 1: Create the Virtual Machine</h3>

- Image: Windows 10 Pro
- Size: 4 vCPUs (Standard_D4s_v3 or similar)
- VM Name: osticket-vm
- Username: labuser
- Password: osTicketPassword1!
- Inbound Port Rules: Ensure RDP (3389) and HTTP (80) are allowed.

<p>
<br />  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />  
<h2>Phase 2: Environment Preparation</h2>
</p>

<h3>Step 2: Remote Access and File Preparation</h3>


- Connect to the VM using Remote Desktop Connection.
- Download the osTicket-Installation-Files.zip within the VM.
- Unzip the folder to your Desktop

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 3: Enable Internet Information Services (IIS)</h3>  
<p>

- Open Control Panel > Programs > Turn Windows features on or off.
- Check Internet Information Services.
- Expand World Wide Web Services > Application Development Features.
- Check CGI, then click OK


</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />

<h2>Phase 3: Dependency Installation</h2>
</p>

<h3>Step 4: Install IIS Extensions & Visual C++</h3>

**From the "osTicket-Installation-Files" folder, run the following installers:**


- PHP Manager: PHPManagerForIIS_V1.5.0.msi
- Rewrite Module: rewrite_amd64_en-US.msi
- Visual C++ Redistributable: VC_redist.x86.exe
  


</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 5: Configure PHP 7.3.8</h3>  

- Create a new directory at C:\PHP.
- Unzip php-7.3.8-nts-Win32-VC15-x86.zip into C:\PHP.
- Open IIS Manager as Administrator.
- Select your server, open PHP Manager, and click Register new PHP version.
- Select C:\PHP\php-cgi.exe.
- Restart IIS (Select server in left pane > Restart in right pane)
- From the “osTicket-Installation-Files” folder install the Rewrite Module
  (rewrite_amd64_en-US.msi)

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 6: Install and Configure MySQL</h3>  

- Run mysql-5.5.62-win32.msi.
- Choose Typical setup.
- Launch the Configuration Wizard after install.
- Choose Standard Configuration.
- Set Password to root (Username: root)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />

<h2>Phase 4: osTicket Deployment</h2>
</p>

<h3>Step 7: Configure Web Directory</h3>
  
- Unzip osTicket-v1.15.8.zip.
- Copy the upload folder and paste it into C:\inetpub\wwwroot.
- Rename the folder from upload to osTicket.
- Restart IIS.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 8: Enable PHP Extensions</h3> 

- In IIS Manager, navigate to Sites > Default Web Site > osTicket.
- Open PHP Manager > Enable or disable an extension.
- Enable the following: php_imap.dll, php_intl.dll, and php_opcache.dll
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 9: Configure ost-config.php Permissions</h3>   

- Navigate to C:\inetpub\wwwroot\osTicket\include\.
- Rename ost-sampleconfig.php to ost-config.php.
- Right-click ost-config.php > Properties > Security > Advanced.
- Click Disable inheritance > Remove all inherited permissions.
- Click Add > Select a principal > type "Everyone" > Give Full control

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h2>Phase 5: Database and Final Setup</h2>
</p>

<h3>Step 10: Create Database via HeidiSQL</h3> 


- Install and open HeidiSQL.
- Create a new session using root / root.
- Right-click the session > Create new > Database.
- Name the database osTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 11: Run osTicket Web Installer</h3>   

- Open a browser and go to http://localhost/osTicket.
- Fill out the System Settings and Admin User info.
- Under Database Settings, use:
  1.  MySQL Database: osTicket
  2.  MySQL Username: root
  3.  MySQL Password: root
- Click Install Now
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 12: Verification</h3>  

- Staff Control Panel: http://localhost/osTicket/scp/login.php
- End User Portal: http://localhost/osTicket/
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


<br />
