**Azure Active Directory**

Azure Active Directory (Azure AD) is a cloud-based identity and access management service that allows the users to access the resources, like Microsoft 365, Azure, and other SaaS applications. Azure Active Directory also offers them to access the internal resources of the organization, such as apps on your corporate network and intranet, along with any cloud apps developed by your own organization. Azure AD provides different benefits, based on their roles, to the users.

The below given image shows how the Azure AD works. In this case, on the on-premises side, Windows Server Active Directory is using the Kerberos and NTLM (Windows New Technology LAN Manager) authentication protocols to authenticate the users. On the Azure side, Azure Active Directory is using the SAML (Security Assertion Markup Language) and OAuth 2.0 (Open Authorization) authentication protocols to authenticate the users. The Azure AD Connect is used to synchronize the on-premises Active Directory with the Azure Active Directory, so that the users can use the same credentials to access the resources on both the sides. The Azure AD Connect helps in both Authentication and Authorization.

![Image 1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/1498de1802ded82db43c7e275c9543ef136b22ae/Images/azure-active-directory-a3b1df09.png)

**Azure Directory Concepts**

- *Identity:* Identity is a set of attributes making it an object which can be authenticated. Identity can be considerably anything, such as a user with a username and password, a device, an application, or a service. As application or A server, that requires some kind of authentication to access these resources, by using some secret keys or certificates. Azure AD is the product in back which is responsible for the authentication of these identities.

- *Account:* An account is a kind of an identity which has attributes like username and password, which are an important resource for authentication. An account can be a user account, a service account, or an application account. To have an account you must need an identity.

- *Azure AD Account:* An Azure AD account is an identity which is created in Azure AD or Another Cloud Service, just like Microsoft 365. Identities are stored in the Azure AD and from there on these identities can be used to access the resources in Azure AD or Access for the services and applications which are integrated or stored in Azure AD.

- *Azure Tenant (Directory):* An Azure Tenant is a dedicated and secured instance of Azure Active Directory (AD). Every single tenant (which is also called as Directory) represents a single organization. Whenevery any organization or users sign up for Azure, a tenant is created for them. As this particular created tenant is a dedicated instance of Azure AD, it is completely isolated and separate from other tenants. This means that the users, groups, and applications which are created in a tenant are not visible to the other tenants. The tenant is also known as the Directory. Under this single tenant you can create multiple tenants, which are also known as the child tenants or resources under the same tenant.

- *Azure Subscription:*