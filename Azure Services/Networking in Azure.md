**Virtual Network**

A Virtual network is a kind of network which is used to connect the virtual devices or machines together, without any physical connection. Virtual Networks are essential and fundamental part of the Azure networking model that allows to enable the resources to communicate with other services in azure. Communication can happen between the resources over the internet with the on-premises internet.

**Azure Virtual Networks**

Azure Virtual Network(VNets) are basic blocks of the private network in Azure. VNets allows you to make complex virtual network which can be similar to of the on-premises network, with the features of cloud or Azure Infrastructure like scaling, availability and isolation.

Every VNets which is created in azure that has its own CIDR Block and can be linked with the other VNets and other on-premises network till the CIDR blocks of the VNets are not overlapping.

The Capabilities of Azure Virtual Network are:

- *Communication with the Internet:* All resources under the virtual network can communicate with the internet in outbound direction and can receive the inbound communication to the resources by using a public IP address or a public load balancer. You can use the same public IP address or public load balancer for multiple resources.

- *Communication between Azure Resources:* There are three ways in which the Azure Resources can communicate with each other:

  - First, VNets which can not only connect the VMs but also other Azure Resources like App Service Environments, Azure Kubernetes Service and Azure Virtual Machine Scale Sets.

  - Second, Azure Service Endpoints which can connect to the other Azure Resources Type like Azure SQL Databases and Storage Accounts.

  - Third, VNet Peering which can connect the VNets to each other, that allows your services and VMs to communicate with each other in the cloud.

- *Communication with on-premises Resources:* You need to securely extend the on-premises network to the cloud to communicate with the resources in the cloud. You can use the Point-to-Site VPN, Site-to-Site VPN and Azure ExpressRoute to connect the on-premises network to the cloud.

- *Filtering Network Traffic:* You can use the Network Security Groups and the network virtual appliances like firewalls, gateways, proxies and Network Address Translation(NAT) services to filter the network traffic between subnets and the VNets.

- *Routing Network Traffic:* Azure can route traffic between subnets, VNets, on-premises network and internet. You can implement the route tables or border gateway protocol(BGP) to override the default routes Azure creates.

For Instance consider, The IP Address range of 192.168.1.0/24 has some of the IP addresses in  reserve state:

- 192.168.1.0: Which is the Network Address.
- 192.168.1.1: This is reserved for the default gateway.
- 192.168.1.2, 192.168.1.3: These are reserved by Azure to map the Azure DNS IPs to VNet space.
- 192.168.1.255: This is the network broadcast address.

**Subnets**

Subnets can be considered as the sub-networks or divisions of the virtual network (VNets), creating subnets as per the requirement in your organization and security in the subscription limit. You can deploy resources to the subnets and can also control the traffic between the subnets. Subnets allow you to segment your VNet address space into multiple segments, which improves the address allocation efficiency. The smallest suported IPv4 subnet is /29 and the largest one is /2 (Using the CIDR defination). IPv6 subnets must be /64 in size. There are some things which you need to keep in mind while creating the subnets:

- Each subnet should have a unique address range under which the resources can work, and it should be specified in CIDR notation.

- There are some Azure services that requires there own subnet.

- Subnets can be used for traffic management as well. For example, You can create multiple subnets to route the traffic through the network virtual appliances like firewalls, proxies and gateways.

- You can limit the access of the Azure Resources to some specific subnets with the virual network service endpoints. You can create subnets and enable the service endpoints for some subnets and not for others. It is more of like a security feature, like if you have multiple flats in a city but you don't allow the people from one flat to enter the other flat or certain flats where you have kept your personal belongings.

**Azure Availability Zones**

As the name shows Availability Zone, it is used to define unique physical locations in a region. Every zone is made of one or more datacenters with multiple functionalities like Power, Cooling and Networking. It is designed to ensure the high availability of azure services. This allow you the seperation of Availability zone in a region protects applications and data from the datacenter failures.

You can consider the availability zone when it is designed for your azure network, and plan for services that supports availability zones.

Azure services that supports Availability Zones are divided into three categories:

- Zonal Services: Resources can be pinned or specified to a single zone, for example like Virtual Machines, Managed Disks or the standard IP addresses which helps in increased resiliency by having one or more instances of resources spread across the zones in a region.

- Zone Redundant Services: Resources are replicated or distributed across zones automatically, in this way if any of the zone goes down, the resouces and servics will be keep running and being available in the other zone.

- Non-Regional Services: Services are always available from different azure geographies and are proned to zone wide failures or region wide failures.

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

Azure assigns the resources in a virtual network a private IP address for the address space that you have provisioned, For example, if you deploy a virtual machine in a virtual network or VNet with subnet address space 192.168.1.0/24, the VM will be assigned a private IP address like 192.168.1.4, as Azure reserves the first four and last IP addresses in each subnet, for total of 5 IP addresses.

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

**Public IP address Allocation**

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

**Private IP address Allocation**

A private IP address resource can be used with multiple services resources across the azure and On-prem environment.You can assign an IP address to a resource (Static IP) or Azure can also provide an IP address to a resource (Dynamic IP).

Here you can see the private address assignment for different resources:

- You can use the NIC to assign a private IP address to a virtual machine.

- You can use the Front-end Configuration to assign a private IP address to an Application Gateway or Internal Load Balancer.

But, here you need to keep some things in mind regarding the Private IP address assignment:

- In case of dynamic IP address allocation, Azure assigns you the next available IP address which is unassigned or unreserved IP address in the subnet's address range. For instance, IP addresses from 10.0.0.5 to 10.0.0.12 are allocated to the resources, then it will assign the next available IP address which is 10.0.0.13.

- In another case of static IP address allocation, you can select or assign any of the unassigned or unreserved IP addres from the subnet's address range. For instance, Subnet's address range is 10.0.0.0/16 out of which addresses from 10.0.0.4 to 10.0.0.9 is already assigned to other resources. In this condition you can assign any address between 10.0.0.10 and 10.0.255.254.

