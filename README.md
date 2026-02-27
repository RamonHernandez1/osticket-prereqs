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
</p>
<p> Once everything has been created I'll use Remote Desktop to connect to my vm . <img width="1168" height="715" alt="Screenshot 2026-01-29 at 2 25 49 PM" src="https://github.com/user-attachments/assets/5b1b91dd-8c7f-45cf-9504-40b2e955e577" />


</p>
<br />  Now we will download, install, and unzipping osticket. [osTicket-Installation-Files.zip ](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)
<img width="717" height="249" alt="Screenshot 2026-01-29 at 3 57 08 PM" src="https://github.com/user-attachments/assets/c1672918-45cd-4443-b8fa-a71d404ccd76" />
<img width="618" height="457" alt="Screenshot 2026-01-29 at 3 57 49 PM" src="https://github.com/user-attachments/assets/d4c06eec-85b9-4435-a468-9606dc68c9d1" />
<img width="798" height="593" alt="Screenshot 2026-01-29 at 4 15 50 PM" src="https://github.com/user-attachments/assets/6364f533-bfb5-40de-a61d-015f41d60610" />




<p> 
</p>
<p>
 Now I will install and enable IIS (Internet Information Servies) by going to Control Panel> Programs> Turn Windows Features On or Off> Internet Information Services and enable it then World Wide Web Services> Application Development Features and enable CGI:

  


</p>  <img width="785" height="679" alt="Screenshot 2026-01-29 at 4 25 09 PM" src="https://github.com/user-attachments/assets/460a306e-3c89-4cb7-ba3d-50f6eeb7e22f" />
<img width="909" height="413" alt="Screenshot 2026-01-29 at 4 27 27 PM" src="https://github.com/user-attachments/assets/dbd6af95-c634-4628-bdbd-92cf9abb876e" /><img width="1209" height="641" alt="Screenshot 2026-02-10 at 11 49 07 AM" src="https://github.com/user-attachments/assets/5e7f14c5-8a4c-4981-b865-25e362cb2d08" />
</p>
<img width="1130" height="587" alt="Screenshot 2026-01-29 at 5 00 40 PM" src="https://github.com/user-attachments/assets/4273528f-e65e-4423-b8e2-f2f3de2e1f03" /></></p>I can test that the web server installed correctly by typing in the loopback IP (127.0.0.1) in the internet browser and this page should load <img width="1430" height="859" alt="Screenshot 2026-02-10 at 11 55 24 AM" src="https://github.com/user-attachments/assets/b972429c-4d46-4e5d-a2c6-71d87515255b" />




</p>
<br />
</p>
<p>
</p>
Now I need to install PHP manager for IIS Setup.<img width="1433" height="860" alt="Screenshot 2026-02-10 at 12 32 36 PM" src="https://github.com/user-attachments/assets/7de415d0-b84d-4ed6-92c9-35d4ce1b9494" /></p>install IIS URL Rewrite Module:</p><img width="1426" height="860" alt="Screenshot 2026-02-10 at 12 33 09 PM" src="https://github.com/user-attachments/assets/b14b4081-1689-4359-b08f-7105060dced8" />

</p>Once those have installed I will create a PHP directory on the C drive
<img width="1438" height="900" alt="Screenshot 2026-02-10 at 12 56 41 PM" src="https://github.com/user-attachments/assets/4e731297-5b0a-4313-ae13-463f0e99d77a" />


</p>
<p>

</p>

<p>
</p>
<p>
</P>
Now I'll download PHP and extract the zip file in the PHP directory I just made</P><img width="1434" height="867" alt="Screenshot 2026-02-10 at 1 06 20 PM" src="https://github.com/user-attachments/assets/e98f81c3-4ac9-4bbe-b58f-273074c9c60a" />


>
</p>
<br />
<p>
</p>
</p>
Download Microsoft Visual C++.<img width="1431" height="869" alt="Screenshot 2026-02-10 at 1 08 57 PM" src="https://github.com/user-attachments/assets/2159e76e-e155-4a5e-971a-d1cd5e22cf6c" />


<br />
</p>
</p>
<p> Download MYSQL:
</p><img width="1423" height="858" alt="Screenshot 2026-02-10 at 1 14 36 PM" src="https://github.com/user-attachments/assets/b261ffcd-f682-47e7-a032-068e72f217b7" /><p></p>Next, I have to setup the login credentials <img width="1430" height="871" alt="Screenshot 2026-02-10 at 1 16 55 PM" src="https://github.com/user-attachments/assets/57c32ece-1a0a-4823-92f2-1ec8c482fe9d" />
<p>
<p>
<p>

Open IIS as an admin:<p><img width="1431" height="856" alt="Screenshot 2026-02-10 at 1 50 29 PM" src="https://github.com/user-attachments/assets/b27f18b8-510a-4da0-96c9-3e3374d03030" />

