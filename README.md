<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This Guide Will Help You Install a Ticketing System Called osTicket.<br/>


<h2> Files You Need to Download</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2> Software & Technologies  Used</h2>

- Windows 10 (Build 19044)
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)
- Internet Information Services (IIS)

  <h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />
<p>
<h3 align="center">To start, we'll establish a Resource Group within the Azure environment. Locate 'Resource Groups' in the Azure portal and click 'Create' to initiate the process.</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/vBjsNHk.png" height="75%" width="100%" />
</p>
<p>
<h3 align="center">Create a Windows 10 Virtual Machine (VM) in Azure:

CPU: 2-4 Virtual CPUs
Username & Password: Choose any you like. You'll use these to connect remotely.
Virtual Network: Let Azure create a new one.</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/emrcmPK.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Connect to your Azure VM That Was Just Created:

Open Remote Desktop Connection: Find and open this app on your computer.
Connect: Enter the connection details for your Azure VM. </h3>
<br />
<p>
	<img src="https://i.imgur.com/Y6WYmJB.png" height="75%" width="100%"/>
	

</p>
<br />
<br />
<h3 align="center"> Enable/Install IIS in Windows:

Search: Type "Control Panel" in the search bar.
Programs: Open "Programs" and then "Turn Windows features on or off."
IIS: Scroll down and check "Internet Information Services (IIS)."
Install: Click "OK" to install IIS.</h3>
<br />
<p>
	<img src="https://i.imgur.com/iB0DDRd.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Enable CGI in IIS:

Expand: In the Windows Features window, expand "Internet Information Services" and then "World Wide Web Services."
Application Development: Expand "Application Development" and check the "CGI" box.
OK: Click "OK" to install CGI.</h3>
<br />
<p>
  <img src="https://i.imgur.com/T7djEHb.png" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Install PHP Manager</h3>
<br />
<p>
<h3 align="center">Download and Install PHP Manager:

Download: Download the PHP Manager file.
Agree: Accept the terms and conditions.
Installation Complete: PHP Manager is now installed on your system.</h3>
<p>
  <img src="https://i.imgur.com/nEsGoIV.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Now Install The Rewrite Module</h3>
<br />
<p>
<h3 align="center">Download: Download the Rewrite Module file.
Install: Follow the on-screen instructions. Accept the terms and conditions.</h3>
<p>
  <img src="https://i.imgur.com/Zguwmm4.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> 1. Create a folder for PHP:

Open File Explorer and type C:\ in the search bar.
Right-click anywhere in the search results and choose "New" > "Folder."
Name the new folder "PHP".
2. Download and extract the PHP files:

Visit the download page (link removed) and download the file named php-7.3.8-nts-Win32-VC15-x86.zip (or a similar filename depending on the version you choose).
After downloading, right-click the zip file and select "Extract All...".
In the extraction window, choose the "PHP" folder you created earlier and click "Extract".
</h3>
<p>
  <img src="https://i.imgur.com/2Ugthb9.png"75%" width="100%"/>
</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD/MS Visual C++</h3>
<br/>
<h3 align="center"> Download and Install VC_Redist:

Download: Download the VC_Redist package.
Install: Run the installer.
Agree: Accept the terms and conditions.
Complete: Finish the installation process.
</h3>
<p>
  <img src="https://i.imgur.com/8pPRYch.png"75%" width="100%"/>
</p>
<br/>
<h3 align="center"> Install MySQL:

Download: Download the MySQL installer.
Install: Follow the on-screen instructions.
Agree: Accept the terms and agreements.
Set Password: Create a strong username and password for your database. This will be used to store your osTicket ticket information. 
</h3>
<p>
  <img src="https://i.imgur.com/84IOQHR.png"75%" width="100%"/>
<br/>
  <img src="https://i.imgur.com/zdhWXNx.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Download: Download the osTicket v1.15.8 archive from within lab files.
Unzip: Extract the downloaded archive. </h3>
<br />
<p>
  Download osTicket (download from within lab files).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot: 
</p>
	<img src="https://i.imgur.com/aVRYv6h.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/fWZHPE5.png" height="75%" width="100%" />
<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/u66e77j.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/JDgAq3t.png" height="75%" width="100%" />
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/3y16Qn9.png" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites then click Default then osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/euNnssd.png" height="75%" width="100%" />
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://i.imgur.com/a/BUT43Ra" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/BUT43Ra.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/6evRpfX.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/gOD1RrV.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/ewd2C07.png" height="75%" width="100%" />
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/D60nsvq.png" height="75%" width="100%" />
</p>
<p>
	<img src="https://i.imgur.com/n1A5m6L.png" height="75%" width="100%" />
</p>
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
<p>
	<img src="https://i.imgur.com/M6iELxF.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/ST28XVX.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/9SP2m3K.png" height="75%" width="100%" />
</p>
<p>
	Create a new session, root/Password1.
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/eAS2l8p.png" height="75%" width="100%" "/>
	<img src="https://i.imgur.com/2DVcU3A.png" height="75%" width="100%" "/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/YEdZ9FG.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/RC9RJkK.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/w95r2sg.png" height="75%" width="100%" />
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://i.imgur.com/eg0ZPG3.png" height="75%" width="100%" />
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/n6k46XL.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/9Wa06DO.jpg" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>

<p>
<img src="https://i.imgur.com/7tPDc14.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

