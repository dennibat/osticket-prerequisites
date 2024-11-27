<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" height="75%" width="100%"alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<!-- <h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) -->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machine in Azure
- Install Web Platform Installer
- Install osTicket v1.15.8
- Install HeidiSQL

<h2>Installation Steps</h2>
<h3 align="center">Create Virutal Machine in Azure</h3>
<br />
<p>
	Create a Resource Group
</p>
<p>
	<img src="https://i.imgur.com/4iw7HEy.png" height="75%" width="100%" alt="Resource Group"/>
</p>
<p>
	Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
	When creating the VM, allow it to create a new Virtual Network (Vnet):
</p>
<p>
	<img src="https://i.imgur.com/dEF1c7h.png" height="75%" width="100%" alt="Windows Virutal Machine"/>
</p>
<br />
<br />
<h3 align="center">Connect to your Virtual Machine with Remote Desktop</h3>
<br />
<p>
	<img src="https://i.imgur.com/8GSNqkm.png" height="75%" width="100%" alt="Remote Desktop"/>
</p>
<br />
<br />
<h3 align="center">Install / Enable IIS in Windows</h3>
<br />
<p>
	<img src="https://i.imgur.com/rA6RizL.png="75%" width="100%" alt="Enable IIS in Windows"/>
</p>
<br />
<br />
<p>
	<img src="https://i.imgur.com/0EDEbap.png"75%" width="100%" alt="Enable IIS in Windows"/>
</p>
<br />
<br />
<h3 align="center">Install Web Platform Installer</h3>
<br />
<p>
	<img src="https://i.imgur.com/YbK46JQ.png="75%" width="100%" alt="Enable IIS in Windows"/>
</p>
<p>
  <h3 align="center"> Install the Rewrite Module</h3>
</p>
<p>
	<img src="https://i.imgur.com/GLhLoYD.png="100%" alt="MySQL 5.5"/>
</p>
<br />
<p>
 <h3 align="center">Create the directory C:\PHP</h3>
</p>
<p>
	<h3 align="center"><img src="https://i.imgur.com/FkBrdTh.png="100%" alt="MySQL 5.5"/></h3>
  </p>
<o>
 <h3 align="center"> unzip PHP 7.3.8 into the “C:\PHP” folder</h3>
</p>
<p>
	<img src="https://i.imgur.com/C3wK4Vt.png="75%" width="100%" alt="Credentials"/>
</p>
<p>
  <h3 align="center">Install C++</h3>
</p>
<p>
	<img src="https://i.imgur.com/A6RXUwS.png" height="75%" width="100%" alt="PHP"/>
</p>
<p>
  <h3 align="center">Install MySQL 5.5.62</h3>  
</p>
<p>
  	<img src="https://i.imgur.com/wWl7bLm.png" height="75%" width="100%" alt="PHP"/>	
</p>
<p>
 <h3 align="center"> Register PHP from within IIS</h3>

</p>
<p>
  	<img src="https://i.imgur.com/jq255if.png" height="75%" width="100%" alt="PHP"/>	
	
</p>
<p>
  <h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>

</p>
<p>
	<img src="https://i.imgur.com/tmUZaGe.png" height="75%" width="100%" alt="PHP"/>
</p>
<p>
<h3 align="center">Install osTicket v1.15.8</h3>
</p>
<p>
	<img src="https://i.imgur.com/tw2cQyG.png" height="75%" width="100%" alt="PHP Manager"/>
</p>
<p>
<h3 align="center">Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”</h3>
</p>
<p>
	<img src="https://i.imgur.com/nDA31g5.png" height="75%" width="100%" alt="PHP Manager"/>
</p>
<p>
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
</p>
<p>
	<img src="https://i.imgur.com/SRej42b.png" height="75%" width="100%" alt="PHP Manager"/>
</p>
<p>
<br />
<br />
<h3 align="center">Go through folder of osTicket and click “Browse *:80” </h3>
<br />
<p>
  	<img src="https://i.imgur.com/vI7u56F.png" height="75%" width="100%" alt="PHP Manager"/>		
</p>
<p>
	 Click “Enable or disable an extension”.

Enable: php_imap.dll.

Enable: php_intl.dll.

Enable: php_opcache.dll: 
<p>

<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
</p>
	<img src="https://i.imgur.com/XP68f6n.png" height="75%" width="100%" alt="PHP Manager"/>
 <p>
	
<p>
	<h3 align="center">Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:</h3>
	
</p>
<p>
	<img src="https://i.imgur.com/pDikkgq.png" height="75%" width="100%" alt="rename to osTicket"/>
</p>
<br />
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
<br />
<p>
</p>
<p>
	<img src="https://i.imgur.com/KRuVrRf.png" height="75%" width="100%" alt="default osTicket"/>
</p>
<p>
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
	</p>
	New Permissions -> Everyone -> All
</p>
<p>
	<img src="https://i.imgur.com/CodE4iy.png" height="75%" width="100%" alt="disable inheritance"/>
</p>
<p>
	
</p>
<br />
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
</p>
<p>
	<img src="https://i.imgur.com/CnlONzy.png" height="75%" width="100%" alt="PHP Manager"/>
</p>
<p>
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/hvH8vjv.png" height="75%" width="100%" alt="download HeidiSQL"/>
</p>
</p>
<p>
	Create a new session, root/root.
</p>
<p>
	Connect to the session:
<br />
<br />
	<img src="https://i.imgur.com/sqUwUqB.png" height="75%" width="100%" alt="download HeidiSQL"/>
<br />
<br />
Create a database called “osTicket”:
<br />
<p>
	<img src="https://i.imgur.com/mU9Dg3d.png" height="75%" width="100%" alt="osTicket change"/>
</p>
<br />
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: root:
</p>
<p>
	<img src="https://i.imgur.com/eyckn1S.png" height="75%" width="100%" alt="setting up osTicket cont'd"/>
</p>
<p>
</p>

</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/Y5rdeO7.png" height="75%" width="100%" alt="installation complete"/>
</p>
</p>
<br />
<br />
<br />
<p>
	And there you have it! I hope this tutorial helped you with installing osTicket.
</p>
<p>
	And now you can practice having your own mock help desk locally to prepare you for a postion in a help desk or IT support position.
</p>
</p>
<p>
	
</p>
<p>
	
</p>
<p>
	
</p>
<br />

<p>
	

<br />


</p>
<p>
	
<p>
	

<p>
	
	


