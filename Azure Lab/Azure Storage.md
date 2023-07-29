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

- *Consider Storage Optimization for Massive Data:* Azure blob storage is optimized for storing massive amounts of unstructured data. Objects in the Azure Blob can be accessed from anywhere in the world using the HTTP or HTTPS.

- *Consider Storage for Messages:* Azure Queue Storage is a perfect fit for storing the messages which are in large size. Azure Queue Storage is mostly used to store and create a queue to process assynchronous messages.

**Azure Storage Services**

*Azure Blob Storage*

Azure Blob Storage is a cloud storage service which is used to store the large amount of unstructured data which is larger in size in the cloud. This unstructured or object data can be text or binary data. The Azure Blob storage is perfect fit for following scenarios:

- Providing images and documents directly access to the browsers.
- Storing files at a remote location and accessing them from anywhere in the world.
- Streaming audio and video.
- Storing the data which is used for backup and restoring, disaster recovery and archiving.
- Storing the data for analysis by on-premises users or by the Azure Services like Azure Machine Learning and Azure Data Factory.

Azure Blob Storage is a service that allows the users to access the objects using HTTP or HTTPS. As mentioned similarly the objects can be accessed using the URL's, The Azure Storage REST APIs, Azure PowerShell, Azure CLI, or Azure Storage client library. The storage client libraries are available in multiple languages including .NET, Java, Node.js, Python, php and Ruby.

*Azure Files*

Azure Files is a cloud storage service provided by Microsoft Azure which allows you to setup a highly available network file share. These file shares can be accessed using the Server Message Block (SMB) protocol or by using the Network File Shares (NFS) protocol. Here Multiple services can share the same file shares at the same time both with read and write access. Azure files can be accessed by using the Azure REST interface and or using the azure storage client libraries. Azure files is a perfect fit for following scenarios:

- While migrating to cloud, you can make use of azure files as being on-premises application mostly make use of the file shares. If you mount the same drive letter to attach azure file shares to your applications then there will be minimum efforts required to migrate the application to cloud.

- The configuration files can be stored and easily shared between multiple Virtual Machines. Tools and utilities which are used by multiple developers can be stored here in a certain location and can be accessed by multiple developers. Also you can keep all the dependencies of your application in a single location and can be accessed by multiple developers.

- Multiple kind of logs like the diagnostic logs, metrics, and crash dumps can be stored down here so they can be accessed by multiple developers and can be used for analysis.

Here the storage account credentials are used to authenticate for accessing the Azure Files, but the users must have the access to the file share. 

*Azure Queue Storage*

Azure Queue Storage is a cloud storage offering by Microsoft Azure which is mostly used to store the messages which are larger in size. Azure queue is a perfect fit for a scenario where you need to store the messages which are sent and received in queue format. Queue messages can be up to 64kb in size and can be stored in a queue which can store multiple messages in once. Queues can be used to store the messages which are used for communication between the components of an application.

In simple terms you can say it as a queue of messages which are stored in a queue and can be accessed by services or developers.Consider a scenario like changing a profile picture where you upload your picture and it is stored in a queue and then it is processed by the service which is responsible for changing the profile picture. This is a perfect fit for scenarios where you need to store the messages which are used for communication between the components of an application. Each part of the queue can be scaled separately based on the requirement, which gives you more control over the configuration.

*Azure Table Storage(Azure Cosmos DB)*

Azure Table Storage is a cloud storage service to have a fully managed NoSQL database. As table storage is schemaless, it is easy to adapt to the changing data requirements. Azure Table Storage is a perfect fit for following scenarios:

- Storing TBs of the structured data which are capable of the scaling web applications
- Storing the datasets which doesn't require complex joins, foreign keys, or stored procedures and can be denormalized for fast access.
- Quickly querying the data using a clustered index.
- Accessing the data using the OData protocol and LINQ queries with WCF Data Service .NET Libraries.

This also allow it to handle the capacity management with cost effectively serverless and autoscaling options for the applications which are used for the internet of things (IoT) and other applications which are used for the web.

**Replication Strategies in Azure Storage**

Replication is a process of copying the data from one location to another location. This process of replication is just like keeping your data safe secure at multiple places so if the data of one location gets corrupted or lost then you can recover the data from the other location. Replication also helps in complying to the standards of the data compliance. Azure Storage provides you with the following replication strategies:

- *Locally Redundant Storage (LRS):* This is the cheapest option available for the replication of the data, as it replicates the data within the same data center. This is the default option available for the replication of the data. If a condition like fire or flooding happens in your datacenter where your data is stored then you will lose your data. This option is suitable for some of the scenarios like:

    - Your data is not a critical data stored by the application and can be recovered easily.
    - Your data is more of like a temporary data or a cache data or a regularly changing data like live feeds or logs, storing which is not a big deal.
    - Your data governance policies don't require you to store the data in multiple data centers.

- *Zone Redundant Storage (ZRS):* As the name suggests the data is stored in the multiple zones situated in a single region. It is simply have 3 houses in 100km of radius and you store 3 data of your car location in each of the house. In this way every single data is stored in 3 different locations. Each zone is a separate physical location within an Azure region and every zone has its own availability zone. So all the entities of the zones and availiablity zones are different from each other. Storing your data in this fashion allows you to recover your data in case of any disaster happens in any of the zone as the data will be available in the other zone. This options allows you to have low latency and excellent overall performance.


    - Zone Redundant Storage is not available in all of the regions.
    - Switching to Zone Redundant Storage from Local Redundant Storage requires the physical migration and movement of data from one data center to another data center which has their own time and cost associated with it.