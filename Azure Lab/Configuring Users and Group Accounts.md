**Configuring Users and Group Accounts**

There are certain types of accounts that are supported in Azure AD. These are:

- Cloud Identity: A Cloud Identity is an user account that is created in Azure AD. This kind of account contains the administrator accounts and users who are managed under the umbrella of Azure AD. Here the cloud identity can be of the accounts which are inside of the Organizations Azure AD and also the accounts which are defined in the external Azure AD instance. In other words, the cloud identity is the user account that is created in the Azure AD and is managed by the Azure AD and in case if you remove the user from the main or primary Azure AD then the user account will also be deleted and removed from the Azure AD.

- Directory-Synchronized Identity: These are the user accounts which are being declared in the on-premises Active Directory and are synchronized with the Azure AD. Here the synchronization activity usually takes place with the help of Azure AD Connect. The user accounts source is the Windows Server Active Directory.

- Guest Users: There are the type of users which are defined outside of the Azure. The main purpose of these kind of users is to provide the access to the resources like internal applications, data, and other resources to the external users like Customers or Clients. These kind of users are the invited users and are not the part of the Azure AD.

**Manage User Accounts**

There are many ways to add a user account in the Azure AD. There are multiple ways to add a user account in the Azure AD, which are through Microsoft 365 Admin Center, Microsoft Intune Admin Console and the Azure CLI.

Here we will be adding the user account through the Azure Portal:

1. Login to the Azure Portal and then click on the Users.

![Image 1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/5028265d7818ae1fdfb996f29dbf260e1d762149/Images/Screenshot%202023-07-02%20125813.png)

2. Click on the new user from the top menu.

![Image 2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/5028265d7818ae1fdfb996f29dbf260e1d762149/Images/Screenshot%202023-07-01%20214334.png)

Here you can see two options to add the user account, which are:

- Creating New User: This option is used to create a new user account which is not present in the Azure AD. 

- Invite External User: This option is mostly for the users who are not the part of the Azure AD and are external users. These kind of users can be the customers or the clients.

**Creating New User**

3.1. Click on the Create New User option, here you will land on the Create New User Page and here you will be asked to fill the details of the user account like the User Principal Name, Mail Nickname, Display Name, Password and the Account Enabled or not.

User Principal Name: This is the main name of the users account and is used to login to the Azure AD. For instance we will be using my Friends Name as the user principal name.

Mail Nickanme: This is the name which is used to create the email address for the user account. Here we will be deriving it from the User Principal Name.

Display Name: This is the name which is displayed in the Azure AD and is used to identify the user account. Here we will be using the same name as the User Principal Name.

Password: This can be the generated password or the password provided by the admin user. Here we will be using the password provided by the admin user.

Account Enabled Checkbox: This is the checkbox which is used to enable or disable the user account. Here we will be enabling the user account.

![Image 3.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/768f9f0e619932ea1b11db4d70d7c977999a30fc/Images/Screenshot%202023-07-02%20143018.png)

3.2. Moving to the another section of properties, with details like Identity, Job Information, Contact Information, Parental Controls and Settings. Here you need all the details of that specific user account so they can be identified easily.

![Image 3.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/78b3ddfeadc04fb5f776ba32a70b790f4f764f0d/Images/portal.azure.com__pwa%3D1.png)

3.3. Moving to the another section of Assignments where you can assign the user account to the specific group or the role. Here we will be assigning the *Global Reader* role to the user account.

![Image 3.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/48221dd51923c09aea3b2cd96a3b48ddbb08613b/Images/Screenshot%202023-07-02%20152148.png)

3.4. Moving to another section to Review the details entered and create the user account. Here you can see the details of the user account which you have entered and if you want to make any changes then you can go back to their respective and make it from here.

![Image 3.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/3db045d0e33d2009ca81013545097f43e96d28f4/Images/Screenshot%202023-07-02%20152626.png)

3.5. Click on the Create button to create the user account. Here you can see the user account is created successfully.

