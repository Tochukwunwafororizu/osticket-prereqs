# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>
I will start by creating a vitual machine on Azure and naming the resource group (osTicket) and naming the virtual machine (os-Ticket-vm)
I picked the image size(windows 10pro,version 22H2-x64 Gen2 and 8GB memory size.

<p>
<img src="https://i.imgur.com/50Kcd7I.png"
  
<p>
<img src="https://i.imgur.com/6zxDjLY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next step is to log into the VM with Remote Desktop using the public IP address.
Within the VM (osTicket) download  https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD (osTicket-installation file).
unzip the file unto the Remote Deskstop.
Please note, I will use the file in this folder to install osTicket and some of the dependencies
<br />
<img src="https://i.imgur.com/2bpobH0.png"
</p>
<p>
Next step is to install or enable IIS(Internet information services) which serves as web server in windows with CGI.To locate it,type control panel on search bar and click on programes-
turn windows features on-IIS-expand it to install CGI-(expand IIS-world wide web services-Application development features-CGI)



<p>
<img src="https://i.imgur.com/UmaOOsZ.png"/>
</p>
<p>
From the osTicket folder we are going to install the web server (PHP and Rewrite Module) in order for our osTicket to work.
Next is to create a directory c\PHP from the osTicket installation folder and unzip it into the PHP folder.
Next is to install Vc_redist-x86 and install my sql_5.5.62-win32. We are going to typically setup our sql server and the reason is because the sql sever database is where all our data will be at(User's information, and client's information)


</p>
<br />

<p>
<img src="https://i.imgur.com/DpVaLlt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/LKMJB0c.png"
</p>
<br />



</p>
<br />
<img src="https://i.imgur.com/obpObnP.png" 

</p>
Next is  to open internet information services(IIS) and run as admin. Register PHP from within IIS(PHP manager and reload it by turning it off and on). 
Next  install osTicket VI. 15.8 (extract it first and it creates new unziped folder)
Copy the upload folder into wwwroot(The root of the webserver) and rename the upload folder to osTicket. Reload IIS again by turning the server off and on.
<img src="https://i.imgur.com/IMsq26D.png"
</p>
<br />

Next is to attempt to load osTicket site in the IIS and to do that go to sites- Default- osTicket and click on Browse 80(http) and see what happens.
</p>
<img src="https://i.imgur.com/ZP4zt6D.png"

Next is to enable some features that are not enabled and to do that, go to IIS and make some configurations.
Go to site-Default site-osTicket and double clickPHP manager and enable the features you want to. 
I enabled PHP Imap Extension and PHP Intl Extension.
</p>
<br />
<img src="https://i.imgur.com/guQRE3u.png"
</p>
I'm going to rename a certain file that osTicket uses to make configuration, so basically inside the webserver "root" in the osTicket folder.
There's this file called ost-sample config.PHP. We are going to rename it to ost-config PHP
Then assign permission ost-config php
Disable inheritance- Remove all
New permission- everyone- All
Continue setting up osTicket in the brower(click continue
Name Helpdesk
Default email(receives email from customers)
</p>
<br />
<img src="https://i.imgur.com/QHwST5x.png"
</p>
<img src="https://i.imgur.com/raBiGRn.png"
</p>
<br />
Next is to crate a new SQL database and call it 'osTicket' from the one we already have in our installation file folder.
To do that we need to go back to the installation file folder and install Herdi SQL Application and create a new database our osTicket will use.
<img src="https://i.imgur.com/Ulwqaz1.png"
</p>
<br />
</p>
<img src="https://i.imgur.com/bFIJIUM.png"
</p>
Next is  continue setting up the osTicket in the browser and then install and see what happens

</p>
<img src="https://i.imgur.com/Z3eiJL4.png"
</p>
<br />




