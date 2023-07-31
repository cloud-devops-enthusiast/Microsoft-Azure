**Azure Storage**

Azure Storage is a cloud storage solution service which is used to implement the mordern day data storage solutions. Azure Storage provides multiple options for storing various types of data in the cloud. When you think about cloud, it is all about storing data in a remote location and accessing it from anywhere in the world. 

In this blog, I will be discussing about following topics:

- Azure Storage
- Storage Accounts
- Types of Storage Accounts in Azure
- Creating a storage account in Azure
- Azure Storage Services
- Replication Strategies of Azure storage
- Storing and Accessing the data in Azure Storage

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

**Creating Azure Storage Account**

1.1. Login to Azure Portal using the credentials and Search for Azure Storage in the search bar. Choose Azure Storage from the search results. Choose add to add a new storage account.

![Image 1.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/21fe58e3c8bd9d1fa3765ea456cfd330b7279cc8/Images/Screenshot%202023-07-30%20190304.png)

1.2. In this basic section of creating a Storage account, enter the details like:

For the project details,
    Subscription: Choose the subscription from the drop down menu.
    Resource Group: Choose the resource group from the drop down menu or create a new one.
For Instance details,
    Storage account name: Enter the name of the storage account. This is required to be unique across the Azure.
    Region: Choose the region from the drop down menu and choose the location where you want to deploy the storage account.
    Performance: Choose the performance from the drop down menu. This is the type of storage account you want to create.
    Redundancy: Choose the redundancy from the drop down menu. This is the type of redundancy you want to have for your storage account like LRS, GRS, ZRS or GZRS.

![Image 1.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/57c17940bad997247720bf5415849ee78b1682dd/Images/portal.azure.com__pwa%3D11.png)

1.3. In the advanced section of creating a Storage account, enter the details like:

For the Security settings you need to enter the details like,
    Under this option you have configuration for Secure transfer required, HTTPs only and Encryption. Setting the TLS version and Permitted scope for copy operations.
    Enabling the Hierarchical Namespace for the Azure Data Lake Storage Gen2.
    Enabling the Access Protocols which enable SFTP and NFS.
    Enabling the Blob Storage setting and setting the access tier of the blob storage.
    Enabling the Azure Files setting which allows you to share large size file shares.

![Image 1.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/a2a1ee0bc322bf8b9fc36ba23b286f472e34311c/Images/portal.azure.com__pwa%3D12.png)

1.4. In the networking section of creating a Storage account, enter the details like:

For setting up network connectivity,
    Choosing the network connectivity method like selecting the public access or disabling the public access.
For setting up Virtual networks,
    Choosing the subscription, Virtual network and subnet from the drop down menu. Here we are creating new subnet and virtual network.
For setting up Network routing,
    Under this you can give the routing preference between Microsoft network routing and Internet routing. Here we will be going with Microsoft Network Routing.

![Image 1.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/bee3c28d0ac375fbd41c413e39e808e033835316/Images/portal.azure.com__pwa%3D1%20(2).png)

1.5. In the data protection section of creating a Storage account, enter the details like:

For setting up Recovery Services,
    Enabling the soft delete options for various services like Blob, File Share, Table and Queue.
For setting up Tracking,
    Enabling versioning, Blob change feed options.
For Access Control,
    Enabling the version level immutability support.

![Image 1.5](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/74c2e29e57b4b4e6f812f45927e6817c0bf2b598/Images/portal.azure.com__pwa%3D1%20(3).png)

1.6. In the Encryption section of creating a Storage account, enter the details like:

For setting up the encryption type, with options of Microsoft managed keys and Customer managed keys.
For setting up the customer managed keys, you need to create a key vault and key for the same. Enabling the infrastructure encryption.

![Image 1.6](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/6a4a1e54a227b6b4e761ffd19297dc15488ba71b/Images/portal.azure.com__pwa%3D1%20(4).png)

1.7. In the Tags section of creating a Storage account, enter the tags which you want place with your storage account deployment.

![Image 1.7](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/de56fc6305dce6779d51e7d02c92a7929cf85145/Images/portal.azure.com__pwa%3D1%20(5).png)

1.8. In the Review + Create section of creating a Storage account, review the details and click on Create to create the storage account.

![Image 1.8](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/2389fab75cbe8888e06873b687bf73563865e89f/Images/portal.azure.com__pwa%3D1%20(6).png)

1.9. Once the deployment is completed, you will see the notification on the top right corner of the screen. Click on Go to resource to go to the storage account.

![Image 1.9](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/e4ddd38548da1dd7da91c510cc87f142a5ef6fa3/Images/Screenshot%202023-07-30%20220237.png)

1.10. Once you click on Go to resource, you will be redirected to the storage account page. Here you can see the overview of the storage account.

![Image 1.10](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/c0cdddf4dbfbd8ed4b55044feeb7af8d5f5c1dea/Images/portal.azure.com__pwa%3D1%20(7).png)

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

