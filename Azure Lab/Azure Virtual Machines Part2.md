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