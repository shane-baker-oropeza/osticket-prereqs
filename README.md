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
<br />

<p>
<img width="873" height="767" alt="Screenshot 2026-01-16 232846" src="https://github.com/user-attachments/assets/061e40eb-28e2-42b3-aca8-2dc7009b1371" />

</p>
<br />

<p>
<img width="971" height="878" alt="Screenshot 2026-01-16 232927" src="https://github.com/user-attachments/assets/9a131917-541a-4a67-a2b4-b0982ac7c1aa" />

</p>
<br />

<p>
<img width="869" height="785" alt="Screenshot 2026-01-16 232942" src="https://github.com/user-attachments/assets/42a4c9c4-ae6b-4bfb-b104-a4a6c8b0eb20" />

</p>
<br />

<p>
<img width="881" height="806" alt="Screenshot 2026-01-16 233004" src="https://github.com/user-attachments/assets/36606530-0378-4534-aa81-cc0e27a613a2" />

</p>
<br />

<p>
<img width="770" height="806" alt="Screenshot 2026-01-16 233033" src="https://github.com/user-attachments/assets/87acee00-2818-4c2e-82bf-32e0b8ccd39d" />

</p>

<br />  
<h2>Phase 2: Environment Preparation</h2>
</p>

<h3>Step 2: Remote Access and File Preparation</h3>


- Connect to the VM using Remote Desktop Connection.
- Download the [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) within the VM.
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


