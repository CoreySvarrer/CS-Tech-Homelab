# CS-Tech-Homelab<img width="1400" height="700" alt="ChatGPT Image Sep 9, 2026, 05_41_15 AM" src="https://github.com/user-attachments/assets/1af31d44-bfe3-42c3-958e-85de669ee98d" />

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
This is going to be Phase 1 of this project. Its focal points are going to be showing how I created and configured different tools and environments using multiple technologies from the list above that I will later use in Phase 2 of this project. 
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

# Creating, Troubleshooting, and Fixing Tickets
This section of the project is Phase 2 and is going to be focused on how I used all the tools and resources that I built and configured in the Phase 1 of the project to create, simulate, troubleshoot, and diagnose real life IT help desk tickets
 <details>
<summary>🏢 2.1 Active Directory</summary>

### Ticket 1
Group Policy Settings Not Applying
## <img width="962" height="501" alt="GroupPolicySettingsTicket" src="https://github.com/user-attachments/assets/8137e22a-21c6-40e3-8d74-f4eb1da735df" />
This first ticket is simulating when an user is experiencing issues with the latest company group policy not applying for some reasoin.

## <img width="751" height="288" alt="GroupPolicySettingsCreratingGPO" src="https://github.com/user-attachments/assets/5b1a0d24-80a3-4ff7-afd8-e446decb3887" />
So this is me creating the group policy that we are going to use to simulate the issue this ticket is showing us.

## <img width="695" height="1089" alt="GroupPolicySettingsShowingGPOWorking" src="https://github.com/user-attachments/assets/167397a7-6d51-4f12-aa60-910c94f130b0" />
This is an image showing me use Microsoft PowerShell to run gpresult /r which will show us whatever group policies are being applied to this user. As you may have noticed we have logged into the users account as seen by the it saying this data is for Lily.Anderson. I am sharing this image to show how the group policy should be working before we go in to simulate the problem essentially making it not work.

## <img width="752" height="573" alt="GroupPolicySettingsRemovingAuthenticatedUsersFromFilter" src="https://github.com/user-attachments/assets/cea913b1-170e-495b-8ea4-b4d0becdb893" />
So here I am creating the issue or breaking the group policy I guess you could say. Basically I'm taking all the users that were authenticated for this group policy and deleting them off of it and replacing them with another group.
## <img width="731" height="1192" alt="GroupPolicySettingsSimulatedPolicyNotShowingUp" src="https://github.com/user-attachments/assets/09212545-a530-4cf7-ba60-ff4cef7f0c9b" />
This is where I am showing that on the  users computer the group policy that we were seeing before is no longer showing up.

## <img width="752" height="572" alt="GroupPolicySettingsFixingIssue" src="https://github.com/user-attachments/assets/a6da4f28-e073-4293-a057-6ebd8dad541a" />
This is simulating me going to the group policy manager and looking to see if there is anything I can find that is wrong that could be causing the issue, there obviously was one seeing how we created it but I identify the issue and then fix it by adding the authenticated users back into the security filter of this group policy.

## <img width="807" height="1185" alt="GroupPolicySettingsShowingFixWorked" src="https://github.com/user-attachments/assets/e2a3f75c-e309-4164-a730-87bee8f0e37a" />
This is me going back to the users account and running gpupdate /force to force the computer to update its group policies and then once again running gpresult /r to check if the group policy is now showing up on this account.
### Ticket 2
New Employee Account can't Authenticate
## <img width="965" height="495" alt="NewEmpoyleeAccountCantAuthenticateToDomainTicket" src="https://github.com/user-attachments/assets/648f1475-b9e2-415f-a89d-a4da102c3eba" />
This ticket is showing how a new employee is unable to authenticate to the domain. 
## <img width="535" height="217" alt="NewEmployeeCantAuthenticateConfirmingLoginB4Simulating" src="https://github.com/user-attachments/assets/0a3563e2-b5f2-40d3-ab01-35aa84162cd9" />
Here is me confirming that I am logged into the users account before we create the scenario of the ticket showing that it is working and able to login.

## <img width="554" height="145" alt="NewEmployeeCantAuthenticateAccountLocked" src="https://github.com/user-attachments/assets/c6ff59c7-d8b7-4616-89e6-44d7f0b507b1" />
This is showing the account is locked out now since I am simulating these tickets I know that it says its because of the amount of login attempts but I am doing that to simulate the account being locked where the root cause was the new employee's AD account was not in a valid state for domain authentication.

