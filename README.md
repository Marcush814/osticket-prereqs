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
- Installation of Prerequisites For OsTicket
- Installation of OsTicket and Creating a database using HeidiSQL
- Post installation install
- Ticket Lifestyle

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/ayuKHBh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this lab i created a resource group named RG-1 and made a virtual machine inside of the resource group named VM-1. The VM is running Windows 10 with (2-4) virtual CPU's. Then i enabled CGI and IIS. Next i installed the files required to run OsTicket. Which includes (PHP manager, Rewrite module, PHP 7.3.8, VC_redist.x86.exe, and MYSQL). The files from PHP 7.3.8 have to be unzipped into a directory named C:\PHP which house the additional files needed for Ostickets install. Next i made sure IIS works buy typing in the loopback ip address in my url (127.0.0.1). Once the page appears i open IIS as an admin an register PHP. 
</p>
<br />

<p>
<img src="https://i.imgur.com/3ia9fj4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to install Osticket itself it is essentialy installed from the files downloaded in your files folder and using IIS. IIS is used to deploy, manage, or host applications. When reloaded thru IIS if you get an error message extensions have to enabled within IIS (php_imap.dll, php_intl.dll, php_opcache.dll) under the osticket folder in order for osticket in fully run. Next would be to allow permissions for users within the organization can have access to osticket. Continuing setting up osticket once its up and running and then donwload the HeidiSQL which is a database for osticket.   
</p>
<br />

<p>
<img src="https://i.imgur.com/mfb0yFK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Post installation i configured roles from within Osticket. Which includes the roles, departments and teams the employee works in. Next is to create tickets so essentially assinging customers to agents and adding users (customers) agents(workers). Next would be to configure SLA's and help topics. SLA is serivce level agreements which is a time frame the ticket is estimated to be resolved. Help topics are descriptions of the tickets nature (buisness critical outage, password reset, equipment request). 


</p>
<br />

<p>
<img src="https://i.imgur.com/mhKEMM7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ticket lifestyle would be SEV-A, SEV-B, SEV-B. SEV is the severity of the ticket with A be the most sevre. Sev-A (1 hour, 24/7) Sev-B (4 hours, 24/7) Sev-B/C (2 hours, business hours). 
