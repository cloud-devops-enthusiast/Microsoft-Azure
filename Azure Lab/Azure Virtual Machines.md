**Azure Virtual Machines**

Azure Virtual Machine is a service provided by microsoft azure which allows us to create a virtual machine based on your needs and requirements.Azure VMs comes with features like high avaialbility,auto scaling,load balancing and many more. Using this cloud service over traditional on-premise servers has many advantages like cost effectiveness,high availability,scalability and specially about maintaining them is not your headache anymore.

Azure Virtual Machines can be used for many purposes like:

- Developing and Testing: Azure VMs can be used for developing and testing the applications before delivering it to the end users or clients. Here VM's created with different OS and configurations can be used for testing the application on different platforms which will help in delivering a bug free application to the end users.

- Running Applications in Cloud: As the traffic on the application based on the business increase, which causes the application to go up and down based on the visitor traffic. Azure VMs thus keeps economies in mind and scales up and down the application based on the traffic. As the tarffic goes up you need to pay more, but you should shut-down the VMs when not in use to save the cost.

- Extension of Resources: Axure VM allows your on-premise resources to be extended to the cloud. This allow you to use the resources on the go and you don't need to worry about the maintenance of the resources.

- Migration of Applications: You can migrate your existing on-premises virtual machines using Azure Migrate service which allows you to have a seamless migration of your virtual machines to the cloud. Migration of virtual machines to the cloud allows you to have a cost effective and scalable solution.

- Web Hosting and Web Apps: Azure VMs can be used for hosting wesites and webapps which can be accessed from anywhere while providing granular control over the VMs and the resources used by them. Even if you host your website on Azure VMs, it will be less expensive then the traditional hosting services.

- Considering Storage, Backup and Recovery: When you think about your virtual machines you need to think also about the resources connected with them, out of which Storage is one of the most important part of the VMs. Azure VMs provides you with these options of Backup and Restoration of Storages while keeping the legal and compliance requirements in mind. Azure VMs which is an IaaS service offering from Azure, which provides you with the flexibility to add or remove the storage as per your needs and requirements and you only need to pay for the storage you use, this plays a major role in unpredictable demands of the business and the applications.

- Consider High-Performance Computing: Azure Virtual Machines support the High Performance computing by providing the VMs with high performance processors and GPUs. This allows you to run the applications which requires high performance computing like Machine Learning, Artificial Intelligence, etc.

- Consider Big data and Analytics: Azure VMs can also be used for the Big data and Analytics purposes. In this scenario, you can use it for massive data sets and run the analytics on them. Mining of data sets can be done using Azure VMs. 

- Considering Extended Datacenters: Azure VMs can be used for extending your on-premise datacenters to the Cloud. This also allows you to physically add the hardware to the VM and use it as per your needs and requirements. This also has the advantage of cost effectiveness and scalability. This also allows you to have a hybrid cloud solution and have to connect your physical network to the cloud network.

There are many such more uses for multiple purposes based on your needs and requirements.

**With Great Power, Comes Great Responsibility too**, There are some things which you need to keep in mind while using Azure VMs:

**Virtual Machine Configuration**

*Network Configuration of VMs*

Azure VMs can be configured with Virtual Networks which allows you to connect your VMs to make connection with other Azure Services and On-Premise Networks. Virtual Networks acts as an enclosed system which does not allows the traffic to go out of the network and does not allow you to access anything out of the network. This is enabled by default when you create a VM, this is because of the security reasons. You can also configure the VMs to allow the traffic to go out of the network and allow the traffic to come in the network. This can be done by configuring the Network Security Groups which also includes the on-premise networks. Network addresses and subnets can be configured for the VMs as well. It is important to make plans for the network configuration of your VMs before you create them as it plays a major role in the security of your VMs.

*Naming Conventions*

Naming Convention is an important part of the VMs as it helps you to identify the VMs and the resources connected with them. The virtual machine name is the same as computer name and is used to identify the VMs. You can name a virtual machine with a maximum of 15 characters on a windows VM and upto 64 characters on a Linux VM.

