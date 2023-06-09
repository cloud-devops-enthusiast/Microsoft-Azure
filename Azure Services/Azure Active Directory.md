**Azure Active Directory**

Azure Active Directory (Azure AD) is a cloud-based identity and access management service that allows the users to access the resources, like Microsoft 365, Azure, and other SaaS applications. Azure Active Directory also offers them to access the internal resources of the organization, such as apps on your corporate network and intranet, along with any cloud apps developed by your own organization. Azure AD provides different benefits, based on their roles, to the users.

The below given image shows how the Azure AD works. In this case, on the on-premises side, Windows Server Active Directory is using the Kerberos and NTLM (Windows New Technology LAN Manager) authentication protocols to authenticate the users. On the Azure side, Azure Active Directory is using the SAML (Security Assertion Markup Language) and OAuth 2.0 (Open Authorization) authentication protocols to authenticate the users. The Azure AD Connect is used to synchronize the on-premises Active Directory with the Azure Active Directory, so that the users can use the same credentials to access the resources on both the sides. The Azure AD Connect helps in both Authentication and Authorization.

![Image 1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/1498de1802ded82db43c7e275c9543ef136b22ae/Images/azure-active-directory-a3b1df09.png)

Azure Active Directory (Azure AD) is one of the most important and critical services of Azure, which is a Platform as a Service offering from Microsoft Azure. Azure AD provides more safe and secure access to the resources for organizations and individuals by:

- Provisioning and de-provisioning the users
- Managing Users and Groups
- Monitoring the Sign-ins
- Creating and Managing the Policies
- Configuring the Multi-Factor Authentication (MFA)
- Extending the On-Premises Active Directory to the Cloud
- Integrating with the other SaaS Applications
- Configuring the Conditional Access for Users and Devices

**Azure Directory Concepts**

- *Identity:* Identity is a set of attributes making it an object which can be authenticated. Identity can be considerably anything, such as a user with a username and password, a device, an application, or a service. As application or A server, that requires some kind of authentication to access these resources, by using some secret keys or certificates. Azure AD is the product in back which is responsible for the authentication of these identities.

- *Account:* An account is a kind of an identity which has attributes like username and password, which are an important resource for authentication. An account can be a user account, a service account, or an application account. To have an account you must need an identity.

- *Azure AD Account:* An Azure AD account is an identity which is created in Azure AD or Another Cloud Service, just like Microsoft 365. Identities are stored in the Azure AD and from there on these identities can be used to access the resources in Azure AD or Access for the services and applications which are integrated or stored in Azure AD.

- *Azure Tenant (Directory):* An Azure Tenant is a dedicated and secured instance of Azure Active Directory (AD). Every single tenant (which is also called as Directory) represents a single organization. Whenevery any organization or users sign up for Azure, a tenant is created for them. As this particular created tenant is a dedicated instance of Azure AD, it is completely isolated and separate from other tenants. This means that the users, groups, and applications which are created in a tenant are not visible to the other tenants. The tenant is also known as the Directory. Under this single tenant you can create multiple tenants, which are also known as the child tenants or resources under the same tenant.

- *Azure Subscription:* An azure subscription is a logical container which is used to provision resources in Azure, this subscripton contains the details about your payment method, billing address, and the organization that owns the subscription and the resources which are created under that subscription. Every subscription is associated with a single tenant, but a single tenant can have multiple subscriptions. The resources which are created under a subscription are billed to the payment method and billed to the billing address which is associated with the subscription.

All in once you can say as If Azure AD is a car, then the Azure Tenant is the engine, and the Azure Subscription is the fuel tank, whereas the Azure AD Account is the driver of the car, Identity is the driver's license and the Account is the car keys.

**Azure Active Directory editions**

There are Four Editions of Azure Active Directory, which comes with different features and capabilities. In which the free edition is the default edition which is available for all the Azure Subscriptions but whereas the Premium Editions are available only for the Microsoft Enterprise Agreements or the Enterprise Agreement Subscription or the Microsoft Cloud Solution Provider program or as Microsoft 365 Subscribers.

- *Azure Active Directory Free:* This is the most basic kind of Azure Active Directory Edition available for all the Azure Subscriptions. This provides you with the basic features like the user and group management, on-premises directory synchronization, with the basic reports for the cloud applications. Also this supports the Single Sign On (SSO) for the cloud applications which are integrated with Azure AD. This edition is best suitable for the organizations which are small in size.

