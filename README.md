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
<IMG src="https://i.imgur.com/LKMJB0c.png"
</p>
<IMG src="https://i.imgur.com/obpObnP.png
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
