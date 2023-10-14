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

- Create a new Resource Group Within Azure
- Create a Windows 10 Virtual Machine 






<h1>Installation Steps</h1>

- ## Create a Windows 10 Virtual Machine within Azure
  
 <img width="1128" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/51323fc8-96d6-40ed-b3f5-b83deda12197">

- ## Configure IIS (Internet Information Services)
  - Login to the VM and navigate to Start > Control Panel > Programs > Turn Windows Features On or Off

    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/38b93632-8e2a-4409-a21f-b2caae9a75c5">

  - Scroll down to "Internet Information Services" and expand the folder > Expand "Application Development Features" > Enable "CGI"
    
    <img width="344" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/1aad4ee8-347c-4b73-b941-958609f1ddf1">

  - Expand "Common HTTP Features"
  - Enable all HTTP Features
    
    <img width="346" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/c92ae779-7ec2-47ac-bf13-8aa28372bd50">

  - Click "Ok" to apply all changes
  - Open a Web Browser and navigate to "127.0.0.1"
  - You should be presented with this page:
    
    <img width="1096" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/284c29f6-0cc1-426e-956d-7a984ad8a986">
    
  - This is the web server that we will be using to run osTicket 




- ## Install PHP Manager for IIS 
  - Dowload PHP Manager and go through the Installation steps: https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=sharing
  - Download the rewrite module and go through the Installation steps (This is a backend module required by osTicket): https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=sharing

  - Create a directory for PHP on the C:\ Hard Drive

    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/161cf9df-52da-4df2-876d-68729a8c37c1">

  - Download the PHP zip file into the PHP directory: https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link
  - Exctract the contents of the downloaded PHP file into the previously created PHP directory

    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/49857146-9b00-4ae6-b6f7-c40c3015ef84">

- ### Download and Install C++ Redistributable file: https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=sharing
  
    <img width="360" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/dd409c05-a161-431a-810d-28567aa334c6">


- ## Download and Install MySQL Server
  
- mySQL Server Download: https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=sharing
  
  <img width="291" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/459aa3d6-0487-43a5-aaf3-fbe90541b3e2">

- Choose a "Typical Install"
  
  <img width="291" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/7e5d37e0-3578-4669-b096-26b1199ed031">

- Click "Finish" to open the MySQL Server Configuration settings
  
  <img width="291" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/f2f864c5-648e-4070-bee6-d1e19275aafd">

- Click on "Next"

  <img width="294" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/83ca6a21-4fb2-49e1-82ae-5b9eef6deae4">

- Choose "Standard Configuration"

  <img width="295" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/f827f033-f2e2-4b11-8f6f-a95a0a60e775">

- Choose "Next"

  <img width="294" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/1ca416ec-4808-4623-9b43-964616b891a6">

- Create a Password for the "root" user and click "Next"

  <img width="294" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/7df62cc7-610c-441d-bf31-94682e95b47f">

- Choose "Execute"

  <img width="293" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/4b4d1f75-945a-4334-b267-9ef6528660f9">

- Choose "Finish"

  <img width="250" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/f776dd38-61dc-4601-b917-ef0e38415e04">




- ## Open IIS (Internet Information Services) as an Admin & Register PHP from within IIS

  - Open and run IIS as an administrator

    <img width="587" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/ee4d2d1b-7aa5-478d-9dc1-bf967327cb51">

  - Click on "PHP Manager"

    <img width="838" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/ad6cb16a-a796-4d20-b66d-d77e2710a083">

  - Click on "Register a new PHP version"
 
    <img width="836" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/05d96872-b98b-4b3d-a41a-6e6559e0b98a">

  - Navigate to the "PHP" directory and choose "php-cgi" and click "Open"

    <img width="835" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/6acba532-b69a-45a8-87cd-10e627c66a01">

  - Navigate back to the IIS homepage and click "Restart" to restart the IIS Server

    <img width="834" alt="serverstart" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/e7f042b7-af5f-4ed5-8467-b3779aa99fbe">



