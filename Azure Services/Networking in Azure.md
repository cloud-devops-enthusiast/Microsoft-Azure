**Virtual Network**

A Virtual network is a kind of network which is used to connect the virtual devices or machines together, without any physical connection. Virtual Networks are essential and fundamental part of the Azure networking model that allows to enable the resources to communicate with other services in azure. Communication can happen between the resources over the internet with the on-premises internet.

**Planning Virtual Networks**

A big benefit of migrating to cloud from the on-prem environment is to save the overall costs and simplify the administrative operations on the IT infrastructure. As after migrating to azure, the IT team needs to make the same networking functionality in the cloud environment too. So, in some kind of scenarios the resources require some kind of network isolation so that they can stay secure and risk free. Azure network services comes with many features and services.

As you have planned for the virtual network in azure, you can use the Azure Virtual Network to create one, but you need to udnerstand some things before you create one:

- An azure virtual network is a logical representation of your network in the cloud, which is dedicated to your subscription and resource group under which it is created.

- You can use these virtual networks to provision and manage the virtual private networks (VPNs) in azure.

- Every virtual network comes with its own Classless Inter-Domain Routing (CIDR) block which can be linked with the other virtual networks and in the on-premises network.

- You can also link the virtual networks with the on-premises IT Infrastructure to create a hybrid or cross-premises solution, but here you need to make sure the CIDR blocks of the Connected networks should not overlap.

- You have control over the DNS server settings for the virtual networks and segmentation of the network into subnets.

- You also need to plan for the IP address space for the virtual network and the subnets.

- You need to keep the requirement of the virtual network in mind while planning as going more than the requirement can increase the cost.

- You can also plan for the network security groups and the routing tables for the virtual network.

- Try to use a IP address space which is not used by any other network or the on-premises network in case of migration. Keep this in mind you can't redefine the IP address space once the virtual network is created.

**Create a Virtual Network**

- Seach for the Virtual Network in the search bar and click on the Virtual Network from the results.

![Image 1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/ba36d2f5f5b60af976ef6ccb3a2f80322147cc87/Images/SS1.png)

- Click on the Add button to create a new virtual network.

![Image 2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS2.png)

Here you need to enter the details like:

  - Choosing a subscription

  - Creating a new resource group or using an existing one from the drop down menu.

  - Enter the name for your Virtual network

  - Choose the region for your virtual network

- Move to the next section of Security:

![Image 3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS3.png)

  - This section focuses on the security configuration of the virtual network.

  - You can choose Azure Bastion, if you want to secure the connectivity to the virtual machines in the virtual network.

  - You can choose the Azure Firewall, if you want to secure the resources in the virtual network.

  - You can also choose the DDoS protection, if you want to protect the resources from the DDoS attacks.

- Move to the next section of IP Addresses:

![Image 4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS4.png)

  - This section lets you configure your virtual network address space with IPv4 and IPv6 addresses.

  - Here You can add an address space for your virtual network and choose from the address space type as IPv4 or IPv6 and address space size.

![Image 5](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS6.png)

  - You can also add the subnets to your virtual network with multiple options as subnet details and security options.

![Image 6](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS5.png)

- Moving to the another section of configuring the tags:

![Image 7](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS7.png)

  - Here you can configure the name/value pairs for your virtual network and this will also allow you to organize the resources in your subscription.

- At the last step, you can review the configuration and click on the Create button to create the virtual network.

![Image 8](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ecb3325263ffef9f755469060a9b137b85911d1/Images/SS8.png)