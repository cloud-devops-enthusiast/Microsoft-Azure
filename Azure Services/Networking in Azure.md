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

**IP Address Planning**

As you're designing a whole network and you must need something to make the communication between the resources. So, you need to plan for the IP address which can help you in the communication between the cloud and on premises resources. There are two types of IP addresses which are used in the Azure Virtual Network: 

- Public IP Address: Public IP address is used to communicate from the internet to the Azure resources. It is a globally unique IP address which is assigned to the resources like virtual machines, load balancers, etc. You can assign a public IP address to the resources which are exposed to the internet.

- Private IP Address: Private IP address is used to communicate within the Azure Virtual Network and the on-premises network. It is a private IP address which is not exposed to the public internet. You can create a private IP address for your resources when you use VPN gateway or Azure ExpressRoute to extend your on-premises network to the Azure Virtual Network.

![Image 9](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/92f4423e62c9f3fe119dfcdf44ec303207f061ec/Images/ip-addressing-54476e47.png)

You can consider the following points while planning for the IP address:

- IP addresses can be assigned to the resources or the services in both ways Static and Dynamic.

- Static IP addresses are best for some kind of scenarios like:
  
  - DNS Name resolution where if you change the IP address of the resource, you need to update the DNS record.

  - Apps and Services which require a fixed IP address or the applications which are frequently trying to access the resources in the Azure Virtual Network.

  - TSL and SSL certificates which are needed to be updated when the IP address of the resource changes.

  - Firewall rules that allow or deny the traffic based on the IP Address ranges.

**Create public IP address**

- Search for the Public IP address in the search bar and click on the Public IP address from the results.

![Image 10](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/92f4423e62c9f3fe119dfcdf44ec303207f061ec/Images/SS9.png)

  - Click on the Add button to create a new public IP address.

- Now you need to enter the details and information about the instance you're creating.

![Image 11](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/92f4423e62c9f3fe119dfcdf44ec303207f061ec/Images/portal.azure.com__pwa%3D1(iPad%20Pro).png)

  - Choose the subscription and the resource group under the Project Details section. 

  - Enter the region under the Instance Details, where you want to create the public IP address.

  - Under the configuration details:
    
    - Enter the name for your public IP address.

    - Choose the IP Version as IPv4 or IPv6.

    - Choose the SKU as Basic or Standard.

    - Choose the Tier as Regional or Global.

    - Choose the assignment as Static or Dynamic. Here it will be public IP address as we're creating a public IP address.

    - Choose the Routing Preference as Microsoft Network or The Internet.

    - Set the Idle Timeout in minutes.

    - Enter the DNS name label, if you want to assign a DNS name to the public IP address.

- Now you will move to the tag section, where you can manage and add th new tags to the public IP address, which will help you in organizing the resources in your subscription.

![Image 12](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/92f4423e62c9f3fe119dfcdf44ec303207f061ec/Images/SS10.png)

- At the last step, you can review the configuration and click on the Create button to create the public IP address.

![Image 13](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/92f4423e62c9f3fe119dfcdf44ec303207f061ec/Images/SS11.png)

As, When you create a public ip address, you select either the Basic or Standard SKU, which determines the IP assignment method, security, available resources and the redundancy options.

Following are the features which are supported by both the basic and standard SKU over

<table>
<thead>
<tr>
<th>Feature</th>
<th>Basic SKU</th>
<th>Standard SKU</th>
</tr>
</thead>
<tbody>
<tr>
<td>IP assignment</td>
<td>Static or Dynamic</td>
<td>Static</td>
</tr>
<tr>
<td>Security</td>
<td>Open by default</td>
<td>Secure by default, closed to inbound traffic</td>
</tr>
<tr>
<td>Resources</td>
<td>Network interfaces, VPN gateways, Application gateways, and internet-facing load balancers</td>
<td>Network interfaces or public standard load balancers</td>
</tr>
<tr>
<td>Redundancy</td>
<td>Not zone redundant</td>
<td>Zone redundant by default</td>
</tr>
</tbody>
</table>