- ## Download and Install osTicket

  - osTicket download: https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=sharing
 
  - Open the "osTicket" folder

    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/d96dff2d-6543-4aed-9da2-5a10cf0d51ec">

  - Drag the "upload" folder from osTicket and drop it into the "wwwroot" folder
  - The "wwwroot" folder can be accessed by navigating to C:\ Directory > inetpub > wwwroot
  - After dragging the "upload" folder into the "wwwroot" folder, rename the "upload" folder to "osTicket"

    <img width="1105" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/66af7c45-1edc-4d69-ab80-92c2432f0884">


  - Open up IIS and restart the server

    <img width="833" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/5e95bc29-f124-4c2a-85a3-6c0f05fcbaf7">

  - Within IIS, on the left panel under "Connections", navigate to "Sites" > "Default Web Site" > "osTicket"

    <img width="836" alt="iisone" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/721d588e-70f2-4048-b086-c0324950ccda">

  - Click on "Browse *:80 (http)" on the right panel under "Manage Folder" > "Browse Folder"

    <img width="834" alt="browse80" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/29e8082d-e78f-4765-b164-d7ca8cc16ead">

  - You should be presented with this screen within the internet browser

    <img width="1091" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/066d4d73-3ac1-4bfd-8824-7afbe547c9c9">

  - Navigate to IIS and open "PHP Manager" > Click on "Enable or disable an extension"

    <img width="835" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/9c4b350a-e105-4d56-865b-4684faa67471">

  - Enable the following extensions by right clicking on the extension and choosing "Enable"
    
      - php_imap.dll
      - php_intl.dll
      - php_opcache.dll
          
    <img width="835" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/dd36b072-fcb3-4c3d-8d61-6a10b2226223">

  - Navigate to IIS and refresh the server
  - You should be able to view the changes take effect by taking note of the green check marks that have appeared

    <img width="454" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/84e5359f-015d-4a72-8acd-c3e9414877f5">
 
  - Navigate to "wwwroot" > "osTicket" > "include" > "ost-sampleconfig.php"
  - Rename the "ost-sampleconfig.php" file to "ost-config.php"
 
    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/4fcc58d5-6f66-46e9-a965-7ce466a21e85">
 
  - Edit the permission of the "ost-sampleconfig.php" file by right clicking on the file > "Properties" > "Security" > "Advanced" > Click on "Disable Inheritance"
 
    <img width="929" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/b5ee5619-c1ae-4ecb-b17b-4096c16245da">
 
  - After Disabling Inheritance, add permissions by clicking "Select a principal" > Enter in "Everyone"
 
    <img width="686" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/3e9b7fe6-2b0c-4531-bf67-e0deb97d7765">

  - Click on the "Full Control" checkbox to give everyone full control (This is temporary and will be changed back later)
  - Click on "Ok" and "Apply" to apply all the changes made
 
    <img width="687" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/7c84a321-75c4-4bf9-afc9-b3e0eda6ac42">

 - ##  osTicket Configuration

  - Navigate to the osTicket installer page and press "Continue" to set up login credentials

    <img width="416" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/e8f24b98-7088-465d-9b80-f4bdceb89894">

    <img width="421" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/7df27376-877d-482d-817b-94ba5f1f1cb5">

  - Enter in desired values for the chosen fields:
    - Helpdesk Name
    - Default Email
    - First Name
    - Last Name
    - Email Address
    - Username
    - Password

  - Setup database before filling in the database section within osTicket

    <img width="211" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/fc05d5c7-9bae-43ed-b8c3-74df0d28a3bd">

  - Download the "HeidiSQL" databse client: https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit?usp=sharing
  - Run the HeidiSQL setup and run through the installation

    <img width="303" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/249c5e6e-c498-4752-89e8-fc6b0ff32941">

  - Click on "Finish" to start HeidiSQL
  - Click on "New" to create a new connection to the database
  - Type in the password for the "root" user that was created before

    <img width="347" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/d23e383d-1035-4d00-bd19-a9f41810612d">

  - Click on "Open" and you will be presented with this page, indicating a succesful database connection

    <img width="472" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/38a325b9-73a3-41bf-b696-1a09b3a875d6">

  - Create a new database within HeidiSQL by right clicking "Unnamed" > "Create New" > "Database"

    <img width="473" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/2235efa5-701e-4a03-b5a1-b755688923bb">

  - Name the database "osTicket" and click "Ok"

    <img width="162" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/f49b955c-606c-4970-bf42-c614139413e5">

  - Go back into the osTicket installation page within the web browser and enter in the database settings fields

    <img width="211" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/4d80a262-27e9-4767-8e7b-0ae3c1429ab3">

  - Click on the "Install Now" button on the bottom of the page
  - You should be able to view this page, indicating a succesful install of osTicket
    
    <img width="1092" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/8604c5e2-cda7-43f8-af29-98f5bd399c1d">

  - Additional cleanup step 1:
      - Navigate to "C:\" > "inetpub" > "wwwroot" > "osTicket" > "setup"
      - Delete the "setup folder"
    
    <img width="440" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/8b1a4936-c256-42a6-94b8-d1aaa8c444ba">

  - Additional cleanup step 2:
      - Navigate to "C:\" > "inetpub" > "wwwroot" > "osTicket" > "include" > "ost-config.php"
      - Right click "ost-config.php" > "Properties" > "Security" > "Advanced" > "Edit"
    
    <img width="850" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/5a95d628-c6b5-4228-a46b-952ea1c50d77">

      - Check the boxes "Read & Execute" and "Read"
      - Click "Ok" 

    <img width="686" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/3ebd7aad-f5db-458e-bf86-093b4ceaab6f">


 - ##  Login to osTicket as an Admin

 - Navigate to this site in a web browser: http://localhost/osTicket/scp/login.php
 - Login with your credentials

   <img width="1093" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/6995bfd9-1d06-4831-bf07-d17f50d2cc82">

 - You should be presented with this admin panel page, indicating a succesful login and installation of osTicket

   <img width="778" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/fa9bb92f-5f72-44f8-befb-1869b17dd5dd">



   

   