<br />
<p>
</p>
<p>
</p>
Next go to PHP Manager> Register new PHP version and then select the file shown:<img width="1429" height="899" alt="Screenshot 2026-02-10 at 1 56 46 PM" src="https://github.com/user-attachments/assets/ccedb2b4-e5da-4b77-b4a1-52cc588269e1" />


<br />
<p>
</p>
<p> 
</p>
Go back to osticketVM Home and hit Restart under Manage Server on the right side:<img width="1438" height="896" alt="Screenshot 2026-02-10 at 2 02 20 PM" src="https://github.com/user-attachments/assets/ee31ff68-7ee4-4027-b000-e5fdc7ade041" />

<br />
<p>
<p>
 <p>
<br />
<p>
 Next I'll download osTicket and copy the upload file to the wwwroot file in the inetpub directory:<img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 12 26 PM" src="https://github.com/user-attachments/assets/8f2c2a7d-3702-46e5-bdbf-8378da0518ca" />

<br />
<p>Rename upload file to osTicket:
<img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 15 16 PM" src="https://github.com/user-attachments/assets/2865bc48-3712-4e55-b445-d554713c6656" />

<br />Reload IIS and restart the server as I did before, then click Browse *80 (http) on the right side:<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 32 08 PM" src="https://github.com/user-attachments/assets/390b00d0-c550-4897-a0d4-b8dc8d9ede97" />


<br />
<p>This page should open.
<p><img width="1432" height="863" alt="Screenshot 2026-02-10 at 2 38 40 PM" src="https://github.com/user-attachments/assets/99c744d0-f937-4967-8c1a-32b3753e9bc8" />


  Notice some extensions are not enabled. I'll enable a few of those in IIS. Go to Sites> Default Web Site> osTicket Click PHP Manager> Enable or disable an extension. Enable php_imap.dll, php_intl.dll, and php_opcache.dll:
<br />
<p>
<img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 42 50 PM" src="https://github.com/user-attachments/assets/28fe6c98-d6ae-4b13-a7a7-dd35d1310f02" />

<p>
<p>
<p>Note the changes.
<img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 45 57 PM" src="https://github.com/user-attachments/assets/192af7b3-ea97-4213-b81d-c9723a757775" />

  
<br />Next browse in file explorer to C drive> osTicket> include> ost-sampleconfig.php and remove the "sample" from the name:
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 52 33 PM" src="https://github.com/user-attachments/assets/e34b4eb2-ef99-4d59-aebe-121e21a5a21a" />

  Right-click on ost-config.php> Properties> Security> Advanced> Disable Inheritance> Remove all inherited permissions from this object:
<br />
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 56 04 PM" src="https://github.com/user-attachments/assets/52d337c1-b65f-4506-a0c2-39845ffb938a" />

 Click on the add button to add permissions to the file> Select a principle> type "everyone"> Check> OK> check all permissions> OK> apply> OK:
<p>
<img width="1440" height="900" alt="Screenshot 2026-02-10 at 2 58 53 PM" src="https://github.com/user-attachments/assets/5baa86a9-a9fc-47ad-b87b-86b1637e0079" />

  Hit continue on the osTicket web page in the browser and fill out the set up page:
<br />
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 3 03 59 PM" src="https://github.com/user-attachments/assets/fb41cfc5-cdd3-45c0-b768-1c6bdd0a80f8" />

  Before database set up we'll have to connect the database using HeidiSQL. Install HeidiSQL from setup links:
<br />
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 3 06 35 PM" src="https://github.com/user-attachments/assets/c6f81609-745d-40bb-842a-bb9e6880fd08" />


  In HeidiSQL click New> Username = root> Password = mySQL password from mySQL setup> Open:
<br />
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 3 11 37 PM" src="https://github.com/user-attachments/assets/559a6ca5-9136-4a27-842c-1d2847b409d0" />


  In HeidiSQL right click Unnamed> Create> New Database> Name it osTicket> OK. Then continue to fill out the database portion of osTicket setup. Click Install Now when done:
<br />
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 3 15 04 PM" src="https://github.com/user-attachments/assets/02103965-2287-4550-9b81-3a3ca5c03733" />


  Last steps, for clean up go to C drive> inetpub> wwwroot> osTicket and look for the setup file and delete it. Then go to C drive> inetpub> wwwroot> osTicket> include right click on ost-config.php> Properties> Security> Advanced> Select Everyone and click edit> only leave Read & Execute and Read checked, then apply settings:
<br />
<p>
<p><img width="1440" height="900" alt="Screenshot 2026-02-10 at 3 22 18 PM" src="https://github.com/user-attachments/assets/defefb8f-5b4c-4c2e-828a-789b70feb51c" />

</p>
<br />
</p>osTicket is now installed and ready for use! In the next project I will walk you through how to configure agents, their permissions and access, users, and more!

</p>
<p>

