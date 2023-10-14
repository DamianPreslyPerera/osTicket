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

<h2>Installation Steps</h2>

- ### Create a Windows 10 Virtual Machine within Azure
  
 <img width="1128" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/51323fc8-96d6-40ed-b3f5-b83deda12197">

- ### Configure IIS (Internet Information Services)
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




- ### Install PHP Manager for IIS 
  - Dowload PHP Manager and go through the Installation steps: https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=sharing
  - Download the rewrite module and go through the Installation steps (This is a backend module required by osTicket): https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=sharing

  - Create a directory for PHP on the C:\ Hard Drive

    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/161cf9df-52da-4df2-876d-68729a8c37c1">

  - Download the PHP zip file into the PHP directory: https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link
  - Exctract the contents of the downloaded PHP file into the previously created PHP directory

    <img width="846" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/49857146-9b00-4ae6-b6f7-c40c3015ef84">

- ### Download and Install C++ Redistributable file: https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=sharing
  
    <img width="360" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/dd409c05-a161-431a-810d-28567aa334c6">


- ### Download and Install MySQL Server
  
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

- Create a Password for the "root" user

  <img width="294" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/7df62cc7-610c-441d-bf31-94682e95b47f">




































- ### Prior to installing osTicket, dowload the following files onto the computer, the files can be found here: https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- 


<img width="1091" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/066d4d73-3ac1-4bfd-8824-7afbe547c9c9">



<img width="1092" alt="image" src="https://github.com/DamianPreslyPerera/osTicket/assets/89204562/8604c5e2-cda7-43f8-af29-98f5bd399c1d">

