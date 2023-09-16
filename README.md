
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

- Enable Internet Information Services (IIS)
- Install web platform installer
- Install C++ redistributable
- Install MySQL and set up username & password
- Install OS Ticket & configure permissions

<h2>Installation Steps</h2> <br>
<p>
- Install / Enable IIS in Windows with CGI and Common HTTP Features.<br> 
- This web server allows the virtual machine to serve up websites. <br>
- Go to 127.0.0.1 to confirm the web server is working.
</p>
<p>
<img width="359" alt="Screenshot 2023-07-10 at 3 55 41 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/b0fd4f35-fde8-4b9a-96b8-b84202e06bf0"><br>
<img width="329" alt="Screenshot 2023-09-16 at 1 53 51 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/34691375-2e98-4bba-9450-811603e3542d"><br>
<img width="330" alt="Screenshot 2023-09-16 at 1 55 11 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/92f9b8e9-b725-4bee-b8da-9b8ee4198507">
<img width="705" alt="Screenshot 2023-09-16 at 2 00 56 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/f9532f92-9fca-4816-9ecd-c8c685f8137d">
</p>
<p>
- Download PHP Manager for IIS.
</p>
<p>
<img width="381" alt="Screenshot 2023-09-16 at 2 08 30 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/94158d63-08bf-4947-9a14-8bcd64b8f7b4">
</p>
- Install Rewrite modules for IIS. It's a special configuration file for OS Ticket that allows it to work.
</p>
<p>
</p><img width="386" alt="Screenshot 2023-09-16 at 2 10 42 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/ef84209e-16e0-4b6a-83fc-922534e554f9">
<p>
<p>
- Create new PHP directory on C drive.
</p>
<p>
<img width="268" alt="Screenshot 2023-09-16 at 2 12 47 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/e5f714d7-1396-43e4-bbb4-465788c7041f">
</p>
<p>
- Install PHP and put it into PHP file previously created. <br>
</p>
<p>
<img width="323" alt="Screenshot 2023-09-16 at 2 22 28 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/8152028c-fe67-4cc6-8435-0603ea5c468a">
</p>
<p>
- Download C++ Redistributable, PHP may require this.
</p>
<p>
  <img width="327" alt="Screenshot 2023-09-16 at 2 24 30 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/e38bf609-e124-4194-ba41-929958fe1146">
</p>
<p>
- Install MySQL Server <br>
- Launch the configuration wizard and ensure standard configuration. <br>
- You will need to use your MySQL credentials.<br>
- OS Ticket will need a database to store all the users, tickets we create, and all other data.
</p> <br>
<p>
<img width="285" alt="Screenshot 2023-09-16 at 2 27 56 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/a62f7282-248b-4a73-9ed8-5fdb54350dd7"><br>
  <img width="376" alt="Screenshot 2023-09-16 at 2 29 00 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/9414d71c-d366-4614-a7c7-5d4fea01f523"> <br>
<img width="382" alt="Screenshot 2023-09-16 at 2 31 11 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/f552af00-9ac1-40de-a6e9-3b140a105d8a"> <br>
<img width="384" alt="Screenshot 2023-09-16 at 2 33 56 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/93dc41c0-7311-40ef-9483-3642ab8e1959">
</p>
<p>
- Open IIS, right-click & run as an admin. <br>
- Register PHP from within IIS via FastCGI (CGI enabled earlier). <br>
- Anytime you make changes to IIS, restart the web server. <br>
<p>
<img width="592" alt="Screenshot 2023-09-16 at 2 36 40 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/185f2bf9-33a8-4f7f-ac65-594c505a8de8"> <br>
<img width="683" alt="Screenshot 2023-09-16 at 2 37 54 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/5fa98d65-f30f-47da-be70-1d42bfe7aabb"><br><img width="488" alt="Screenshot 2023-09-16 at 2 39 05 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/ada17d9c-4756-425d-8da7-81c1324af08e"> <br>
<img width="915" alt="Screenshot 2023-09-16 at 2 39 55 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/98d7c5ce-4589-4288-8995-f93c0e4a670f">
</p>
</p>
<p>
- Install OS Ticket to the C:\inetpub\wwroot folder which is web servers main folder.<br>
- Rename zipped upload folder to "osTicket".<br>
- Reload, stop, start IIS web server.<br>
- Go to "sites" then "default" then "osTicket, then "Browse*:80" - you should see osTicket Installer page.<br>
<p> <br>
  <img width="331" alt="Scree![Uploading Screenshot 2023-09-16 at 2.45.44 PM.png…]()
