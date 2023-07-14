**Azure Policies**

Azure policy is a service by Microsoft Azure which allows you to Create, Assign and Manage Polices to control or audit of your resources in Azure. These policies make the resources in Azure to be compliant with the rules and regulations with the corporate standards and service level agreements. You can enforce these policies using the management groups. Azure Policies evaluate and access your resources to make them sure that they are compliant with the policies that you have enforced in place.

When you plan to implement the Azure policies, you need to consider the following things:

- Consider Deployable Resources: Before you enforce any policy you need to specify the scope of the policy, like here you need to specify the resources that you can deploy using the Azure policy. You can specify the set of Virtual Machines, Storage Accounts, Key Vaults, etc that under your organization can deploy. 

- Consider Location Restrictions: You can also specify the locations where the resources can be deployed. You can specify the locations like the regions or geographical locations which are available to your organizations.

- Consider Rules Enforcement: You can specify the rules and the configuration options under which the resources can be deployed in your organization. You can also specify the required tags for the resources that are deployed in your organization.

- Consider Inventory Audits: You can use the Azure policy here with Azure Backup Service over your workloads and run inventory audits to make sure that the resources are compliant with the policies that you have enforced in your organization while ensuring the backup of your resources.

**Creating Azure Policies**s

You can create Azure policies using Azure CLI or Azure portal. Here we will create the Azure policies using the Azure portal. There are four basic steps which are required to create the Azure policies:

- Step 1: Create the policy definition: A policy definition is just like a logic which needs to be satisfied by the resources to perform certain actions in your organization. You can either create your own policy definitions or you can use the buil-in-policy definitions. For example, you can create a policy definition to specify the locations where the resources can be deployed in your organization.

- Step 2: Create an initiative definition: An initiative definition is a collection of multiple policy definitions which help you to keep log of the compliance of your resources and also gives you a wider scope to manage the policies. You can either create your own initiative definitions or you can use the built-in initiative definitions. You can use the initiative definition to verify and ensure your resources are compliant with the security requirements.

- Step 3: Scope of the initiative definition: Azure Policies lets you to control how the initiative definitions are enforced to your resources in your organization. In the same you can also specify the scope of the initiative definition to the specific management groups, subscriptions or resource groups.

- Step 4: Determine Compliance: As you allot the initiative definition, where you can check the compliance of the resources in your organization. Individual resources, resource groups and subscriptions within a scope can be unchecked from the compliance of the initiative definition. Exclusions are handled individually for each initiative definition.

For Creating the Azure Policies, you need to follow the below steps:

1.1: Search for the **Policy** in the Azure portal and select the **Policy** from the search results.

![Image 1](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/553c263be85ae775d744613fd66c0cf4e030e142/Images/Screenshot%202023-07-14%20221846.png)

1.2: In the **Policy** blade, select the **Definitions** from the left pane. Here you can see the list of the built-in policy definitions. You can also create your own policy definitions by selecting the **+ Policy definition**.

![Image 2](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/7ccd0f40db63a5ef8cb4eab8e012895ffca33955/Images/Screenshot%202023-07-15%20000927.png)

1.3: As you start with creating a *Policy Definition* you need to add the following details:

- **Definition location**: It will be the location where you want to create the policy definition. You can select the location from the drop-down list. Here we have two options, either we can use the *Management Groups* or *Subscriptions*.

![Image 3](https://github.com/cloud-devops-enthusiast/Microsoft-Azure/blob/9b0eac8038f18b68860aeb2e1810fbb4969ed99f/Images/Screenshot%202023-07-15%20015006.png)

- **Name**: It will be the name of the policy definition.

- **Description**: It will be the description of the policy definition.

- **Category**: It will be the category of the policy definition whether it can be a newly created or an existing one.

- **Policy rule**: It will be the rule which you want to enforce on the resources in your organization. You can either create your own policy rule or you can use the built-in policy rule. Here we will use the built-in policy rule.

![Image 4]()

**Advantages of Azure Policies**

- Enforce Rules and Compliance: This allows you to enforce the rules and compliance on the resources in azure. Azure policies can here be used for the real time policy evaluation which makes it more practical to test the policies before enforcing them also if you want to do some changes in the policies you can take some time or periodic changes to the policies which makes it more flexible to on-demand compliance and governance.

- Applying Policies at Scale: Enforcing policies to a management group which gives you a whole cover like umbrella to the subscriptions and resources under your whole organization. Here you can apply multiple policies and aggregate policy states with the policy initiative. You can also define an exclusion scope here.

- Perform Remediation: Azure policies can be used for the real time remediation of your resources or the existing resources in your management group. You can also use the policies to remediate the resources which are not compliant with the policies.

- Exercise Governance: Azure policies can be used to exercise or implement the governance tasks in the environment. These consists of tasks like the policy assignment to multiple engineering teams, while managing multiple subscriptions. This also helps in the standardization and enforcing of the cloud resources configurations across the organization, under the management group where you need to enforce the compliance, cost control, security and design consistency.

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