- *Azure Active Directory Microsoft 365 Apps:* This edition is included with the Microsoft 365 suite. This edition comes with all the basic features like the one in Azure Active Directory Free edition, but also has some more and extra features to that like this edition supports the Identity and Access management for the Microsoft 365 Apps. This edition supports has branding features which lets the organization for more customization of the login and access pages. This edition also supports the Multi-Factor Authentication (MFA) for the cloud applications and the self-service password reset for the cloud applications and the on-premises applications which has been integrated with Azure AD. This edition is best suitable for the organizations which are medium in size.

- *Azure Active Directory Premium P1:* This edition is the first from the premium editions of the azure active directory. This edition comes with all the features which are available in the Azure Active Directory Microsoft 365 Apps edition, but this also lets you to do something beyond like, This edition comes with support that lets your hybrid users access the both on-premises and cloud resources at the same time. This edition gives more granular control over the cloud administration like Dynamic Groups, Self-Service Group Management and with some of the Cloud Write-back capabilities. This P1 edition includesthe Microsoft Identity Manager (MIM) which is a hybrid identity management solution for the on-premises and the cloud environments, which allows the on-premises users to allow them for self service password reset.

- *Azure Active Directory Premium P2:* This edition is the second and final kind of premium edition of the Azure Active Directory. In addition of the features of the Free and P1 editions, this edition comes with some more advanced features like Azure AD Identity Protection to provide the risk-based Conditional Access to your Apps and The critical company data. This edition also comes with the Azure AD Privileged Identity Management (PIM) which help in discovery, management, and monitoring of the privileged identities and their access to the resources and to provide the just in time access to the resources.

**Azure Active Directory Join**

This features lets you to join the devices to the Azure Active Directory, which lets you to manage the devices from the Azure AD. As azure active directory enables the single sign-on (SSO) from the devices due to which IT admins must ensure the company or corporate assets are protected and secured which meet the certain standards for the security and compliance. This Azure AD join allows the whole process of accessing the devices and the resources to simplify the windows deployments and the management of the devices.

There are some things which are needed to be considered for the Azure AD Join like:

- Azure AD has two ways to join the devices: *Azure AD Join* and *Azure AD Registered*. The azure AD join is a full-fledged domain join whereas the Azure AD registered is a lightweight version of the domain join. In Register your device to azure, the device is used to register and authenticate into the Azure Active directory and you can use the identity to enable or disable the device. In Azure AD Join, the device provides the existing features of registering the device to Azure AD and also provides extra features like changing the local state of the device, which is like the local administrator account which allows you to sign in to the device with an organizational or work account rather than a local or personal account.

- You can use other Solutions for combining the registration of the device to Azure AD and the Mobile Device Management (MDM) like the Microsoft Intune. This is a cloud-based service which lets you to provide the management of the mobile devices and the PCs from a single console. This lets you to create the conditional access rules that can enforce the access from the devices which are registered to Azure AD and meet the security and compliance standards.

- Azure AD Join is created for the scenarios where you have your own devices or servers which do not have the on-premises Active Directory Domain Services (AD DS) or the Azure AD (AD), but you can use it for the conditions like branch offices, retail stores, or schools where you do not have the on-premises AD DS or the Azure AD DS.

**Azure AD Schema**

An Azure AD Schema is a set of objects which define the attributes and the objects which can be stored in the Azure AD. This schema has less number of objects than of the on-premises Active Directory Domain Services (AD DS) schema. The Azure AD schema is extensible, which means you can add your custom attributes to the same and can extend the schema too, at the same time it is reversible too, which means you can remove the custom attributes from the schema and can revert the schema to the original state.

The effectiveness and efficiency of the features provided by the Azure AD depends on the schema. This schema can easily be seen as the blueprint of the Azure AD which can be easily seen in the existing deployments on the Cloud Services like Microsoft 365, Azure, and the Dynamics 365, which depends on the Azure AD for the identity management and support 'n' of users.

Objects in the Application and Service Principal classes define the structure of the applications in Azure AD. Here an object in the application class represents the application defination and objects that are present in the service principal class consists of the instance in the current Azure AD tenant. Seperating away the two sets of characteristics allows you to define the application in one tenant and using it in multiple tenants by creating the service principal objects in each tenant. Azure AD creates the service principal objects automatically when you register the application in the Azure AD.