**Azure Storage**

Azure Storage is a cloud storage solution service which is used to implement the mordern day data storage solutions. Azure Storage provides multiple options for storing various types of data in the cloud. When you think about cloud, it is all about storing data in a remote location and accessing it from anywhere in the world. Azure Storage provides the following storage options:

There are mainly three categories of storage options available in Azure Storage:

- *Virtual Machine Data:* Virtual machine data consists of the data that is stored on the virtual storage devices like disks and files stored onto them. Here the disks are kind of persistent block storage whereas Files are the File shares that are stored onto the cloud.

- *Unstructured Data:* This is a kind of data which doesn't have a specific format. This type of data is stored can't be stored in the traditional databases, as Unstructured data has its own internal structure. The format of unstructured data is more to be referred as non-structural data.

- *Structured Data:* It is a data which is stored in a structured format, which has a well-defined structure and can be stored in the traditional databases. The data is stored in the form of rows and columns. This type of data is also referred as relational data. Tables are an autoscaling no-sql database service that is provided by Azure.

There are primarily four types of storage accounts available in Azure:

- *Standard general-purpose v2:* This is the most commonly used type of storage account and generally available as a default option. This kind of storage consists of Blob Storage (Data Lake Storage), Queue Storage, Table Storage and Azure Files as Storage options.

- *Premium block blobs:* This type of storage account is primarily used for storing the data of scenarios with high number of transactions or to store smaller objects or to have low storage latency. This type of storages comes with LRS (locally redundant storage) and ZRS (zone redundant storage) options. This kind of storage consists of Blob Storage (Data Lake Storage) as Storage option.

- *Premium file shares:* This kind of storage account is specifically used for sceanrios where you need to have higher performance and higher throughput. The use of this account is adviced in case if you need to have storage account that should support both Server Message Block (SMB) and NFS or Network File Shares. This storage account comes with LRS (locally redundant storage) and ZRS (zone redundant storage) options. This kind of storage consists of Azure Files as Storage option.

- *Premium Page Blobs:* This kind of storage account is specifically used for the scenarios where you need to have something in behind to support your Azure IaaS. The storage service available under this option is Page Blobs. This storage account comes with LRS (locally redundant storage) only.

*The above stated 3 storage account options are available only in the premium tier which have SSDs as the underlying storage media due to which they are able to achieve lower latencies and higher throughput.*

As I have mentioned earlier in my older blogs, You need to think and verify the requirement on which you will be deploying the resources in Azure. You must be aware of the fact that the resources deployed in Azure are charged on the basis of the usage. So, keep your resources in check and deploy only those resources which are required for your application to run.

So, there are certain things which you need to have in place for consideration:

- *Consider Durability and Availability:* You need to know Azure Storage is durable and highly available resource. Where, Redundancy keeps check of your data is safe during the times of downtime, and Availability keeps check of your data is available for access during the times of downtime. 

- *Consider Secure Access:* Every bit of data stored into Azure is secured by default using the encryption. Also, Azure Storage provides you with the granular control over the access of the data stored into it. You can control the access of the data stored into Azure Storage using the Azure Active Directory, Shared Access Signatures and by using the Access Keys.

- *Consider Scalability:* Azure storage is scalable based on the requirement like adding more storage space or increasing the throughput. You can scale the storage account based on the requirement.

- *Consider Manageability:* This feature of Azure Storage provides you with tools and utilities to manage the data stored into Azure Storage while handelling the hardware maintainence, upgrades and patching the critical issues for your sake.

- *Consider Data Accessibility:* Azure storage allows you to access data from anywhere in the world over the internet using HTTP or HTTPS. You can also access the data stored into Azure Storage using the Azure Portal, Azure CLI, Azure PowerShell, Azure Storage Explorer, Azure Storage Client Libraries, Azure REST API and Azure Storage REST API.

**Azure Storage Services**

*Azure Blob Storage*

Azure Blob Storage is a cloud storage service which is used to store the large amount of unstructured data which is larger in size in the cloud. This unstructured or object data can be text or binary data. The Azure Blob storage is perfect fit for following scenarios:

- Providing images and documents directly access to the browsers.
- Storing files at a remote location and accessing them from anywhere in the world.
- Streaming audio and video.
- Storing the data which is used for backup and restoring, disaster recovery and archiving.
- Storing the data for analysis by on-premises users or by the Azure Services like Azure Machine Learning and Azure Data Factory.

Azure Blob Storage is a service that allows the users to access the objects using HTTP or HTTPS. As mentioned similarly the objects can be accessed using the URL's, The Azure Storage REST APIs, Azure PowerShell, Azure CLI, or Azure Storage client library. The storage client libraries are available in multiple languages including .NET, Java, Node.js, Python, php and Ruby.