![Image 3.5](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/057f38d1de42a7f424d0a29998668dcf596e15bc/Images/Screenshot%202023-07-02%20152844.png)

3.6. Click on the user account to see the details of the user account. Here you can see the details of the user account.

![Image 3.6](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/0d6e4d18b9522e44146b043fc5f589ec68c866a3/Images/Screenshot%202023-07-02%20225315.png)

**Invite External User**

4.1. Click on the Invite External User option, which will take you to the Invite external user page. Here you will be asked to enter the details of the external user to collaborate with them.

Email: Enter the email address of the external user which you want to invite and collaborate with.

Display Name: Enter the display name of the external user whom you want to invite and collaborate with.

Send invite message Checkbox: This is the checkbox which is used to configure the invite message to the external user like "Please join us for the collaboration".

Cc recipient: Here you can enter the email address of the user whom you want to send the copy of the invite message.

![Image 4.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/84edf8e0f2278dd597acbf07772577aaa36bf77b/Images/Screenshot%202023-07-03%20234938.png)

4.2. Moving to the another section of the properties, with details like Identity, Job Information, Contact Information, Parental Controls and Settings. Here you need all the details of that specific user account so they can be identified easily.

![Image 4.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/d59af6d0b6e03b4c3ca2ce4f0beffd9e2596d7e8/Images/portal.azure.com__pwa%3D2.png)

4.3. Moving to the another section of Assignments where you can assign the user account to the specific group or the role. Here we will be assigning the *Global Reader* role to the user account.

![Image 4.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/a16d2c36fc99a51c8feba3f8cae02cd070ce28f1/Images/Screenshot%202023-07-03%20235706.png)

4.4. Now moving to the another section where we will be reviewing the details entered and can make the change if required.

![Image 4.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/876af9662f47af06355a12fcef1cf035bd5e7df1/Images/Screenshot%202023-07-04%20000331.png)

4.5. Click on the Invite button to invite the external user. Here you can see the external user is invited successfully.

![Image 4.5](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/0237169b9bf5374da105173dcd338c62084bd730/Images/Screenshot%202023-07-04%20000550.png)

4.6. Click on the user account to see the details of the invited user account. Here you can see the details of the invited user account.

![Image 4.6](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/0bfc7751ed13b8bb4afc975058ebe3453fc9f104/Images/Screenshot%202023-07-04%20000812.png)

**Bulk User Account Creation**

5.1. Go to the Users section of Azure, and choose the *Bulk Operation* option under that choose *Bulk Create* option.

![Image 5.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/21d67df22b99cab73b6d0a6c9b002efbc41fe5b5/Images/Screenshot%202023-07-04%20195921.png)

5.2. Click on the Download CSV template option to download the CSV template. Here you can see the CSV template is downloaded successfully. Now enter all the details of the user account in the CSV template. Here we will be creating the user account with the name User1 and User2, for which upload the edited CSV file to *Upload your csv file* option.

![Image 5.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/68ab6dd25f4483e9002a0a67bcfe050ed83354a1/Images/Screenshot%202023-07-04%20224727.png)

5.3. Click on Submit. After which the process will be showing *In Progress* status which will starting a bulk process of creating the user accounts and after the process is completed it will show the status as *Completed with no errors*.

![Image 5.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/856aa30b5e264cf5072243d7460c883bec9cbdfc/Images/Screenshot%202023-07-04%20225836.png)

5.4. Now you can see the user accounts are created successfully with the name User1 and User2.

![Image 5.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/420eab51a872b99b61c104439829ac479443f8a2/Images/Screenshot%202023-07-04%20231355.png)

**Group Accounts**

There are two types of group accounts in Azure:

1. Security Group: This group is used to manage the access to the resources. This can be implemented only by an Azure AD administrator.

2. Microsoft 365 Group: This group is used to manage the access to the Microsoft 365 services. This can be implemented by both normal or an Azure AD administrator.

There are some things to be considered while giving access rights to the group accounts:

1. If you want to give *Assigned* access rights, then give unique permissions to the members of the group account and only add specific kind of users to the group account only.

