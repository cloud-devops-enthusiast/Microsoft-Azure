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