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
<img width="266" height="190" alt="Screenshot 2026-01-16 234846" src="https://github.com/user-attachments/assets/c68c59fa-98eb-40fb-bb2a-91808b3e46fa" />

</p>
<p>

<p>
<img width="817" height="481" alt="Screenshot 2026-01-16 234853" src="https://github.com/user-attachments/assets/66c21dd5-e068-4eee-96a8-ad2da97288f5" />

</p>

<p>
<img width="823" height="410" alt="Screenshot 2026-01-16 234901" src="https://github.com/user-attachments/assets/b53b9788-a9c8-4fa1-82fe-a8d24a338e13" />

</p>

<p>
<img width="783" height="394" alt="Screenshot 2026-01-16 235011" src="https://github.com/user-attachments/assets/68abb21b-a42f-4d04-8441-f5b3f85ece72" />

</p>

<p>
<img width="791" height="492" alt="Screenshot 2026-01-16 235640" src="https://github.com/user-attachments/assets/92036652-cb8f-4fd6-aba8-649476bff3d3" />

</p>
<br />

<h3>Step 5: Configure PHP 7.3.8</h3>  

- Create a new directory at C:\PHP.
- Unzip php-7.3.8-nts-Win32-VC15-x86.zip into C:\PHP.
- Open IIS Manager as Administrator.
- Select your server, open PHP Manager, and click Register new PHP version.
- Select C:\PHP\php-cgi.exe.
- Restart IIS (Select server in left pane > Restart in right pane)

</p>
<br />

<p>
<img width="290" height="490" alt="Screenshot 2026-01-16 235141" src="https://github.com/user-attachments/assets/9abfc8bb-a079-4006-8129-a1643990f826" />

</p>
<p>

<p>
<img width="795" height="647" alt="Screenshot 2026-01-16 235219" src="https://github.com/user-attachments/assets/bd96f365-c571-4f10-af64-cd338075ec3b" />

</p>

<p>
<img width="810" height="721" alt="Screenshot 2026-01-16 235235" src="https://github.com/user-attachments/assets/38409a4b-1d5a-4255-82b4-8bf9e3090772" />

</p>

<p>
<img width="801" height="655" alt="Screenshot 2026-01-16 235254" src="https://github.com/user-attachments/assets/49c86ec4-f320-4546-80fa-1ca7262e4d04" />

</p>

<p>
<img width="730" height="617" alt="Screenshot 2026-01-16 235421" src="https://github.com/user-attachments/assets/8d189a66-083e-4877-ad45-9dd1a424958b" />


</p>

<p>
<img width="606" height="445" alt="Screenshot 2026-01-16 235519" src="https://github.com/user-attachments/assets/fdd390d3-c191-4c52-abd1-52384d125dc0" />

</p>

<p>
<img width="859" height="675" alt="Screenshot 2026-01-17 000324" src="https://github.com/user-attachments/assets/428539b9-8d45-4693-b10a-bb38102b45b3" />

</p>

<p>
<img width="1111" height="527" alt="Screenshot 2026-01-17 000426" src="https://github.com/user-attachments/assets/ad991cc5-6bdb-48fb-8fdc-86b0bc9017db" />

</p>

<p>
<img width="971" height="520" alt="Screenshot 2026-01-17 000438" src="https://github.com/user-attachments/assets/7ec8d5ce-1724-4107-b122-cf5be8aa4741" />

</p>

<p>
<img width="522" height="236" alt="Screenshot 2026-01-17 000544" src="https://github.com/user-attachments/assets/01a73e1e-8d03-4647-bdf8-3da16f427bf2" />

</p>

<p>
<img width="1320" height="500" alt="Screenshot 2026-01-17 000620" src="https://github.com/user-attachments/assets/71b74470-5391-46a8-bc85-098edfb8296c" />

</p>

<p>
<img width="243" height="344" alt="Screenshot 2026-01-17 000632" src="https://github.com/user-attachments/assets/cdce3ace-31b9-437e-813d-86c8ea678388" />

</p>

<p>
<img width="226" height="359" alt="Screenshot 2026-01-17 000640" src="https://github.com/user-attachments/assets/2f92f904-1244-49b3-b308-2079fe3b1c5f" />

</p>
<br />