## <img width="1090" height="589" alt="NewEmployeeCantAuthenticateShowingWorkstationToDomainConnection" src="https://github.com/user-attachments/assets/6f6d8d64-f2c3-44b9-b3ec-a575bb8791e9" />
This is actually showing how on another account separate from the users account the workstation actually does have a connection with the domain. Meaning the issue has got to be something with the account authentication.

## <img width="412" height="546" alt="NewEmployeeCantAuthenticateUnlockingAccount" src="https://github.com/user-attachments/assets/ee8ac03f-90ae-4a8e-9ddd-5d7fc40d559c" />
This is showing the unlocking of the account which is simulating the account being locked and that being the reason the authentication was failing. So here I am unlocking the account to see if that fixes the issue/

## <img width="1204" height="221" alt="NewEmployeeCantAuthenticateLoggedBackIn" src="https://github.com/user-attachments/assets/dcfb8d38-fbf3-41e6-9690-2686a86952a2" />
Here we see the users account is logged back in which means that it was able to authenticate with the domain server and now log in.

### Ticket 3
User cant Access Department FileShare

## <img width="956" height="499" alt="UserCantAccessDeptFileShareTicket" src="https://github.com/user-attachments/assets/4b8e997d-f67c-44dc-ba67-a2500c8c1aae" />
Here is a ticket that I created to be simulating when an user can't access department file shares. 

## <img width="1122" height="633" alt="UserCantAccessDeptFileShareWorkingState" src="https://github.com/user-attachments/assets/4f3d49ce-76c7-4ddf-ad31-ca99f8e1e499" />
This photo shows what it looks like when the user is able to access the department file shares before we recreate the issue.

## <img width="407" height="357" alt="UserCantAccessDeptFileShareRemovingFromAccountingSG" src="https://github.com/user-attachments/assets/c08366a0-afb2-494a-acf2-b66106bedcd6" />
So to recreate the issue I went into the Active Directory and removing this users account from the accounting group which will make it so they can't access the departments shared files since they are no longer apart of that department.

## <img width="518" height="191" alt="UserCantAccessDeptFileShareProof" src="https://github.com/user-attachments/assets/caefb4fc-72cf-4966-95a0-26322f375c4e" />
Here Is me showing when I went back into the users account and tried to access that same department file. As you can see the access was denied.

## <img width="401" height="451" alt="UserCantAccessDeptFileShareAddingThemToDept" src="https://github.com/user-attachments/assets/4ec4198c-05ab-44c7-9cb6-7e88bc93354e" />
Here is how I went about the problem which was going into the Active directory and finding the users account and then adding them to the accounting department.

## <img width="1122" height="633" alt="UserCantAccessDeptFileShareWorkingState" src="https://github.com/user-attachments/assets/ce09db58-693e-466c-913a-d06a831bc111" />
Finally this is after I went through and added the user back into the accounting group and then checking to see if the account can now access those file shares and they were able to again, meaning the issue was fixed.

### Ticket 4
Password is expired and account is locked

## <img width="985" height="567" alt="LockedAccountTicket" src="https://github.com/user-attachments/assets/f727558c-c325-4132-89f6-4941685d85ce" />
This is a ticket simulating an account that has been locked out and can't get back in.

## <img width="556" height="150" alt="LockedAccountConfirmation" src="https://github.com/user-attachments/assets/8cf2aecf-a46e-4898-a14a-e8960e80eef2" />
So this is showing me going and confirming that the account is actually locked out and unable to log in.

## <img width="407" height="540" alt="LockedAccountOnAD" src="https://github.com/user-attachments/assets/c0ac9526-5892-4ba3-91a5-cd55872403e3" />
This is showing me going into the Active Directory and finding the users account and seeing that the account has been locked. Now before I just unlock the account I would make sure to confirm the users identity and make sure to follow all of the security protocols in place at that company. Wanted to make sure I clarified that since I cant really do that since I created this. 

## <img width="1198" height="226" alt="AccountLockedSolved-LoggedIn" src="https://github.com/user-attachments/assets/974c4b36-1bbb-43c0-a1ee-4f3622271c4e" />
Here is the account being logged back into and showing that they are indeed on the correct account and are no longer locked out.
</details>

<details>
<summary>🌐2.2 Networking & Azure Networking</summary>