2. If you want to give *Dynamic membership* access rights, then you can automatically add or remove the group members based on the rules defined by you.

3. If you want to give *Dynamic Device* access rights, then you can add or remove the devices in your security groups. If any kind of attributes of the device changes, then the device will be automatically added or removed from the group account.

**Create Group Accounts**

6.1. Go to the Groups section of Azure, and choose the *New Group* option under that choose *New Group* option. Enter all the details of the group account.

- Group Type: Choose the type of the group account, here we will be choosing the *Security* group type.

- Group Name: Enter the name of the group account, here we will be entering the name as *Group 1*.

- Group Description: This contains the description of the group account, here we will be entering the description as "This group will allow the members of the group to manage the resources."

- Membership Type: This contains the type of the membership of the group account, here we will be choosing the *Assigned* membership type.

- Owner: This contains the owner of the group account, here we will be choosing the *my account* as the owner of the group account.

![Image 6.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/a4c2a624974a233e4246061e82ee2e3271d8b185/Images/Screenshot%202023-07-04%20233913.png)

6.2. Now you can see the account is created successfully with the name Group 1.

![Image 6.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/1bf635809f4605d45e7bc32dd0a37dd7160e00c8/Images/Screenshot%202023-07-05%20004247.png)

**Administrative Units**

Administrative units are usually used in the organizations where there are multiple individual or independent departments and each department has their own resource where it can be useful to restrict the administrative scope of the users roles and responsibilities. This can be implemented only by an Azure AD administrator.

- Always keep in mind that a role that has administrative permissions for only Azure AD and its resources, should be only assigned to the users who are members of the administrative unit.

- Create the administrative units based on the departments of the organization.

- You need to specifically assign the users of IT Engineering department with the roles and their scope.

**Create Administrative Units**

7.1. Go to the Administrative units section of Azure, Click on the *ADD* option to create the administrative unit.

7.2. Enter all the details of the administrative unit in the properties section.

- Name: In this section enter the name of the administrative unit, here we will be entering the name as *Engineering Team*.

- Description: In this section we will be providing the description of the administrative unit, here we will be entering the description as "This team consists of members which are responsible for managing the resources and providing access".

- Restricted Management Administrative Unit: This option allows you to block the tenant level administrators from accessing this administrative unit, here we will be choosing the *No* option.

![Image 7.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/9ef1a0a199e883eafc558141ada20797e64126f4/Images/Screenshot%202023-07-08%20001128.png)

7.3. In this section you will need to assign the roles to the users under the administrative unit. Click on each of the role and assign the users to the roles.

![Image 7.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/820d4b8188f1332cce51abacc032fbc1372432ed/Images/Screenshot%202023-07-08%20011833.png)

7.4. In this one of the last section you will need to review all the details of the administrative unit and click on the *Create* option to create the administrative unit.

![Image 7.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/77f84a673e204bd43bca3d668637fd8486117780/Images/Screenshot%202023-07-08%20012216.png)

7.5. Now you can see the administrative unit is created successfully with the name Engineering Team.

![Image 7.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/96bc4a773c03a08fa6f92c2c39fc3cf45d67aa38/Images/Screenshot%202023-07-08%20015016.png)

**Deleting Bulk Users**

8.1. Click on the *Bulk delete* option under the users section of Azure and click on the *Download* option to download the CSV file.

![Image 8.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/2b226758efeaccf0b3949bde022fee2a8beaf3a5/Images/Screenshot%202023-07-09%20193413.png)

8.2. Open the CSV file and enter the User name [userPrincipalName] of the users you want to delete and save the file. Now upload the CSV file and click on the *Delete* option to delete the users.

![Image 8.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/2b226758efeaccf0b3949bde022fee2a8beaf3a5/Images/Screenshot%202023-07-09%20193634.png)

8.3. Now you can see the users are deleted successfully from the Azure AD and can check for the delete users in the bulk operations result.

![Image 8.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/2b226758efeaccf0b3949bde022fee2a8beaf3a5/Images/Screenshot%202023-07-09%20193708.png)