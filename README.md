<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
Project consists of setting up all the prerequisites and installing osTicket from scratch. This was done on a Windows 10 Virtual Machine I created in Azure. osTicket is a widely used and trusted open source Help Desk ticketing system.
</p> You can find all the necessary installation files used in this project.(https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
<br />


<h2>Environments and Technologies Used</h2>

</p>Microsoft Azure
</p>Virtual Machines
</p>Remote Desktop Connection
</p>Internet Information Services
</p>MySQL
<h2>Operating Systems Used </h2>

 Windows 10</b> 



<h2>Installation Steps</h2>

<p>
</p>
<p>
  Navigate to microsoft Azure and create a resource group.





  
 <img width="1352" height="785" alt="Screenshot 2026-02-10 at 8 35 13 AM" src="https://github.com/user-attachments/assets/55d702c2-7aa2-4ccd-b4ac-6d7bef0611a7" /><p><img width="1348" height="809" alt="Screenshot 2026-02-10 at 8 38 44 AM" src="https://github.com/user-attachments/assets/c452c69e-b3d3-4e28-946c-43a4caaddc44" />


<br /><p> my resource group has been created, now i will create the virtual machine<p><img width="1433" height="742" alt="Screenshot 2026-02-10 at 8 47 01 AM" src="https://github.com/user-attachments/assets/59c10c09-3f38-4db0-9b86-428b398980fc" /></p><img width="1432" height="805" alt="Screenshot 2026-02-10 at 8 52 58 AM" src="https://github.com/user-attachments/assets/028b5e07-93cc-4c77-aa68-818433917d3a" /><p><img width="1432" height="801" alt="Screenshot 2026-02-10 at 8 54 14 AM" src="https://github.com/user-attachments/assets/c7b66e8c-93cc-4e67-aa1d-f5bf2923bf49" />



<p>
</p>
<p> once everything has been created I'll use Remote Desktop to connect to my vm . 
</p>
<img width="1168" height="715" alt="Screenshot 2026-01-29 at 2 25 49 PM" src="https://github.com/user-attachments/assets/5b1b91dd-8c7f-45cf-9504-40b2e955e577" />


</p>
<br />  Now we will download, install, and unzipping os ticket 
<img width="717" height="249" alt="Screenshot 2026-01-29 at 3 57 08 PM" src="https://github.com/user-attachments/assets/c1672918-45cd-4443-b8fa-a71d404ccd76" />
<img width="618" height="457" alt="Screenshot 2026-01-29 at 3 57 49 PM" src="https://github.com/user-attachments/assets/d4c06eec-85b9-4435-a468-9606dc68c9d1" />
<img width="798" height="593" alt="Screenshot 2026-01-29 at 4 15 50 PM" src="https://github.com/user-attachments/assets/6364f533-bfb5-40de-a61d-015f41d60610" />




<p> 
</p>
<p>
osTicket has been installed now we need to enable IIS (internet information services). In the virtual machine, click the start menu, type control panel, on the bottom left select PROGRAM uninstall a program. On top left select Turn windows features on or off and  A list will appear from there  you will begin to enable IIS (Internet Information Services).



  


</p>  <img width="785" height="679" alt="Screenshot 2026-01-29 at 4 25 09 PM" src="https://github.com/user-attachments/assets/460a306e-3c89-4cb7-ba3d-50f6eeb7e22f" />
<img width="909" height="413" alt="Screenshot 2026-01-29 at 4 27 27 PM" src="https://github.com/user-attachments/assets/dbd6af95-c634-4628-bdbd-92cf9abb876e" />
<img width="1130" height="587" alt="Screenshot 2026-01-29 at 5 00 40 PM" src="https://github.com/user-attachments/assets/4273528f-e65e-4423-b8e2-f2f3de2e1f03" />






<>
</p>
<br />
</p>
<p>
IIS has been enabled now we need to install Web Platform Installer. Below i have provide an example of what we need to install and enable to get osTicket up and running. 
</p>
<img width="795" height="377" alt="Screenshot 2026-01-29 at 5 11 25 PM" src="https://github.com/user-attachments/assets/a4d61ec4-c6ee-4a67-9069-3adf6f4e5358" />
<img src="https://i.imgur.com/AxHCfQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>

<p>
</p>
<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
</P>
<<img width="612" height="594" alt="Screenshot 2026-01-30 at 12 59 57 PM" src="https://github.com/user-attachments/assets/700259c6-6924-423e-9ca3-599895ef96cc" />
>
</p>
<br />
<p>
</p>
<p>
Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
</p>
<img src="https://i.imgur.com/4AkTkV0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Go back into IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket
Then double click on PHP manager. Click on "Disable or enable an extension" Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and obsereve the changes "Intl Extension" should now be enabled. 
</p>
<img src="https://i.imgur.com/APZgUTT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php
Assign permissions to ost-config.php Disable inheritance->Remove all
New Permissions->Everyone->all
</p>
<img width="1440" height="900" alt="Screenshot 2026-01-30 at 1 21 07 PM" src="https://github.com/user-attachments/assets/9034acc5-7ed9-4dac-96c7-75f7cc928001" />

<br />
<p>
</p>
<p>
Afterwards continue setting up osTicket in the browser (click continue) then you will name the Helpdesk to your liking. Select a default email that will receive emails from customers who submit tickets. 
</p>
<img src="https://i.imgur.com/RmVk3q5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
<p>Continue Setting up osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1 Click “Install Now!”