### Ticket 1
Computer Receiving Incorrect DHCP Configuration 
## <img width="964" height="488" alt="ComputerReceivingWrongDHCPTicket" src="https://github.com/user-attachments/assets/051636f2-34ac-4479-8817-32d5fe46aea8" />
First thing this is showing is a ticket showing a user having DHCP issues which stands for Domain Host Configuration Protocol. 

## <img width="730" height="720" alt="ComputerReceivingWrongDHCPWorkingConfig" src="https://github.com/user-attachments/assets/f0e716eb-60bd-4fd8-916c-eee57de82969" />
First thing I wanted to show was what the proper configuration looks like before I go and recreate the issue.

## <img width="718" height="994" alt="ComputerReceivingWrongDHCPChangingDNSToSimulateDHCPNotWorking" src="https://github.com/user-attachments/assets/56470bcc-e9d1-4595-a019-26b49604cba2" />
Next thing here is me changing the DNS to simulate the issue on the ticket because what this essentially does is it makes it so the DHCP will be trying to access the original DNS and it wont be able to reach it because we changed it. This also shows me pinging 8.8.8.8 and getting a response but when I run nslookup google.com the DNS request times out.

## <img width="729" height="715" alt="ComputerReceivingWrongDHCPFixingToShowReconnectionToCorrectDHCP" src="https://github.com/user-attachments/assets/9c604667-5e01-490d-97aa-ea4bea7a1ef4" />
This image is showing how I went and fixed the issue by resetting the DNS to the correct one an then running ipconfig /renew.

## <img width="633" height="713" alt="ComputerReceivingWrongDHCPEstablishingConnections" src="https://github.com/user-attachments/assets/06c34a84-df33-4604-954d-defe81395b25" />
This is where I run a series of PowerShell commands to check and establish connections to multiple things to make sure the DHCP and DNS are both working.

### Ticket 2
VPN Connects but Internal Resources are Inaccessible
## <img width="964" height="431" alt="VPNConnectsButInternalsDontTicket" src="https://github.com/user-attachments/assets/d43d5042-b0e1-4e76-8e76-3123cac84774" />
This is a recreation of a ticket simulating a VPN issue where the VPN connects but the internal resources are unable to be used or accessed.

## <img width="1422" height="575" alt="VPNConnectsCreatingTheConnectionError" src="https://github.com/user-attachments/assets/3e3d2449-f45e-415b-b8ad-df6108addea6" />
This is how I simulated a scenario where a VPN connection provides Internet access but internal network resources are inaccessible. Seeing how I am using a virtual machine I couldn't figure out a way to actually create a real VPN so i focused on recreating the same result using a different method for the purpose of the lab.

## <img width="608" height="623" alt="VPNConnectsSimulatingVPN InternetConnection" src="https://github.com/user-attachments/assets/0ad03160-883e-487b-a15f-5cd604f17de2" />
So basically the this is showing that the connection to the internal server is working but  they're unable to establish the connection required to access the internal file share. But that the connection is working showing that I can ping an external Internet Address.

## <img width="685" height="294" alt="VPNConnectsConnectionComingBackTrue" src="https://github.com/user-attachments/assets/99a1edc0-633a-4822-9119-f8aa6e9697ff" />
This where I'm showing how the connection is now coming back true showing the issue is now fixed showing that we now have access to the internal server and therefore access to the internal resources.

### Ticket 3
Unable to Connect to Office WIFI
## <img width="964" height="437" alt="osTicket-UnabletoConnecttoNetwork" src="https://github.com/user-attachments/assets/3586a44d-c948-4b79-b6b0-bbc8ea22ad1b" />
Here is a very common ticket that comes up a lot for a lot of a different reasons an user is unable to connect to the network.

## <img width="663" height="722" alt="NoNetworkDiagnosticPowerShell" src="https://github.com/user-attachments/assets/b2899b59-5e95-4d80-a138-ea3f4c8134de" />
So this me running ipconfig /all to see the ip configuration to check for anything abnormal or out of place. After not finding anything I ping 8.8.8.8 to test network connection and it comes back with a response meaning that the network is in fact coneected. I finally run ping google.com and it comes back could not find host name meaning that the issue is probably actually with the DNS.

