# CS-Tech-Homelab
<h2>Project Overview</h2>
I made this project to simulate the IT infrastructure of an organization using virtual machines and Microsoft technologies. Throughout this project you will see my process of building and configuring a osTicket System, Active Directory, Virtual Machines one a Client user and the other being a Domain Server.

My goal for this project was to create a realistic environment where common IT problems can be intentionally introduced, investigated, and resolved using the same troubleshooting concepts used in an enterprise IT support environment.
Rather than simply configuring a working environment, this lab focuses on building, troubleshooting, diagnosing, and documenting the process.
<h2>Technologies and Environments Used</h2>
☁️ Cloud / Azure

🖥️ Windows / Server Administration

🏢 Active Directory / Identity

📁 File Services / Permissions

🌐 Networking

⚙️ PowerShell

🖨️ Hardware / Endpoint Support

🎫 Help Desk / IT Support

🔐 Security

# Building the Infrastructure
<details>
<summary>🖥️ 1.1 Azure & Virtual Machines</summary>

### What I Built
- <h2>Created Azure resource group<h2> <img width="1299" height="972" alt="CS-Tech-HomeLab-ResourceGroup" src="https://github.com/user-attachments/assets/b71ca1ad-6112-461f-ae4b-4da372f07a08" />
This is the Resource Group I created in Azure so I could put all of the future resources I would be using in an organized manner

- <h2>Created virtual network<h2> <img width="1372" height="1005" alt="CS-Tech-HomeLab-VNET" src="https://github.com/user-attachments/assets/834feebb-02f9-413b-b298-06e7e74eb597" />
This is the overview of the Virtual Network I built for my virtual machines to be able to connect to the internet when I created them. The virtual network is also what allows the virtual machines to connect and communicate with each other.


- <h2>Created Windows Server VM<h2> <img width="1493" height="1126" alt="Cs-Tech-DomainVM" src="https://github.com/user-attachments/assets/d9326b6c-2111-442b-9ce8-3629c672e44d" />
This is the overview of the windows server virtual machine I created. This is what served as my domain server for this project meaning this is where I built, managed, and configured the Server Manager, Active Directory, and Group Policy Management

<img width="2554" height="619" alt="CS-Tech-DomainStaticIPAddress" src="https://github.com/user-attachments/assets/0f20e026-ca70-4d9f-923c-740898871120" />
I wanted to share this picture as well as it shows setting a static IP Address to the domain server which makes it have the same IP Address all the time. This is very important because this makes it so the Client Virtual Machine is able to connect to the domain server.


- <h2>Created Windows Client VM<h2> <img width="1473" height="1194" alt="CS-Tech-ClientVM" src="https://github.com/user-attachments/assets/684d9148-bf88-4963-8dc7-9b1ea6f5db2b" />
This shows the client virtual machines overview and I had to make sure that both of my virtual machines were connected to the same network. I also had to make sure they were both using the correct image which is basically what operating system the virtual machine is using.
<img width="1261" height="1282" alt="CS-Tech-Client-DNStoDomain" src="https://github.com/user-attachments/assets/36b2b556-f5e1-47f0-a25b-b7b0ae1384f0" />
I chose to show this picture as it shows me setting the client virtual machines DNS to the Domain virtual machines IP Address which is will allow the client virtual machine to be able to essentially translate domain names we use such as google.com to their respective IP Addresses in order to find out where to send traffic to.
<img width="2559" height="1393" alt="Screenshot 2026-09-09 004435" src="https://github.com/user-attachments/assets/d0238e11-a6d0-4de6-8d4c-a9a7042efe29" />
I'm showing how both of the virtual machines are working here confirming that the setup and configuration of the virtual machines was succesful
*<h2>This concludes my building and configuration of my virtual machines<h2>*
</details>

<details>
<summary>🎫 1.2 osTicket System</summary>

### What I Built
- <h2> OsTicketing System<h2><img width="1120" height="468" alt="osTicketInstallFiles" src="https://github.com/user-attachments/assets/a7351bf7-2148-4966-ac73-487eb7c923f0" />
These are all of the file and things you have to install and configure before you can install the actual browser osTicketing system. So I went through and downloaded all os these and made sure they were configured correctly to allow for the the osTicket system to be properly installed.


<img width="2324" height="1293" alt="CS-Tech-Client-InstallingOSTicketBrowser" src="https://github.com/user-attachments/assets/b0fb384b-62c7-4cdf-891c-abd5b0b2a049" />
This is the page setting up basic information for your osTicketing system before actually installing it, such as its name the admin user and also the  SQL it will use.
- <img width="2341" height="490" alt="CS-Tech-Client-OSTicketAdmin" src="https://github.com/user-attachments/assets/80b37f2f-4ef4-4625-9044-36c484e1ba9d" />
After you set up the basics this is the landing page you get put on and this is just showing that the ticketing system was installed and working properly
<img width="2334" height="616" alt="CS-Tech-Client-OSTicketEndUser" src="https://github.com/user-attachments/assets/14ed2f78-0a98-44d4-ba35-5c2d06e7fe9d" />
I added this picture to show that the end user of the ticket system is also working as expected.