<h3>Step 6: Install and Configure MySQL</h3>  

- Run mysql-5.5.62-win32.msi.
- Choose Typical setup.
- Launch the Configuration Wizard after install.
- Choose Standard Configuration.
- Set Password to root (Username: root)
</p>
<br />

<p>
<img width="796" height="435" alt="Screenshot 2026-01-16 235719" src="https://github.com/user-attachments/assets/42caf90c-840d-4727-a235-abece302dc1f" />

</p>
<p>

<p>
<img width="513" height="403" alt="Screenshot 2026-01-16 235813" src="https://github.com/user-attachments/assets/bcf88e9a-8173-4821-aea6-8c4ca2fdb3fc" />

</p>

<p>
<img width="515" height="408" alt="Screenshot 2026-01-16 235845" src="https://github.com/user-attachments/assets/20f75612-82ff-4a1d-b426-ef0f5dbe7703" />

</p>

<p>
<img width="525" height="395" alt="Screenshot 2026-01-16 235916" src="https://github.com/user-attachments/assets/73aeaa8c-56a1-4051-9833-0ee0df1ee6ee" />

</p>

<p>
<img width="520" height="399" alt="Screenshot 2026-01-16 235927" src="https://github.com/user-attachments/assets/f347780f-a333-4cff-912f-2eaefeccc1d1" />

</p>

<p>
<img width="520" height="392" alt="Screenshot 2026-01-16 235956" src="https://github.com/user-attachments/assets/6c2d67f0-1adc-4ad8-84bf-64d2fbf0088e" />

</p>

<p>
<img width="515" height="389" alt="Screenshot 2026-01-17 000015" src="https://github.com/user-attachments/assets/1676bc49-5549-419c-8c6b-e6c3b773f5ad" />

</p>

<p>
<img width="517" height="395" alt="Screenshot 2026-01-17 000223" src="https://github.com/user-attachments/assets/35a1614b-62ec-42b9-b729-97433e2ae85c" />

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
<img width="803" height="659" alt="Screenshot 2026-01-17 000801" src="https://github.com/user-attachments/assets/fc34d3ba-1ea6-4c3a-8abd-c7541a60aab9" />

</p>

<p>
<img width="624" height="457" alt="Screenshot 2026-01-17 000813" src="https://github.com/user-attachments/assets/a293c3e3-c260-47ff-aa76-a9f3d2a28575" />

</p>

<p>
<img width="778" height="639" alt="Screenshot 2026-01-17 001037" src="https://github.com/user-attachments/assets/dc9ee95b-b228-4dd1-9d5b-da41a7546a8d" />

</p>

<p>
<img width="289" height="659" alt="Screenshot 2026-01-17 001058" src="https://github.com/user-attachments/assets/53fabc1a-5a51-49eb-8a07-ffc69f856ebb" />

</p>

<p>
<img width="762" height="617" alt="Screenshot 2026-01-17 001115" src="https://github.com/user-attachments/assets/6b539a34-f269-43b3-a93f-3d3f5a8287c7" />

</p>

<p>
<img width="780" height="404" alt="Screenshot 2026-01-17 001125" src="https://github.com/user-attachments/assets/51336414-65fc-44f7-9265-1b777d19d3c1" />

</p>

<p>
<img width="779" height="449" alt="Screenshot 2026-01-17 001136" src="https://github.com/user-attachments/assets/5c317f40-62df-44df-b3ec-9afe912c647d" />

</p>

<p>
<img width="1345" height="578" alt="Screenshot 2026-01-17 001226" src="https://github.com/user-attachments/assets/56bd2a7a-f07f-4cef-a03f-df2bf12f0031" />

</p>

<p>
<img width="779" height="421" alt="Screenshot 2026-01-17 001240" src="https://github.com/user-attachments/assets/9ef61ada-5d08-48ef-9fbc-8fb9be9b5ed7" />

</p>

<p>
<img width="599" height="585" alt="Screenshot 2026-01-17 001326" src="https://github.com/user-attachments/assets/8202e2d9-e1db-4774-bcc9-e75c3067910a" />

</p>

<p>
<img width="778" height="366" alt="Screenshot 2026-01-17 001340" src="https://github.com/user-attachments/assets/8a39ea21-f156-4d98-a359-743d15262eab" />

</p>