## <img width="531" height="475" alt="NoNetworkTestingSolutionComplete" src="https://github.com/user-attachments/assets/509da90e-290a-4f3f-ab5b-bea4781e46b4" />
Finally here is where I go and flush the DNS cache and then retry pinging google.com which this time we get a response. This mean the issue is fixed and what the user thought was a network issue was actually an issue with the DNS so they weren't able to reach domain names when they searched them up.
</details>

<details>
<summary>💻 2.3 Endpoint & Desktop Support</summary>

### Ticket 1
Outlook is not receiving new messages
## <img width="964" height="474" alt="OutlookNotReceivingMessages" src="https://github.com/user-attachments/assets/c40009a6-0306-4233-89ab-6b9509b76f82" />
This is a ticket simulating an user not getting any new messages on their outlook.

## <img width="626" height="512" alt="OutlookNotReceivingMessagesTestEmailPreRule" src="https://github.com/user-attachments/assets/9a63b74d-e346-440e-a71d-22b8032f81d8" />
So this is the outlook I created for this user to simulate them getting messages before we create a rule that will make it look like they aren't receiving any messages. So here is them receiving messages.

## <img width="1606" height="380" alt="OutlookNotReceivingMessagesTestEmailSentFromITpro" src="https://github.com/user-attachments/assets/51048ea0-d529-4a7b-83ed-f60f0424ed61" />
Here is me sending a test email or message to see if they are still receiving messages.

## <img width="628" height="384" alt="OutlookNotReceivingMessagesDidntReceiveTestEmail" src="https://github.com/user-attachments/assets/115735b2-e6bc-4107-8722-853724087204" />
This is showing after I sent that email it is nowhere to be seen and has not been received by the users outlook account.

## <img width="1279" height="585" alt="OutlookNotReceivingMessagesFindingTheRule" src="https://github.com/user-attachments/assets/c39c4796-21a3-4f48-854c-1b5f06a2634f" />
I then go and look into their mail setting and then go look into the mail rules and find a rule that is sending all mail received to go straight into the spam folder. That explains why it looked why they thought the weren't getting any new messages.

## <img width="2247" height="402" alt="OutlookNotReceivingMessagesTestEmailAfterRuleDeletion" src="https://github.com/user-attachments/assets/05efc061-fc02-4acd-b878-aecca55ee67a" />
This is finally after we deleted the rule that was in place and you can now see that the test emails we have sent are now showing up in the correct folder.

### Ticket 2
Printer not appearing on workstation
## <img width="951" height="550" alt="PrinterNotConnectedTicket" src="https://github.com/user-attachments/assets/99895e59-3c49-487e-9d65-f2ccfb8348ba" />
This is A ticket that was created to simulate a printer not being connected to the network.

## <img width="1211" height="340" alt="PrinterNotConnectedConfirmingError" src="https://github.com/user-attachments/assets/f1bea76a-24d3-4949-a6d9-082e1aeff094" />
So this was me going in and confirming that the printer was actually not connected and it wasn't. In order to simulate this I actually had to create a fake printer so I did that and since it was a fake printer that made sure the connection would fail.

## <img width="454" height="523" alt="PrinterNotConnectedPrintersIPaddress" src="https://github.com/user-attachments/assets/7b8bbc74-d542-4ffa-8803-603ce07823de" />
This is an image showing me going into the setting of the printers and then finding the one I was looking for and then goin into its properties and checking to see what the devices IP Address was.

## <img width="592" height="371" alt="PrinterNotConnectedPingedIPaddress" src="https://github.com/user-attachments/assets/8a3ac337-aed8-4c19-b17d-9fa1fe30e3ff" />
This is why we needed that IP Address because we are now pinging it to see if we can get a response which we didn't. This means that we are unable to communicate with the printer over the local network.

## <img width="611" height="735" alt="PrinterNotConnectedPinging8 8 8 8 google com" src="https://github.com/user-attachments/assets/05bb0f95-4749-4682-bd01-53bc6e24a26b" />
We then ping 8.8.8.8 and google.com to show that we do have internet access and also that our DNS is working properly. This helps give us more information to make sure that certain things are still working and not the issue, such as that the IP connectivity and DNS resolution are both working.

## <img width="741" height="713" alt="PrinterNotConnectedipconfigall" src="https://github.com/user-attachments/assets/47304033-b808-4036-a19b-c68b417c39e1" />
Finally to get a full picture of everything I ran ipconfig /all to make sure everything was working properly and I didn't find anything wrong which leads me to conclude that the printer is not working due to some kind of printer side connectivity or hardware issue.
</details>






