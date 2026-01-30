<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop (RDP)
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> 

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>

<p>
</p>
<p>
Welcome in this tutorial we will be setting up a virtual machine in azure, connecting to windows app (previously remote desktop) and installing osTicket.





  
 <img width="1433" height="809" alt="Screenshot 2026-01-29 at 2 12 07 PM" src="https://github.com/user-attachments/assets/931cfbc4-2ff6-4c61-ba45-158b93ca61ad" />

</p>
<br />
<p>
</p>
<p> We have created our virtual machine, now we connect to windows app (Remote Desktop) using the vm public IPv4 address. 
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
osTicket has been installed now we enable IIS (internet information services). In the virtual machine click the start menu, type control panel then select uninstall a program. on top left select "Turn windows features on or off". A list will appear from there  you will enable Internet Information Services.



  


</p>  <img width="785" height="679" alt="Screenshot 2026-01-29 at 4 25 09 PM" src="https://github.com/user-attachments/assets/460a306e-3c89-4cb7-ba3d-50f6eeb7e22f" />
<img width="909" height="413" alt="Screenshot 2026-01-29 at 4 27 27 PM" src="https://github.com/user-attachments/assets/dbd6af95-c634-4628-bdbd-92cf9abb876e" />
<img width="1123" height="592" alt="Screenshot 2026-01-29 at 4 41 35 PM" src="https://github.com/user-attachments/assets/becd5cef-fc36-40f7-8ee2-c30b99c17b0d" />





<img src="https://i.imgur.com/qtEnuWu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
</p>
<p>
Excellent. Now that you have enabled IIS we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
  That link will provide you with all of the material you need to download to get osTicket up and running. Simply click the link and install the Web Platform Installer
</p>
<img src="https://i.imgur.com/AxHCfQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Once you have installed Web Installer Platform open it. From inside the application you are going to install MySQL 5.5 Afterwards install x86 version of PHP up until 7.3. There are some failed files such as C++ redistributable package as well as PHP 7.3.8 and PHP Manager for IIS those files can be found with the install link.
</p>
<img src="https://i.imgur.com/JJ8bZeJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
</p>
<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
</P>
<img src="https://i.imgur.com/TUGiSKi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
Assign permissions to ost-config.php Disable inheritance->Removeall
New Permissions->Everyone->all
</p>
<img src="https://i.imgur.com/1nYaYGe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
Congratulations, hopefully it is installed with no errors!
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