Virtual machine name should define what they are being used for, as well as it should consist of other attributes as well.

- If you are using the VMs for environment like development (dev), testing (QA), production (prod), etc then you can add these attributes to the name of the VMs.

- If you are using the VMs at a specific location due to some data compliance or legal requirements then you can add the location attribute to the name of the VMs like uw(US West), je (Japan East), ne (North Europe), etc.

- If there are multiple number of VMs which has similar names, then you can include this instance number into it like VM1, VM2, VM3, etc which makes it easy to identify the VMs.

- If you are using the VMs for a specific purpose like for a product or service then you can include the name of the product or service in the name of the VMs. This will help you to identify the VMs easily.

- If you are using the VMs for a specific roles like web server, security firewall or messaging server then you can include the role of the VMs in the name of the VMs. This will help you to identify the VMs easily.

For example if you name a VM as *dev-usc-webvm01* then it means that it is a development VM which is located in US Central Region and is a web server with instance number 01.

*Virtual Machine Location*

Azure VMs can be created in any of the Azure Regions, These Regions have Datacenters with all of the services are always ready to serve you with the services. You can choose the region based on your needs and requirements. 

You can also choose the region based on the legal or compliance requirements by your organization, here you can think like that too as your users are located in a specific region so you just create the resources in that region only. This will help you to reduce the latency and increase the performance of the application.

There are some things which you need to be kept in mind while considering the location of the VMs:

- The machine location decides the limits of your available options. Each region has a totally different set of options available to you. So keep this in mind all the configurations are not available in all the regions.

- There is a cost difference between the regions, so you need to keep this in your mind while choosing the region for your VMs. Try to checkout the configurations and the cost of the VMs in different regions and then choose the region which is best for you.

*Virtual Machine Size*

Azure VMs comes in different sizes and configuration, just like clothes comes in different sizes. You can choose the size of the VMs based on your needs and requirements. There are six different categories in which the VMs are divided:

- General Purpose: These VMs are used for the general purpose computing and comes with balanced CPU-to-memory ratio. These VMs are an ideal choice for testing and development purpose, small to medium databases and a low to medium traffic web servers.

- Compute Optimized: This kind of VMs are used for the workloads which requires high performance processors. These VMs are an ideal choice for the medium traffic web servers, network appliances, batch processes and application servers.

- Memory Optimized: These VMs are used for the workloads which requires high memory to CPU ratio. These VMs are an ideal choice for the relational database servers, medium to large caches and in-memory analytics.

- Storage Optimized: These VMs are used for the workloads which requires high disk throughput and IO. These VMs are the perfect choice for Big Data, SQL, NO SQL databases, Data Warehousing and large transactional databases.

- GPU: These VMs are used for the workloads which has graphic intense applications like rendering and video editing and also the compute intensive applications like Machine Learning, Artificial Intelligence, etc. This service is available with single or multiple GPUs.

- High Performance Compute: These VMs are used for the workloads which requires the fastest and most powerful processors. These VMs are an ideal choice for modelling and simulating the complex systems, high performance computing (HPC) and analytics.

After knowing a lot about the VMs size, lets think about a scenario where you want to add more cores or memory to your existing VM or you want to reduce the cores or memory of your existing VM. Here you can do this by resizing your VMs. This option gives you full control with the flexibility and elastic approach to your VMs.

*Azure Storage*

As discussed in my previous blog, Here Azure Managed Disk does all the work for you in backend and you don't need to worry about the storage of the VMs. You just need to specify the disk size and the performance you need out of your VMs.

When you create a vitual machine you have at least 2 disks attached to it, one is the OS disk and the other is the temporary disk. Virtual machines can have one or more disks in place for storing the data based on the needs and requirements. These disks can be attached or detached from the VMs as per the needs and requirements. These disks can be of two types:

