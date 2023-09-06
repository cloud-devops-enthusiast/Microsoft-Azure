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

5. Now you will be on the Management tab, Here you will need to fill in the following details related to the management:

*Microsoft Defender for Cloud*

It is a cloud-based security service that helps you protect your organization's data and endpoints against cyberthreats.

*Identity*

- *Enable system assigned managed identity*: This is a system assigned managed identity that enables the authentication to the cloud services without storing the credentials in the code. Here we will be using as Enabled.

*Azure AD*

- *Login with Azure AD*: This is the Azure AD feature that enables the authentication to the VM, enforcing MFA and enabling RBAC. Here we will be using as Enabled.

*Auto-shutdown*

This features enables the auto-shutdown of the VM at a specific time. Here we will be using as Disabled.

*Backup*

This feature enables the backup of the VM. Here we will be using as Disabled.

*Guest OS Updates*

- *Patch Orchestration Options*: This feature enables the patch orchestration options for the VM. Here we will be using as Image-Default.

![Image 1.6](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/ee7138e61e8e58c7e9a654e0d1043ec320972af3/Images/portal.azure.com__pwa%3D17.png)

7. Now you will be on the Monitoring tab where you can enable the monitoring for the VM.

*Alerts*

This feature enables the alerts for the VM.

- *Enable recommended alert rules*: This feature enables the recommended alert rules for the VM. Here we will be using as Disabled.

*Diagnostics*

This feature enables the diagnostics for the VM.

- *Boot Diagnostic*: This is a feature for the VM to troubleshoot the boot failures and this also improved the creation time of the virtual machine. Here we will be Enable with managed storage account.
- *Enable OS guest Diagnostics*: It is more like of a monitoring feature that enables the monitoring of the VM. Here we will be using as Disabled.

![Image 1.7](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/381843784b8b71ea6f0b11c2a11fb8ed961fdaf8/Images/portal.azure.com__pwa%3D18.png)

8. Now you will be on the Advaned tab where you can enable the advanced features for the VM.

*Extensions*

This feature enables the extensions for the VM, this helps in the post deployment configuration of the VM.

- *Extensions*: Here we will not be using any of the extensions here.

*VM applications*

This feature allows you to install the applications on the VM at the time of deployment.

*Custom data and cloud init*

This feature allows you to run the custom scripts at the time of deployment. You can also add other data while the process of provisioning the VM.

- *Custom data*: Here we will be using as None.

*User Data*

This feature allows you to have your data available on the VM at the time of deployment.

*Performance (NVMe)*

This feature allows you to have the NVMe disk for the VM and boost the performance of the VM.

*Host*

If you want to manage the host for the VM, you can enable this feature.

*Capacity reservations*

This feature allows you to reserve the capacity for the VM.

*Proximity placement groups*

If you want to keep your Azure Resources physically closer to each other, you can enable this feature.

![Image 1.8](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/8107b9d20776c8a2c0c67426780be8665078f000/Images/portal.azure.com__pwa%3D19.png)

9. Now you will be on the Tags tab where you can add the tags for the VM. These tag will help you in the billing and the management of the VM. If you create tags and change their assignments, you can use the tags to filter the view of your resources in the portal.

![Image 1.9](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/bcafd6b746719ab9ff0635761a84ad31a58291d7/Images/portal.azure.com__pwa%3D20.png)

10. At this step you will be on the Review + create tab. Here you can review all the settings that you have configured for the VM. If you want to make any changes, you can go back to the respective tab and make the changes. If you are satisfied with the settings, you can click on the Create button to create the VM.

![Image 1.10](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/755f5777deb90cfd7fb7e4a80fb1b267516178f6/Images/portal.azure.com__pwa%3D21.png)


As you will create the VM you will see a pop-up to Generate the key pair. As you will click on download and create resources it will download a PEM file.

![Image 1.11](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/6fc4a25f36c39ba5adc95d7ae6811c687da098a6/Images/Screenshot%202023-09-04%20230954.png)

Here you can see that the VM is being created and other resources with it are created as well.

![Image 1.12](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/6fc4a25f36c39ba5adc95d7ae6811c687da098a6/Images/Screenshot%202023-09-04%20231215.png)

As the VM is created you can see the overview of the VM.

Now, you can connect to the VM using the SSH key pair that you have downloaded or the connect page from the VM.

![Image 1.13](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/bdd96e4ea44f61e523c7328f2a1b57d7e50d306b/Images/Screenshot%202023-09-04%20232020.png)

Now we will connect the VM using our local machine using the Azure CLI which is installed on our local machine.

```
az login
```

Enter this command to login to your Azure account, when you enter this command you will see a pop-up to login to your Azure account. Enter the credentials and login to your Azure account.

![Image 1.14](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/bdd96e4ea44f61e523c7328f2a1b57d7e50d306b/Images/Screenshot%202023-09-04%20232626.png)

Before connecting to your created VM you need to make your VM SSH ready, for which azure comes with all the pre-requisites installed on the VM to connect to it. This process lets you enable the port 22 on the VM with the Just in Time policy of the VM.

![Image 1.145(https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/8c69930197f9b64810e99fd314d9dfb48d0a0829/Images/Screenshot%202023-09-06%20220925.png)

Now, you will need to enter the following command to connect to the VM.

```
az ssh vm --ip 20.163.159.76
```

Here you will need to enter the IP address of your VM. As you will enter this command you will see a pop-up to enter the SSH key pair. Enter the path of the PEM file that you have downloaded and enter the passphrase for the PEM file. Here it will ask you to install an extension ssh to connect to the VM. Enter y to install the extension.

![Image 1.16](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/367c0a26abd213d2d2eae671c1984ca6d753fb17/Images/Screenshot%202023-09-04%20233742.png)

![Image 1.17](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/8c69930197f9b64810e99fd314d9dfb48d0a0829/Images/Screenshot%202023-09-04%20233925.png)

Now, We will just update the VM.

```
sudo apt-get -y update
```

![Image 1.18](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/fcdc6ad8a47252c96d2afcc2b64f70da2fd6b8f8/Images/Screenshot%202023-09-04%20235013.png)

Now, we will be installing NGINX web server on the VM.

```
sudo apt-get -y install nginx
```

![Image 1.19](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/bf6a47f29d6f15f4124048765515cf2cd37dccce/Images/Screenshot%202023-09-06%20230034.png)

![Image 1.20](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/bf6a47f29d6f15f4124048765515cf2cd37dccce/Images/Screenshot%202023-09-06%20230057.png)

Now, we will check the status of the NGINX web server.

```
sudo systemctl status nginx
```

![Image 1.21](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/3198aed638bc406b827ded28ff71db7228f0d675/Images/Screenshot%202023-09-06%20231046.png)


Now, we will check the status of the NGINX web server on the browser.

```
http://<PUBLIC IP ADDRESS>/
```

![Image 1.22](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/fa7e3a31e134852bcc356fa3331ee653432e8e38/Images/Screenshot%202023-09-06%20231347.png)

We can also check the status of the NGINX web server on the Azure portal.

```
curl -m 80 <PublicIPAddress>
```

![Image 1.23](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/5c569036c90bf8f7394555ad327508e5fb81edab/Images/Screenshot%202023-09-06%20232534.png)