- <h2>SLA<h2><img width="2329" height="575" alt="CS-Tech-Client-ConfiguringSLA" src="https://github.com/user-attachments/assets/d9ac6819-a14d-4313-8f7a-ea984024dd55" />
This is showing a very basic SLA pr service level agreement I set up in my ticket system to simulate one inside an actually company setting. It has different severity levels SEV-A being the highest importance and SEV-C being the lowest. Below you will see the different configurations for each of the severity levels.
<img width="960" height="406" alt="SEV-A" src="https://github.com/user-attachments/assets/bf7812af-d2c7-46c7-9c77-963470695de6" />
<img width="952" height="397" alt="SEV-B" src="https://github.com/user-attachments/assets/9f081f43-b610-4da7-9521-ccc07cc1a852" />
<img width="951" height="398" alt="SEV-C" src="https://github.com/user-attachments/assets/1af37093-b473-432c-b937-1a4d6ecf678a" />

- <h2>Users<h2><img width="961" height="990" alt="CS-Tech_Client_osTicketUsers" src="https://github.com/user-attachments/assets/434eeadc-840f-402d-8515-5adc7f03fbb3" />
These are all of the users I created in my ticketing system to replicate a small company that has employees that are using the system. Now the reason all the users say "guest" has to do with the way I Created all the users. Which was instead of manually creating individual users through the ticketing systems user creation process, I had the ticketing system create a new API key which is essentially a permission slip that allows the script I used to communicate with the ticketing system. The script I used submitted HTTP requests containing each user's information to the user creation endpoint. Then the API authenticated the request using the API key, and created the users in the application's database.
*<h2>That's how I built my ticketing system<h2>*
</details>
<details>
<summary>🏢 1.3 Active Directory</summary>

### What I Built
- <h2>Installed Active Directory Domain Server<h2><img width="2198" height="1149" alt="CS-Tech-Domain-FirewallOff" src="https://github.com/user-attachments/assets/0d97b08c-4bca-444a-99ec-4cb80177dc7d" />
Here is the first thing I did to start the process of installing the Active Directory which was to configure the firewall to allow the Active Directory to be installed on the domain server.

## <img width="2198" height="1150" alt="CS-Tech-Domain-InstallingAD" src="https://github.com/user-attachments/assets/dab6bfe1-3a1b-4a0e-8990-4679d8155b83" />
Here I am showing the end of the installation process of the Active Directory after going through and configuring the installation process.

<img width="2355" height="1151" alt="CS-Tech-Domain-InstallingPromotionDomain" src="https://github.com/user-attachments/assets/75aea64c-cc35-41c4-b008-6e8b9f81419e" />
This is after installing the Active Directory I then had to promote the domain server to be the domain controller which enables it to authenticate users, enforce security policies, and manage Active Directory. This is showing it going through all the prerequisites it has to confirm. 

- <h2>Created Admin For AD<h2><img width="2345" height="1152" alt="CS-Tech-Domain-SettingUpAD DomainAdmin" src="https://github.com/user-attachments/assets/9574418e-8f7e-4414-8810-12314cb23702" />
Here I am setting up and choosing the account that will be the Active Directory admin. Which is important because it allows that user to pretty much do anything within that Active Directory.

- <h2>Created Organizational units<h2><img width="638" height="383" alt="AD" src="https://github.com/user-attachments/assets/c725f06f-1576-48ff-ae8d-970632ebf134" />
 After opening Active Directory I then made the organizational units for things such as employees, admins, accounting, and clients
 
- <h2>Created users<h2><img width="2339" height="1347" alt="CS-Tech-Domain-CreatingUserForAD" src="https://github.com/user-attachments/assets/5e9ae335-2dba-442d-afc6-ebe82c1a6da4" />
So here is where I used windows powershell ISE in order to create a couple thousand users for my Active Directory using the script shown. This is basically to just recreate a giant company that has thousands of employees which would need the Active Directory to manage all of them.

## <img width="841" height="1343" alt="CS-Tech-Domain-CheckingADUsersAreThere" src="https://github.com/user-attachments/assets/66323dc1-9a2b-4620-bddb-bfde1df2c0ae" />
This is just me confirming that all of the users that I created are actually showing up and got implemented into the Active Directory.

<img width="2348" height="1148" alt="CS-Tech-Client-AddingDomainUsersToRemoteDesktop" src="https://github.com/user-attachments/assets/8454a20a-064b-4c3d-a71a-7bc75fe291b4" />
Finally after creating all of the users I had to go to the client server and make sure all the users had access to login into the client server which I use for diagnosing tickets in future for specific users.

*<h2>That Wraps up the building and configuration of my Active Directory<h2>*
</details>

# Creating and Troubleshooting Tickets
<details>
<summary>🏢 2.1 Active Directory</summary>

### Scenario
User reports they cannot log into their account.

### Troubleshooting
1. Checked account status
2. Confirmed account was locked
3. Unlocked account
4. Tested authentication

### Evidence
- Screenshot before
- PowerShell commands
- Screenshot after

</details>

<details>
<summary>🌐2.2 Networking & Azure Networking</summary>

### Scenario
User reports they cannot log into their account.

### Troubleshooting
1. Checked account status
2. Confirmed account was locked
3. Unlocked account
4. Tested authentication

### Evidence
- Screenshot before
- PowerShell commands
- Screenshot after

</details>

<details>
<summary>💻 2.3 Endpoint & Desktop Support</summary>

### Scenario
User reports they cannot log into their account.

### Troubleshooting
1. Checked account status
2. Confirmed account was locked
3. Unlocked account
4. Tested authentication

### Evidence
- Screenshot before
- PowerShell commands
- Screenshot after

</details>






