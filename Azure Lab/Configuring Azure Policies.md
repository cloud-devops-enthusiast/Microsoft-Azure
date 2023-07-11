**Azure Policies**

Azure policy is a service by Microsoft Azure which allows you to Create, Assign and Manage Polices to control or audit of your resources in Azure. These policies make the resources in Azure to be compliant with the rules and regulations with the corporate standards and service level agreements. You can enforce these policies using the management groups.

**Management Groups**

Management groups are the containers which provide a wider scope for the policies above the subscriptions. Here you organize the subscriptions in the management groups, where you apply the governance conditions and policies are inherited to the subsriptions in the management groups. Management groups gives you the enterprise level management at the scale without the need to manage the individual subscriptions. All the subscriptions under the management groups must trust the Azure Active Directory tenant where the management group is created.

Here the management group can support upto six level of depth. Azure's RBAC(Role Based Access Control) authorization for the management group operations are enabled by default. The below given diagram shows the management group hierarchy. In the below image, you can see the organization has a single top-level, Root Management Group.

![Management Group Hierarchy](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/e47e168a795d501a869096d3bd14e3bdef5f9809/Images/management-groups-aa92c04a.png)

There are some ways by which you can use these management groups to manage subscriptions:

- Considering Custom Hierarchies and Groups: You can use the management groups to create the custom hierarchies and groups that meets the standards of your organizational structure and business needs. You can use the management groups to target the polices and budgets to specify the scope across the multiple subscriptions.

- Considering the policy inheritance: Controling the hierarchical inheritance of the access and rights in the policy definations is possible with the management groups. All the subscriptions under the management groups inherit the policy definations from the management groups too, where you can use these policies to enforce the constraints and condition like limiting the regions where the resources can be created or the types of the resources that can be created. You can also use the policies to enforce the tags on the resources.

- Considering compliance rules: You can create management groups to enforce the compliances based on your organizational structure or departmental structure, to meet the regulatory requirements. 

- Considering Cost Reporting: You can use the management groups to create the custom prespectives of the cost reporting, where you the scenarios like the cost reporting by the department or by the project. You can also use the management groups to create the budgets and alerts for the cost reporting, which can be applied to the subscriptions under the management groups.

In conclusion to all of the above you can use the management groups to manage the access, policies and compliance for the multiple subscriptions at the enterprise level, it is just like a big mountain where if it rains on the top, it will flow down to the bottom, where the top is the management group and the bottom is the subscription so the policies are just like the rain which flows from the top to the bottom.

**Create Management Groups**

1.1. In the Azure portal, search for and select Management groups.

1.2. Select + Create to create a new management group. Here you can see the Root Management Group, which is the top-level management group in the hierarchy. The Root Management Group is created automatically when you create your Azure subscription.

Enter the following information for the new management group: 

Management group ID (Cannot be updated after creation): My_Azure_Blogs

Management group display name: My Azure Blogs

![Image1.1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/58e95d5df76d6e85723ecc08005a35b153136e07/Images/Screenshot%202023-07-11%20232623.png)

1.3. Select Submit to create the new management group.

![Image1.2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/a4d5b7a5efe4808e10926929b8cf56677bdc6497/Images/Screenshot%202023-07-11%20233936.png)

1.4. Select the new management group to view its details.

![Image1.3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/9a4ab56709510264cccb3b1a1700e9bec16ad473/Images/Screenshot%202023-07-11%20234139.png)