- Temporary Disks: These disks are used for storing the temporary data like page or swap files. These disks are not persistent and the data stored on these disks will be lost when the VMs are shut down or restarted. These disks are not charged separately and are included in the cost of the VMs. On the Windows virtual machine these temporary disks are labelled as D: and on the Linux virtual machine these temporary disks are labelled as /dev/sdb. On Linux, the disk can be formatted and mounted as a file system at /mnt by the azure linux agent.

- Data Disks: These disks are used for storing the data which makes it a persistent disks and the data stored on these disks will not be lost when the VMs are shut down or restarted. These disks are registered as SCSI drives and are labeled with the letter you assign when you attach the disk to the VM. These disks are charged separately and are not included in the cost of the VMs.

Considerations for Azure Storage:

- Consider Azure Premium Storage: Azure premium storage is about gaining high performance, low-latency disk to gain higher IOPS and throughput. Virtual machine disks uses the SSDs for the storage of the data behind the scenes. If you don't have any specific requirements for the storage then you can use the standard storage which is the default storage for the VMs or If you have existing virtual machines in place and want a performance boost then you can upgrade the storage to the premium storage and migrate your data to the premium storage. Just keep in mind that you can't downgrade the storage from premium to standard and it will also increase the cost at the time of billing.

- Consider Multiple Storage Disks: In Azure you can attach several premium disks to a virtual machine and upto 256 TB of storage can be attached to a virtual machine. This allows your applications to achieve 80000 IOPS per virtual machine and 2000 MB per second disk throughput per virtual machine. This also allows you to have a high availability and scalability of your applications. The read operations with premium storage have a lower latency than the write operations. So if you have a read intensive application then you can use the premium storage for the read intensive operations and standard storage for the write intensive operations.

- Consider Azure Managed Disks: An azure managed disk is a VHD. Azure managed disks are the best option for the storage of the VMs as it does all the work for you in the backend and you don't need to worry about the storage of the VMs. When you provision the managed disk, Azure takes care of the rest. There available types of disks are Ultra Solid State Drives(SSDs), Premium SSD, Standard SSD and Standard hard disk drives(HDD).

- Consider Migrating to Premium Storage: If you have your existing applications running on the standard storage and migrate them to the premium storage that requires very high IOPS to run the applications. This will help you to increase the performance of the applications and also the cost will be increased at the time of billing.

*Pricing in Virtual Machines*

Here the subscription bills every Virtual machine in two parts: One is the Cost of the Compute Service and Second is the Cost of the Storage. Here this seperation help you in figuring out which is costing more and so you can scale up or down based on your needs.

- Compute Expenses: This is the cost of the VMs which is based on the size of the VMs and the time for which it is running. This is calculated on the basis of the number of cores, memory and the duration for which the VMs are running. This is calculated on the basis of per minute basis. There are two options for the payment of the compute expenses:

  - Pay as you go or Consumption based: Under this option you need to pay for the compute resoources you use and you can shut down the VMs when not in use to save the cost. This is the best option for the unpredictable workloads where you can increase or decrease the amount of resources you need. This is also the best option for the workloads which are not running 24/7.

  - Reserved Instances: This option allows you to reserve the VMs for a specific period of time like one or three years in a specific region based on your choice and need. The commitment is made in upfront and The Reserved Instances can save a lot like upto 72% of the cost of the VMs. This is the best option for the workloads which are running 24/7.

- Storage Expenses: These expenses are charged totally separately from the compute expenses. These expenses are based on the azure storage used by the disks for storing the data.

*Operating System*

Azure VMs supports multiple operating system imgaes which you can install onto your VMs. If you need more than the base layer operating system, then you can search from Azure Marketplace for the images which are available for the operating system you need. Azure Marketplace also provides you with the images for the operating system which are preconfigured with the applications like SQL Server, Oracle, etc, this helps you a lot in saving the time and efforts in installing and configuring the applications. 

If you're not able to find the operating system of your choice then you can also upload your own custom image, and use it to create the VMs. Here you need to keep a check of the operating system you are choosing should be 64- bit operating system as Azure VMs does not support 32-bit operating system.

**Connecting a Azure Virtual Machine**