nshot 2023-09-16 at 2 44 24 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/47f20078-b1b3-4554-81c1-1a6d33c8aace"> <br>
<img width="317" alt="Screenshot 2023-09-16 at 2 46 00 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/d87f11e7-6eac-4a6f-95c7-29e98ada9ccd"> <br>
<img width="764" alt="Screenshot 2023-09-16 at 2 48 43 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/95caff33-afe9-4179-8246-10e44c7ea0bd"> <br><img width="728" alt="Screenshot 2023-09-16 at 2 50 25 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/87d8b8b9-17d9-44e2-8046-0c10f7050290"> <br>
</p>
<p>
- Enable IMap extension (email fetching), intl.dill extension (improved localization), and opache.dill (faster performance), then refresh the osTicket site in the browser. You should now see green check marks under "Recommended".<br>
- Rename ost-sampleconfig.php to ost-config.php <br>
- Assign permissions in ost-config.php to allow anyone to access this file for the purpose of this lab.<br>
- "Disable inheritance" <br>
- Enter "everyone" and allow full control.<br> 
</p>
<p>
<img width="573" alt="Screenshot 2023-09-16 at 3 02 13 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/a1b7013a-07f0-409b-b93c-8b9c6b86d588"> <br>
<img width="714" alt="Screenshot 2023-09-16 at 3 02 56 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/b918acbe-3eca-45bf-aed2-d6b6856c5f21"> <br>
<img width="629" alt="Screenshot 2023-09-16 at 3 03 41 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/0f505c24-23df-48a8-8d64-c37753d0e0f1"> <br>
<img width="461" alt="Screenshot 2023-09-16 at 3 07 51 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/1337c167-f5b3-450d-81b1-f879bd17bdbe"><br>
<img width="338" alt="Screenshot 2023-09-16 at 3 08 02 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/7d84cbb5-f79a-4bb5-b5f3-97c5b630c758"> <br>
<img width="569" alt="Screenshot 2023-09-16 at 3 10 19 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/17e84fd5-ae34-40bc-b3cd-5d6c720af5b3"><br>
<img width="335" alt="Screenshot 2023-09-16 at 3 29 09 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/46e90877-e2f1-4f75-ae44-a62c86302957"> <br>
<img width="434" alt="Screenshot 2023-09-16 at 3 29 34 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/9c2dd0d6-efb8-4997-a788-db05968d93a1"> <br>
<img width="395" alt="Screenshot 2023-09-16 at 3 30 07 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/5b212d50-2619-47c8-aab0-3ec4b8406cd9"> <br>
  <img width="580" alt="Screenshot 2023-09-16 at 3 41 51 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/b4bf4bc5-e888-4abb-a371-6375b31def8a"> <br>
<br><img width="278" alt="Screenshot 2023-09-16 at 3 42 20 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/a65f708e-05e2-4e08-bca6-27735f073d1b"> <br>
</p> <br>
- Click "Continue"  to set up osTicket in the browser.<br>
- Name your Help Desk and create a default email that will receive emails from customers (write this info down for later use).<br>
- Create Admin User for your primary administrator account (write this info down for later use). <br>
- Install HeidiSQL - a database client that allows us to connect to the MySQL database. <br>
- Create new connection to the database called (need root credentials created earlier).<br>
- Connect HeidiSQL to MySQL by creating a "new session" in HeidiSQL called "osTicket" and putting "osTicket in the MySQL database settings.<br>
- Perform "clean up" on the congratulations screen.<br>
- Make sure your login works so that you can create tickets/respond to tickets.
</p>
<p>
  <img width="626" alt="Screenshot 2023-09-16 at 3 43 32 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/f9369ad6-1874-434c-85fd-62a3265ce5e2"> <br>
<img width="327" alt="Screenshot 2023-09-16 at 3 48 22 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/406a3803-2697-42ef-af1c-d4a2ac40b8c8"> <br>
<img width="520" alt="Screenshot 2023-09-16 at 3 49 17 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/4d16812a-ca02-4d2e-8946-65a7cdeffa24"><br>
<img width="714" alt="Screenshot 2023-09-16 at 3 50 52 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/ab600f33-ad03-48b2-8e96-821236e0b355"><br>
<img width="378" alt="Screenshot 2023-09-16 at 3 51 31 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/79ce129d-8ff5-43e9-a1dc-15392c1b1514"> <br>
<img width="503" alt="Screenshot 2023-09-16 at 3 55 03 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/68d4cd95-c235-4f62-a962-d801876fa7eb"> <br>
<img width="407" alt="Screenshot 2023-09-16 at 3 55 56 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/4b20ad6b-1951-48db-bf7f-637b1b742a11"><br>
<img width="626" alt="Screenshot 2023-09-16 at 3 56 32 PM" src="https://github.com/MariahTali/osticket-prereqs/assets/76408932/a3ffa308-7a39-46d1-bff7-ae69ab2280d7">
</p>

  
</p> <br>
