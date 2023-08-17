**Creating a Virtual Machine**

1. Go to Azure Portal and click on **Virtual Machines** and then click on **Add**.

![Image 1.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/42820c42506c0a2364d0f1b9811ad9f481d39a6c/Images/Screenshot%202023-08-15%20224310.png)

2. Now you will be on the Basics tab. Here you will need to fill in the following details:

- *Subscription*: Select the subscription you want to use for this VM.
- *Resource group*: Select the resource group you want to use for this VM.
- *Virtual machine name*: Enter a name for your VM. Here we will be using as Test_VM.
- *Region*: Select the region you want to use for this VM. Here we will be deploying in East US.
- *Availability options*: Select the availability options you want to use for this VM. Here we will be using as No infrastructure redundancy required.
- *Security Type*: Select the security type you want to use for this VM. Here we will be using Standard.
- *Image*: Select the image you want to use for this VM. Here we will be using Ubuntu Minimal 22.04 LTS.
- *VM Architecture*: Select the VM architecture you want to use for this VM. Here we will be using x64.
- *Size*: Select the size you want to use for this VM. Here we will be using Standard_B1s.
- *Username*: Enter a username for your VM. Here we will be using as azure_user.
- *SSH public key source*: Select the SSH public key source you want to use for this VM. Here we will be using as Generate new key pair.
- *Key pair name*: Enter a key pair name for your VM. Here we will be using as azure_key.
- *Public inbound ports*: Select the public inbound ports you want to use for this VM. Here we will be using as Allow selected ports.
- *Select inbound ports*: Select the inbound ports you want to use for this VM. Here we will be using as SSH (22), HTTP (80), HTTPS (443).

![Image 1.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/3f0e92015353e5b925c4eed270cd5090ba6bcebd/Images/portal.azure.com__pwa%3D13.png)

3. Now you will be on the Disks tab, Here you will need to fill in the following details related to the disks:

*VM Disk Encryption*

- *Encryption at the host*: Select the encryption at the host you want to use for this VM. This option enables the encryption for the temporary disks and ephemeral OS disks with the platform managed keys  Here we will be using as Disabled.

*OS Disk*

- *OS Disk Size*: Select the OS disk size you want to use for this VM. Here we will be going with the Resize to 32 GiB (P4).
- *OS Disk Type*: Select the OS disk type here we will be going with Standard SSD. (Locally Redudant Storage)
- *Delete with VM*: Select this checkbox if you want to delete the created drive at the time of VM deletion.
- *Key Management*: Select the key management as Platform managed key. This will be used to encrypt the OS disk.

*Data Disk for the TestVM*

As we don't have any data disk prior to this, we will be adding a new data disk to the VM. So for this we will be going ahead with the Create and attach a new disk option.

- *Name*: Enter a name for your data disk. Here we will be using as TestVM_DataDisk.
- *Source Type*: This option allows you to configure your data disk as Snapshot, Storage blob, or None (Empty Disk). Here we will be using as None (Empty Disk) as we dont have any data disk prior to this.
- *Size*: This option determines the size of the data disk. Here we will be using as 32 GiB with Standard SSD (Locally Redudant Storage).
- *Key Management*: Select the key management as Platform managed key. This will be used to encrypt the data disk.
- *Enable Shared Disk*: Enable this option if you want to use the disk as a shared disk with other VMs as well. Here we will be using as Disabled.
- *Delete Disk with VM*: Select this checkbox if you want to delete the created drive at the time of VM deletion. Here we will be checking this as Enabled.

![Image 1.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/1de1619f5b98e4871372e082e0942736070f9afe/Images/portal.azure.com__pwa%3D14.png)

*Advanced*

- *Use managed Disks*: Select this checkbox if you want to use managed disks for your VM. Here we will be using as Enabled.
- *Ephemeral OS disk*: Select this checkbox if you want to use ephemeral OS disk for your VM. Here we will be using as None.

![Image 1.4](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/b3feaa3f11a58ec41d61225261e1f5f95102e209/Images/portal.azure.com__pwa%3D15.png)

4. Now you will be on the Networking tab, Here you will need to fill in the following details related to the networking:

*Network Interface*

- *Virtual Network*: This is the virtual network that will be used for the VM. Here we will be using as TestVM-vnet.
- *Subnet*: This is the subnet that will be used for the VM. This will be the default subnet as (10.0.0.0/24).
- *Public IP*: This is the public IP that will be used for the VM. Here we will be using as TestVM-ip.
- *NIC network security group*: The NSG is a set of security rules that allow or deny any of the inbound or outbound traffic for the VM. Here we will be using the basic one.
- *Public Inbound Ports*: This is the public inbound ports that will be used for the VM. Here we will be using as Allow selected ports.
- *Select Inbound Ports*: This is the inbound ports that will be used for the VM. Here we will be using as SSH (22), HTTP (80), HTTPS (443).
- *Delete public IP and NIC when VM is delete*: Select this checkbox if you want to delete the created public IP and NIC at the time of VM deletion. Here we will be using as Enabled.

*Load Balancing*

This shows you the option for placing your VM in a backend load balancer pool. Here we will be using as None.

- *Place this virtual machine behind an existing load balancing solution*: We will be unchecking this as we will be using as None.

![Image 1.5](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/aa361e833c355a0c5777fd261c9d377921f48360/Images/portal.azure.com__pwa%3D16.png)