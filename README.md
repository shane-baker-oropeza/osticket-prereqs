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
<img width="1421" height="773" alt="Screenshot 2026-01-16 232806" src="https://github.com/user-attachments/assets/0db579c2-368e-42fb-b65d-2df1ba0a5c77" />

</p>
<p>

<p>
<img width="873" height="767" alt="Screenshot 2026-01-16 232846" src="https://github.com/user-attachments/assets/061e40eb-28e2-42b3-aca8-2dc7009b1371" />

</p>

<p>
<img width="971" height="878" alt="Screenshot 2026-01-16 232927" src="https://github.com/user-attachments/assets/9a131917-541a-4a67-a2b4-b0982ac7c1aa" />

</p>

<p>
<img width="869" height="785" alt="Screenshot 2026-01-16 232942" src="https://github.com/user-attachments/assets/42a4c9c4-ae6b-4bfb-b104-a4a6c8b0eb20" />

</p>

<p>
<img width="881" height="806" alt="Screenshot 2026-01-16 233004" src="https://github.com/user-attachments/assets/36606530-0378-4534-aa81-cc0e27a613a2" />

</p>

<p>
<img width="770" height="806" alt="Screenshot 2026-01-16 233033" src="https://github.com/user-attachments/assets/87acee00-2818-4c2e-82bf-32e0b8ccd39d" />

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
<img width="1639" height="572" alt="Screenshot 2026-01-16 233327" src="https://github.com/user-attachments/assets/0ab0d8a8-1400-4f2c-adb2-b316148112b9" />

</p>
<p>

<p>
<img width="433" height="248" alt="Screenshot 2026-01-16 233423" src="https://github.com/user-attachments/assets/c8aeace5-ee97-427d-bbd6-c146dbcf6eaf" />

</p>

<p>
<img width="412" height="496" alt="Screenshot 2026-01-16 233531" src="https://github.com/user-attachments/assets/a8a98ac0-6ec6-42bd-a26f-7dc54b385b73" />

</p>

<p>
<img width="1095" height="453" alt="Screenshot 2026-01-16 233806" src="https://github.com/user-attachments/assets/987f7024-7808-45a4-ac94-99b99d6bcfbd" />

</p>

<p>
<img width="579" height="252" alt="Screenshot 2026-01-16 233817" src="https://github.com/user-attachments/assets/8adf0185-f831-4da3-a6ab-3e6a69f730c0" />

</p>

<p>
<img width="840" height="538" alt="Screenshot 2026-01-16 233935" src="https://github.com/user-attachments/assets/b164c523-b01a-488e-9f08-e742e7d9c4c3" />

</p>

<p>
<img width="855" height="672" alt="Screenshot 2026-01-16 234009" src="https://github.com/user-attachments/assets/733ff052-d844-4fd3-8926-3ad0372f96c4" />

</p>

<p>
<img width="396" height="479" alt="Screenshot 2026-01-16 234058" src="https://github.com/user-attachments/assets/3d432dbd-f635-4ffa-bf26-110be44eeb8d" />

</p>

<p>
<img width="672" height="520" alt="Screenshot 2026-01-16 234119" src="https://github.com/user-attachments/assets/ab4523fb-46d5-4c3a-8fff-96fe9abbe434" />

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
<img width="822" height="689" alt="Screenshot 2026-01-16 234441" src="https://github.com/user-attachments/assets/900d5be0-1b78-4eb7-bc18-62c76142779f" />

</p>
<p>

<p>
<img width="985" height="541" alt="Screenshot 2026-01-16 234504" src="https://github.com/user-attachments/assets/0e463ecf-8e16-42da-9822-bbdcc15f2cec" />

</p>

<p>
<img width="1148" height="457" alt="Screenshot 2026-01-16 234521" src="https://github.com/user-attachments/assets/5916d2d5-2c9a-4c73-9b4f-4b2b27efbbc3" />

</p>

<p>
<img width="442" height="381" alt="Screenshot 2026-01-16 234559" src="https://github.com/user-attachments/assets/d26051e7-b066-42c4-a364-edbf4b89e3eb" />

</p>

<p>
<img width="442" height="385" alt="Screenshot 2026-01-16 234637" src="https://github.com/user-attachments/assets/b46ae479-b3b2-4aa0-b808-d5b9f1994a84" />

</p>

<p>
<img width="430" height="381" alt="Screenshot 2026-01-16 234653" src="https://github.com/user-attachments/assets/c064814e-31f2-49e1-a17a-b6003bf2cac7" />

</p>

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