There are multiple ways by which you can connect to your Azure VMs:

- Remote Desktop Protocol (RDP): This is the most common way of connecting to the Azure VMs. This is the same way by which you connect to your on-premise servers. This is the best way to connect to the Windows VMs.

- Connect using SSH: This is the most common way of connecting to the Azure VMs. This is the same way by which you connect to your on-premise servers. This is the best way to connect to the Linux VMs.

- Bastion: This is a new service provided by Azure which allows you to connect to the Azure VMs through the Azure Portal. This is the best way to connect to the Azure VMs if you don't want to use the RDP or SSH. 

- Azure Cloud Shell: This is a new service provided by Azure which allows you to connect to the Azure VMs through the Azure Portal. This is the best way to connect to the Azure VMs if you don't want to use the RDP or SSH. This is a browser based shell experience which allows you to manage your Azure resources from anywhere using a browser.

**Azure Virtual Machine Availability**

You should always keep in mind about the worst case scenario and you should always plan for it. So you need to plan for the unplanned downtime of your VMs and the applications running on them. This planning includes the unplanned hardware maintenance, unexpected downtime of the VMs, or any other planned or unplanned event which can cause the downtime of the VMs.

- An unplanned hardware maintenance can be caused due to the hardware failures or any other hardware related issues like the system predicts about certain hardware which is about to fail and so it needs to be replaced. As there is no other option for this, the VMs needs to be shifted to healthy hardware so that the VMs can be up and running again. Here the Azure Live Migration runs in the background for reducing the downtime. For during this kind of operations Azure VMs can be down for a short duration of time but the performance of the VMs might be degraded. 

- An unexpected downtime of the VMs can be caused due to the hardware and physical infrastructure failures. Such failures consists of the local network failures, local disk failures or other kind of failures. When these kind of failures are detected, Azure automatically moves the VMs to a healthy physical machine. During this process of healing the VMs, the VMs can be down for a short duration of time, sometimes in some situations there is a loss of the temporary disk data.

- A planned downtime of the VMs can be made by Microsoft Azure for the maintenance of the Azure Infrastructure to improve the overall reliability and performance of the Azure Infrastructure. This kind of downtime is very rare and is done only when it is required. This kind of downtime is done in a planned manner and is done in a way that it does not affect the availability of the VMs.

**Availability Sets**

Availability set is logical grouping of the VMs which is used for the high availability of the VMs. This feature helps in keeping the VMs up at the time when even a single point in the VM gets down due to any reason it will not be impacting any other VMs in the availability set. The grouping ensures that the all the VMs in the availability set are not updated or rebooted at the same time.

Characteristics of Availability Sets:

- All virtual machines of the same availability set should be in the same region and same subscription, should have the same softwares installed in place and should be performing the similar or identical set of functionalities.

- Azure ensures that the virtual machines from a single availability set are placed in different sevrer racks, storage units and network switches. This ensures that if any of the hardware fails then it will not affect the other VMs in the availability set and If it fails then the availability set would still be available and will be serving the customers.

- Azure allows you to create a virtual machine and availability set at the same time. You can also add an existing virtual machine to an availability set but if you have your VM in one of the availability set then you can't move it to another availability set and if you want to do so then you need to delete the VM and recreate it in the new availability set.

- You can create availability set using Azure Portal, Azure Resource Manager Templates, scripting and API tools.

Things to keep in mind while creating an Availability Set:

- Considering the redundancy: To attain the high availability of the VMs, place you VM in an availability set.

- Considering seperation of application tiers: Each application tiers should be placed in a seperate availability set. This will ensure that the VMs are not affected by the single point of failure. This will also ensure that your VMs are not updated or rebooted at the same time.

- Consider load balancing: For the high availability and network performance of the VMs, you should create a load balanced availability set. Load balancer distributes the network traffic between the VMs in the availability set using Azure Load balancer across multiple VMs in the availability set.

- Consider Managed Disks: You can make use of the Azure managed disks with your azure virtual machines across the availability sets for the block level storage.