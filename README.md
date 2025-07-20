
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />





<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)



<h2>Installation Steps</h2>
I will start by creating a virtual machine in Microsoft Azure and naming the resource group (osTicket) and naming the virtual machine (os-Ticket-vm)
I picked  image size(windows 10pro,version 22H2-x64 Gen2) and 8GB memory size.

<p>

  
<p>
 
</p>
<p>
Next step is to log into the VM with Remote Desktop Protocol (RDP) using the public IP address.
Within the VM (osTicket), download  https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD (osTicket-installation file).
unzip the file onto the Remote Deskstop.
Please note, I will use the file in this folder to install osTicket and some of the dependencies.
<br />
<img width="1831" height="986" alt="image" src="https://github.com/user-attachments/assets/bf27f7bd-19df-4208-aa13-cf12afbae287" />

</p>
<p>
Next step is to install or enable IIS (Internet Information Services), which serves as a web server in
Windows with CGI. To locate it, type “Control Panel” in the search bar and click on Programs → Turn
Windows features on → IIS → expand it to install CGI → (expand IIS > World Wide Web Services > 
Application Development Features > CGI)



<p>
<img width="1874" height="1031" alt="image" src="https://github.com/user-attachments/assets/db2a9058-c1b5-4f8f-b592-1a6c04f00780" />

</p>
<p>

From the osTicket folder, we are going to install the web server (PHP and Rewrite Module) in order for
our osTicket to work. Next is to create a directory C:\PHP from the osTicket installation folder and unzip
it into the PHP folder. Next is to install Vc_redist.x86 and install mysql_5.5.62-win32. We are going to
typically set up our SQL server, and the reason is because the SQL server database is where all our data
will be at (user's information and client's information).

</p>
<br />

<p>
<img width="1863" height="954" alt="image" src="https://github.com/user-attachments/assets/66f9d5df-611f-4daf-83d0-06539b71469e" />

<p>
<img width="1861" height="981" alt="image" src="https://github.com/user-attachments/assets/e502ecd1-66d3-47df-982e-5cb87a13f23a" />

</p>
<br />



</p>
<br />
<img width="1005" height="543" alt="image" src="https://github.com/user-attachments/assets/c7185f79-af1a-4117-bf21-a22c510326db" />
 

</p>
Next is  to open internet information services(IIS) and run as admin. Register PHP from within IIS (using PHP Manager) and reload it by turning it off and on). 
Next  install osTicket VI. 15.8 (extract it first and it creates new unziped folder)
Copy the upload folder into wwwroot(The root of the webserver) and rename the upload folder to osTicket. Reload IIS again by turning the server off and on.
<img width="1915" height="1022" alt="image" src="https://github.com/user-attachments/assets/32574043-9923-43c6-9350-18bdfe36c53f" />

</p>
<br />

Next is to attempt to load osTicket site in the IIS and to do that go to sites > Default > osTicket and click on Browse 80(http) and it should work.
</p>
<img width="1902" height="958" alt="image" src="https://github.com/user-attachments/assets/dab6df8a-a7cc-4ce5-b602-8cf870b10280" />


Next is to enable some features that are not enabled. To do that, go to IIS and make some configurations.
Go to site > Default site > osTicket and double click PHP Manager and enable the features you want to. 
I enabled PHP IMAP Extension and PHP Intl Extension.
</p>
<br />
<img width="1886" height="966" alt="image" src="https://github.com/user-attachments/assets/03f731a7-d64f-4483-ba03-2c241b480610" />

</p>
I'm going to rename a certain file that osTicket uses to make configuration. So basically, inside the webserver "root" in the osTicket folder,
There's this file called ost > sample config.PHP. We are going to rename it to ost > config PHP
Then assign permission ost > config php
Disable inheritance > Remove all
New permission > everyone- All
Continue setting up osTicket in the brower(click continue
Name Helpdesk
Default email(receives email from customers)
</p>
<br />
<img width="1336" height="930" alt="image" src="https://github.com/user-attachments/assets/15e4af91-5048-4495-8469-4ace1219fd9d" />

</p>
<img width="1771" height="1012" alt="image" src="https://github.com/user-attachments/assets/bfbd084b-d23e-441c-b254-fc25f319508d" />

</p>
<br />
Next is to create a new SQL database and call it 'osTicket' from the one we already have in our installation file folder.
To do that we need to go back to the installation file folder and install Herdi SQL Application and create a new database our osTicket will use.
<img width="1919" height="1014" alt="image" src="https://github.com/user-attachments/assets/ecb5664e-9f28-433e-ae7c-6cd054324705" />

</p>
<br />
</p>
<img width="1920" height="1004" alt="image" src="https://github.com/user-attachments/assets/44a52a43-ffb5-4981-832e-afa032c9270e" />

</p>
Next is  continue setting up the osTicket in the browser and then install.

</p>
<img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/640eb025-fc5d-462c-8d9e-c52e5d8154a8" />

</p>
<br />