- *Geo-Redundant Storage (GRS):* In this process of replication the data is replicated to the secondary region which is much away from the primary region like 100's of miles away. This is the more effective way of saving your data to an another location, making the data available in case of any regional outages like natural disasters or data center failures. GRS is designed in such a way that it can provide the maximum durability for your data. GRS is a perfect fit for the conditions or scenarios which are mentioned below:

    - You've a critical data which is required to be backed up and needed to be available in case of any disaster.
    - Your data governance policies require you have to store the data in the multiple data centers.
    - You want to have your data with maximum durability.

  GRS comes with two certain options from which you can choose based on your requirement:

    - GRS: In this option the data is replicated to the secondary region which is much away from the primary region. In such condition the access to secondary region is only available when primary region is unavailable which is also done by Microsoft as a part of failover process.

    - Read-access geo-redundant storage (RA-GRS): This option allows you to have read access to the secondary region even when the primary region is up and available. This option also replicates the data similar to the GRS option while also giving you the read access to the secondary region regardless of the primary region failover or downtime.

  The whole process happens like when you start the replication, it makes a replication using the LRS option and then it updates the data to the primary location using the LRS. Then the update is synchronously pushed to the secondary region using the GRS option. This process is done in such a way that it doesn't affect the performance of the application.The process of LRS happens again at the end of the secondary region to manage the replicas of the data.

- *Geo-Zone Redundant Storage:* This is the combination of the GRS and ZRS. In this process the data is replicated to the secondary regions which are much away from the primary region and also the data is replicated to the secondary zones which are situated in the same region. Which means the data is replicated to all the three availability zones of primary region and also to the secondary region. Here Every region is paired with the another region with the same region pair. With a GZRS account you can continue to read or write a data even if the primary region is unavailable. This is the most expensive option available for the replication of the data. In case your primary region is completely destroyed or gone in case of any natural disaster the data will be available in the secondary region and also recoverable.

   GZRS is designed in such a way that it can provide the maximum durability of data at 99.99999999999999% (16 9's) of the durability of the data in the given year. GZRS has a scalability target same as the LRS, ZRS, GRS or RA-GRS. Here you can additionaly enable the read access for the secondary region in the same way as you do in the GRS option.

**Accessing Azure Storage**

Every Azure Storage object comes with a unique address which is used to acces that object. Here the storage account name is used as the subdomain name for the storage account. The combination of this with the with the primary domain name of the azure storage which is specific to the azure service with which it is binded with. This whole combination forms an endpoint for your storage account. The endpoint for the storage account is in the following format:

- *Container Service:* //mystorageaccount.blob.core.windows.net
- *Table Storage:* //mystorageaccount.table.core.windows.net
- *Queue Storage:* //mystorageaccount.queue.core.windows.net
- *File Storage:* //mystorageaccount.file.core.windows.net

You can also customize the domain names for the Azure Storage Accounts which will look like \<storage-account-name>.blob.core.windows.net, for which there two ways you can do it:

- Direct Mapping: In this process you can map the custom domain for the subdomain with your azure storage account. For this you need to create a CNAME record in your DNS zone file which will point to the default domain name of the storage account. This process is also known as the direct mapping of the custom domain name.

- Intermediate Mapping: In this process, the domain is already mapped to the intermediate domain which is already mapped to the default domain name of the storage account. This process is also known as the intermediate mapping of the custom domain name.

**Uploading and Accessing an Object to Azure Storage**

2.1. Uploading file to blob and creating a blob as there is no blog available to upload the files.

![image 2.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/9beb83ffd39c06f71a0d5f1b5d03c3bfa55a702b/Images/Screenshot%202023-07-30%20221616.png)

2.2. Creating a new container to store the files.

{IMP} You need to check the role assignments, as if you don't have right role assignments you wouldn't be able to do any operations on the storage account. You need to have the role assignments of the storage account as the owner or the contributor to perform any operations on the storage account.

![image 2.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/6b5378de1eed3d7a29d19e48b40213316c8f1ca6/Images/Screenshot%202023-07-30%20221855.png)

2.3. Go to your created container and upload the file. Select the file and click on upload.

![image 2.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/35be1f5c32c04c5efda3ebe48f2643ce114df2e6/Images/Screenshot%202023-07-30%20223047.png)

2.4. Click on the upload button and select the file to upload.

![image 2.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ad5f2e95276d3b16e795e92aa636b217484c796/Images/Screenshot%202023-07-30%20223205.png)

2.5. You can access this file from anywhere using the endpoint of the storage account. You can get the url to the uploaded image and access it from anywhere.

![image 2.5](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/b52e68c3758b8f3f0a5bc8923b89ccb0a4c13425/Images/Screenshot%202023-07-30%20223647.png)

2.6. Accessing the file in incognito mode as the file is public.

![image 2.6](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/ff9c1466ccebe44aaeb0410bff746cce1d801886/Images/Screenshot%202023-07-30%20223837.png)

2.8. Original Uploaded File:

https://myazureblogs.blob.core.windows.net/myblob/catscafe-penguin.gif