<p>
<img width="1250" height="695" alt="Screenshot 2026-01-17 001435" src="https://github.com/user-attachments/assets/04f24b96-8353-441b-88a5-baaa7d4192bf" />

</p>

<p>
<img width="229" height="262" alt="Screenshot 2026-01-17 001442" src="https://github.com/user-attachments/assets/6ba8acdf-6542-4312-9004-5fd6e9af3158" />

</p>

<p>
<img width="215" height="313" alt="Screenshot 2026-01-17 001451" src="https://github.com/user-attachments/assets/ab20eb05-f57e-4c3f-afa0-5e01911862c6" />

</p>
<br />


<p>

<h3>Step 8: Enable PHP Extensions</h3> 

- In IIS Manager, navigate to Sites > Default Web Site > osTicket.
- Open PHP Manager > Enable or disable an extension.
- Enable the following: php_imap.dll, php_intl.dll, and php_opcache.dll
</p>
<br />

<p>
<img width="1043" height="432" alt="Screenshot 2026-01-17 001558" src="https://github.com/user-attachments/assets/5714a931-b6bd-445d-ae05-473412b124fb" />

</p>

<p>
<img width="1262" height="393" alt="Screenshot 2026-01-17 001623" src="https://github.com/user-attachments/assets/0036b969-79ff-4c71-be60-562fbc8c5182" />

</p>

<p>
<img width="845" height="761" alt="Screenshot 2026-01-17 001641" src="https://github.com/user-attachments/assets/149b8569-14f2-4cb3-be20-0685737a10c3" />

</p>

<p>
<img width="1267" height="503" alt="Screenshot 2026-01-17 002105" src="https://github.com/user-attachments/assets/36b3c53a-427c-4343-9d8a-85da3a5b306c" />

</p>

<p>
<img width="920" height="660" alt="Screenshot 2026-01-17 002124" src="https://github.com/user-attachments/assets/7d909a73-9661-44f9-bbad-596bb86871db" />

</p>

<p>
<img width="661" height="652" alt="Screenshot 2026-01-17 002211" src="https://github.com/user-attachments/assets/bd4fdc9a-9a06-440e-84fc-edee4922774a" />

</p>

<p>
<img width="373" height="209" alt="Screenshot 2026-01-17 002241" src="https://github.com/user-attachments/assets/66f9f245-48b7-4f3f-b935-1fec05646a9e" />

</p>

<p>
<img width="307" height="159" alt="Screenshot 2026-01-17 002301" src="https://github.com/user-attachments/assets/cb108510-3bab-4b6c-88da-66e431084b31" />

</p>

<p>
<img width="350" height="195" alt="Screenshot 2026-01-17 002332" src="https://github.com/user-attachments/assets/e3a7b62e-f3a5-4f25-9857-0667b3d4fbfd" />

</p>

<p>
<img width="840" height="752" alt="Screenshot 2026-01-17 002426" src="https://github.com/user-attachments/assets/a379ae36-93de-43c4-b815-a216943260d5" />

</p>
<br />


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
<img width="312" height="665" alt="Screenshot 2026-01-17 002521" src="https://github.com/user-attachments/assets/d4475e3b-50ac-45d5-a6a5-6f79b95ce362" />

</p>

<p>
<img width="732" height="554" alt="Screenshot 2026-01-17 002538" src="https://github.com/user-attachments/assets/c030e295-9dda-4a3e-9b19-111f197d197c" />

</p>

<p>
<img width="603" height="563" alt="Screenshot 2026-01-17 002550" src="https://github.com/user-attachments/assets/0abc0551-8750-4bd4-b88b-afc3a74c485a" />

</p>

<p>
<img width="587" height="546" alt="Screenshot 2026-01-17 002600" src="https://github.com/user-attachments/assets/54feab4d-3a39-471f-97f7-e967da726ea4" />

</p>

<p>
<img width="592" height="527" alt="Screenshot 2026-01-17 002628" src="https://github.com/user-attachments/assets/99c90cd6-e5dd-4051-82bf-6a57de0047f6" />

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

<h3>Step 12: Verification</h3>  

- Staff Control Panel: http://localhost/osTicket/scp/login.php
- End User Portal: http://localhost/osTicket/
</p>
<br />

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


<br />
