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