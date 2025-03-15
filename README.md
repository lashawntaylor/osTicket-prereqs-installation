<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. You'll use this system in order to work service tickets for customer support requests.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=LOzmM5ZjKi0)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (For Virtual Machine)
- Windows Server (Remote Desktop)
- PHP 7.3.8 with extensions like imap, intl, and opcache
- MYSQL 5.5.62
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10
- Windows Server</b> 

<h2>List of Prerequisites</h2>

- Installed MySQL
- Enabled IIS
- Installed  VC_redist.x86.exe
- Installed osTicket installation folders and unzipped them into the Windows C drive
- Enabled extensions imap, intl, and opcache
- Installed HeidiSQL

<h2>Installation Steps</h2>


![image](https://github.com/user-attachments/assets/df78f6a3-4410-4b21-af6a-d81fdde7da5b)

You’ll create a resource group, then name the virtual machine. Then you’ll review and create the virtual machine.
</p>
<br />


<img width="1440" alt="image" src="https://github.com/user-attachments/assets/f91c17bd-ec3e-43e1-bb1f-d7c17848a323" />


Next you’ll get logged into the virtual machine. You can access it by typing ‘virtual machine’ in the search bar.
You’ll then copy the Public IP Address from that virtual machine you created. 
</p>
<br />


![image](https://github.com/user-attachments/assets/87964e3e-79cc-4b1d-91ab-496fcab48b10)

Then from MacBook, open up the Microsoft Windows App. (This is how you access Remote Desktop from Mac)
</p>
<br />

<img width="1440" alt="Screenshot 2025-03-11 at 12 45 00 AM" src="https://github.com/user-attachments/assets/c21a3dfa-14de-4de0-a8ce-bd1e08a091ac" />

Next you’ll hit the ‘+’ sign in the top right corner to add a PC. You’ll then paste the Public IP Address from the virtual machine you created into the PC Name box.
</p>
<br />

<img width="1440" alt="Screenshot 2025-03-11 at 12 46 41 AM" src="https://github.com/user-attachments/assets/ed451f57-3b52-4490-8517-b9aaaaf2197d" />


Name the PC then log into it with your credentials to access the desktop.
</p>
<br />

![image](https://github.com/user-attachments/assets/f6dd60ae-fd29-4f95-84bb-8f4900ba2e5e)



(Here's how it will look when you're logging in.)
</p>
<br />

![image](https://github.com/user-attachments/assets/690578fd-4071-4101-9b5a-7287ae33494b)


Once you’re in you’ll open up the Microsoft edge browser, and you’ll download and install the osTicket Installation Files and unzip it onto your desktop.
</p>
<br />

![image](https://github.com/user-attachments/assets/6708f392-3b6b-4930-a6c8-8c9ac64c34cb)


Next step you’ll install and enable IIS in Windows as well as CGI. You’ll click the start menu and type in control to access the ‘Control Panel’.
</p>
<br />

![image](https://github.com/user-attachments/assets/e5a042e2-6a40-4cbd-b83b-842b3fa829b9)


Click on Programs. From that window, on the left you’ll click on ‘Turn Windows features on or off’
</p>
<br />

![image](https://github.com/user-attachments/assets/9910d061-b889-4416-824e-85db547c3abd)


You’ll scroll down and check the box next to ‘Internet Information Services’. Then you’ll click on it.
</p>
<br />

![image](https://github.com/user-attachments/assets/a68853df-1c59-43c7-b369-8f23cc92427c)


Then click World Wide Web services, click Application Development Features, locate CGI and check the box next to it.

Click Ok and it’ll start installation.
</p>
<br />

![image](https://github.com/user-attachments/assets/323cb5fd-197b-46a9-bb3b-5ba4d7a064f3)


Next from the osTicket Files you’ll install PHP Manager.

So you’ll click on the osTicket folder and then it’ll pull up PHPManager, click on it and install it
</p>
<br />


![image](https://github.com/user-attachments/assets/e9f7c41c-77a4-43d7-ba83-ed7d22dcafa4)


Then from the same folder you’ll install Rewrite Module. Click on it and install it.
</p>
<br />

![image](https://github.com/user-attachments/assets/a01310c3-94b5-41f0-886f-83d497d63cfc)


Next you’ll create a directory C:\PHP
You’ll open up File Explorer, from there you’ll click This PC to pull up Windows C.
</p>
<br />

![image](https://github.com/user-attachments/assets/f0160021-b1b1-4d13-847e-839c31aa302d)


Click New Folder to create a New Folder in there, name it PHP

You’ll then unzip the PHP file into the PHP folder. You’ll extract the PHP file into the folder.

</p>
<br />

![image](https://github.com/user-attachments/assets/b49b01ce-f9ec-4f5d-9e5b-8559cdbcb463)


Next we’re installing the VC redist file.
</p>
<br />

![image](https://github.com/user-attachments/assets/df94860f-78a5-45d6-9e76-61763535c1e0)


After that we’re installing the MySQL file.
</p>
<br />

![image](https://github.com/user-attachments/assets/a1d18f80-cda0-4968-8211-58dbf8d7ffd8)



Next you’ll open IIS as an admin
You’ll click start and then type ‘IIS’ in the search, when it pulls up you’ll select ‘Run as administrator’.
</p>
<br />

![image](https://github.com/user-attachments/assets/0f50b446-44a1-4e12-a198-5d67b49f2b93)



The osTicket home you created will pop up.
</p>
<br />

![image](https://github.com/user-attachments/assets/c1524a9c-5577-4dd2-b25c-d7ed1eaa2c54)



Next we’ll register the PHP from within the IIS
So On the menu you’ll click ‘PHP Manager’ then click ‘Register new PHP version’.
</p>
<br />


![image](https://github.com/user-attachments/assets/bfc8411f-044d-4d55-9113-38c9caa21358)



On the next screen you’ll click the 3 dots and browse for the file you added to the Windows C drive in the PHP folder.

You’ll click php cgi and then press ok.
</p>
<br />


![image](https://github.com/user-attachments/assets/bed1da21-af00-4107-acd6-ac232bd7c0a2)



Next you’ll reload IIS

So you’ll go back to the osTicket home, you’ll click stop on the right side of the tab
Then click start.
</p>
<br />


![image](https://github.com/user-attachments/assets/6f58d62c-ca60-4076-8632-860ad5bd6432)



Next we’ll install osTicket v1.15.8

You’ll then copy the upload folder into the Windows C Drive/inetpub/wwwroot and then you’ll rename ‘upload’ to ‘osTicket’

You’ll then reload IIS again. (Click osTicket server, press stop, and then start)
</p>
<br />


![image](https://github.com/user-attachments/assets/eed97718-f31d-493f-b2d5-1cebbe831218)


![image](https://github.com/user-attachments/assets/733f7ba6-86aa-4e41-a861-93bd14f027d1)


![image](https://github.com/user-attachments/assets/948af053-9a80-4983-ae18-e3141e8e67dc)


Now we’ll load the osTicket site.
You’ll expand the osTicket server, then click on Sites, then Default Web Site, then osTicket. 


![image](https://github.com/user-attachments/assets/5c187f98-2af9-47f0-8339-642e64b60a98)



And the osTicket website will pop up.
</p>
<br />


![image](https://github.com/user-attachments/assets/d71d8d11-6699-4b41-b856-739867892aca)



Now we’re going to enable some extensions.
You’ll go back to IIS, then click on Sites, then Default Web Site, then osTicket, then PHP Manager.
</p>
<br />


![image](https://github.com/user-attachments/assets/1d6c2052-e29e-49d2-99e3-71a5f3b70caa)



Then you’ll click Enable or Disable an Extension.


</p>
<br />

![image](https://github.com/user-attachments/assets/4bcc98ab-c795-4c44-b66a-d2950cd2daef)


You’ll scroll down and enable: 
php_intl.dll,
php_imap.dll,
php_opcache.dll.
</p>
<br />


![image](https://github.com/user-attachments/assets/a3404a17-2142-4a6c-a1d6-de0e62e6f3d6)



Then refresh your browser.
</p>
<br />


![image](https://github.com/user-attachments/assets/4ed0bd32-2080-492c-a0e6-e31a0e4b02c4)



Next we’ll rename ost-sampleconfig.php
Go back to file explorer, click on Windows C Drive/inetpub/wwwroot/osTicket/include then scroll down to ost-sampleconfig.php and change the name to ost-config.php.
</p>
<br />


![image](https://github.com/user-attachments/assets/6fc83b67-2b02-4b35-be3f-9d6be5c3c211)



Then we’ll assign new permissions, so click on ost-config.php, and then click on the properties button (white paper with red check mark) in the top left corner.
</p>
<br />


![image](https://github.com/user-attachments/assets/b0e765e4-eee1-42ea-b0ce-c81cff5009a7)



Click security, then advanced, then Disable Inheritance, and then ‘remove all inherited permissions from this object’.

</p>
<br />


![image](https://github.com/user-attachments/assets/00cbfdcf-bc69-47b3-90ed-2c0190a14bfd)



Then click add to put in new permissions, select a principal, and then in the box type ‘Everyone’ and click ok

Then check full control and click ok

Click apply and then ok, then ok again.
</p>
<br />


![image](https://github.com/user-attachments/assets/1db6756d-20e7-4de0-95e4-f2f13a6dd06e)



Now we’ll continue setting up osTicket in the browser, so go back to the browser and click continue

Then fill out the Basic Installation page

After you fill that out before you continue, you’ll have to install the SQL files.
</p>
<br />


![image](https://github.com/user-attachments/assets/d9939f51-32fc-40f4-b417-a65404a0c460)



So you’ll go back into file explorer, back into the osTicket installation files, and click on HeidiSQL, then install the file.
</p>
<br />


![image](https://github.com/user-attachments/assets/e480757d-a53c-45ea-8c23-06875e1e19b8)


![image](https://github.com/user-attachments/assets/5c1bb2ae-8eca-4ec0-8ed3-430a7f233d6c)



Once it opens start a new file, type in username and password and then click open.
</p>
<br />


![image](https://github.com/user-attachments/assets/1e2dc611-4898-4989-aa12-510b89a54798)



Then you’ll right click Unnamed, then Create new, then click Database and then type ‘osTicket’ in the name box.
</p>
<br />


![image](https://github.com/user-attachments/assets/0f528fd5-88fc-4105-b01b-cc4255051855)




Now you’ll go back to the browser and finish setting up the SQL portion at the bottom .
</p>
<br />


![image](https://github.com/user-attachments/assets/465f49ea-5769-4b43-af5d-2435c9df6849)




At the end click install now.
</p>
<br />



![image](https://github.com/user-attachments/assets/f5aee3cd-d597-4e50-9ec1-f0f334655824)




If you would like to check to make sure it’s running correctly you’ll take the ‘Your osTicket URL’ on the Congratulations page, copy and paste it into your browser, and login with your credentials.
</p>
<br />


![image](https://github.com/user-attachments/assets/e4be36f9-1839-4dbd-94d7-05443bcd296f)



![image](https://github.com/user-attachments/assets/cb59f933-f9cb-44d2-a6ee-90bd737442f2)


Congratulations, you’ve successfully installed osTicket!
</p>
<br />













