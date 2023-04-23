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

<h2>List of Prerequisites</h2>

- Create a VM in Microsoft Azure
- Install OsTicket prerequisites
- Install OsTicket v1.15.8
- Install HeidiSQL

<h2>Installation Steps</h2>



 Create Virtual Machine in Azure
 
<p>
<img src="https://i.imgur.com/azannJE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Windows 10 Virtual Machine or VM with 2-4 Virtual CPUs allow VM to create new Vnet:
</p>
<br />

<p>
<img src="https://i.imgur.com/oTizlQz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Connect to your Virtual Machine with Remote Desktop using the public ip address of your virtual machine:
</p>
<br />

<p>
<img src="https://i.imgur.com/mPO7Xyv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install/ Enabel IIS in Windows:
</p>
<br />
<p>
<img src="https://i.imgur.com/3JbkLSP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install required Programs to run Osticket PHP 7.3.8 will have to be unzipped in the directory C:\PHP:
</p>
<br />

<p>
<img src="https://i.imgur.com/ureGH7f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install MySQL:
</p>
<br />

<p>
<img src="https://i.imgur.com/bGzBWjQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Open IIS as an Administrator and Register PHP:
</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/8xMFrke.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then you would register PHP in IIS by going to PHP manager inisde of IIS:
</p>
<br />
<img src="https://i.imgur.com/r8tvKWb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>

Install Osticket From Files:
</p>
<br />

<p>
<img src="https://i.imgur.com/XvV5L4F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then from within the osticket file we drag the upload folder into the wwwroot folder and make sure to rename upload folder to "osTicket". 
</p>
<br />

<p>

Next we open osticket from witin IIS to do so you would 

Go to sites -> Default -> osTicket

and then on the right, click “Browse *:80” and it should look like so:
</p>
<br />

<p>
<img src="https://i.imgur.com/Iq4klXh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Note that some extensions are disabled so we have to enable them inside of IIS
<p>
Enable: php_imap.dll

Enable: php_intl.dll

Enable: php_opcache.dll

</p>

<img src="https://i.imgur.com/gjnRPJJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p>

Refresh osticket and Observe changes:

Rename: ost-config.php

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Then assign permissions: 

Disable inheritance -> Remove All

New Permissions -> Everyone -> All


</p>
<br />

<p>
<img src="https://i.imgur.com/UsB0jIW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/zuT4LAM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/pDgKZoj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue to set up Osticket in the browser (click continue)

Name Helpdesk.

Deafault email ( gets emails from customers):
</p>
<br />

<p>
<img src="https://i.imgur.com/fujSm1m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HedidiSQL
</p>
<br />

<p>
<img src="https://i.imgur.com/qJx0pQy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Connect to session: 
</p>
<br />

<p>
<img src="https://i.imgur.com/2qU4pLy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Database
</p>
<br />

<p>
<img src="https://i.imgur.com/fuL3q4t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue to set up osTicket in the Browser

MySQL Database: osTIcket

MySQL Username: root

MySQL Password: Password1:
</p>
<br />

<p>
<img src="https://i.imgur.com/HPsJIAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click install now and hopefully there are no errors!
</p>
<br />

<p>
<img src="https://i.imgur.com/DPQQjXl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Clean up: 

Delete: C:\inetpub\wwwroot\osTicket\setup

</p>
<br />

<p>
<img src="https://i.imgur.com/dqqKv1I.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/NSPQcRM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Log into osTicket Admin Panel (http://localhost/osTicket/scp/login.php)


</p>
<br />

<p>
<img src="https://i.imgur.com/TLzffXD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
And this completes my tutorial of the installaion of osTicket i hope it helped you.

Now you can practice having your own mock help desk to prepare you for a positon in help desk

or it support role.
</p>
<br />
