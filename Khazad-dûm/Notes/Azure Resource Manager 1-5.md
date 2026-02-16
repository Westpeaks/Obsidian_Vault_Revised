2024-05-30 23:40

Tags: [[Khazad-dûm/Tags/Azure]] [[Fundamentals]] [[Cloud]] [[Engineering]]

# Azure Resource Manager Units 1 & 2

## Learning objectives

In this module, you'll learn how to:

- Identify the features and usage cases for Azure Resource Manager.
- Describe each Azure Resource Manager component and its usage.
- Organize your Azure resources with resource groups.
- Apply Azure Resource Manager locks.
- Move Azure resources between groups, subscriptions, and regions.
- Remove resources and resource groups.
- Apply and track resource limits.

## Review

- The infrastructure for your application is typically made up of many components – maybe a virtual machine, storage account, and virtual network, or a web app, database, database server, and third-party services. These components are not separate entities, instead they are related and interdependent parts of a single entity. You want to deploy, manage, and monitor them as a group.

- Azure Resource Manager enables you to work with the resources in your solution as a group.
- Azure Resource Manager provides a consistent management layer to perform tasks through Azure PowerShell, Azure CLI, Azure portal, REST API, and client SDKs.

![[AzRM.png]]

- You can deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
- You can repeatedly deploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.


## Azure Resource Manager Unit 3

### A glossary of terms:

- **resource** - A manageable item that is available through Azure. Some common resources are a virtual machine, storage account, web app, database, and virtual network, but there are many more.
- **resource group** - A container that holds related resources for an Azure solution. The resource group can include all the resources for the solution, or only those resources that you want to manage as a group. You decide how you want to allocate resources to resource groups based on what makes the most sense for your organization.
- **resource provider** - A service that supplies the resources you can deploy and manage through Resource Manager. Each resource provider offers operations for working with the resources that are deployed. Some common resource providers are Microsoft.Compute, which supplies the virtual machine resource, Microsoft.Storage, which supplies the storage account resource, and Microsoft.Web, which supplies resources related to web apps.
- **template** - A JavaScript Object Notation (JSON) file that defines one or more resources to deploy to a resource group. It also defines the dependencies between the deployed resources. The template can be used to deploy the resources consistently and repeatedly.
- **declarative syntax** - Syntax that lets you state "Here is what I intend to create" without having to write the sequence of programming commands to create it. The Resource Manager template is an example of declarative syntax. In the file, you define the properties for the infrastructure to deploy to Azure.

## Resources and Resource Groups Unit 4

### Resource Groups

Resource Groups are at their simplest a logical collection of resources. There are a few rules for resource groups.

- Resources can only exist in one resource group.
- Resource Groups cannot be renamed.
- Resource Groups can have resources of many different types (services).
- Resource Groups can have resources from many different regions.

### Creating Resource Groups

There are some important factors to consider when defining your resource group:

- All the resources in your group should share the same lifecycle. You deploy, update, and delete them together. If one resource, such as a database server, needs to exist on a different deployment cycle it should be in another resource group.
- Each resource can only exist in one resource group.
- You can add or remove a resource to a resource group at any time.
- You can move a resource from one resource group to another group. Limitations do apply to [moving resources](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/move-support-resources).
- A resource group can contain resources that reside in different regions.
- A resource group can be used to scope access control for administrative actions.
- A resource can interact with resources in other resource groups. This interaction is common when the two resources are related but don't share the same lifecycle (for example, web apps connecting to a database).

## Azure Resource Manager Locks Unit 5

A common concern with resources provisioned in Azure is the ease with which they can be deleted. An over-zealous or careless administrator can accidentally erase months of work with a few steps. Resource Manager locks allow organizations to put a structure in place that prevents the accidental deletion of resources in Azure.

- You can associate the lock with a subscription, resource group, or resource.
- Locks are inherited by child resources.

There are two types of resource locks.

- **Read-Only locks**, which prevent any changes to the resource.
- **Delete locks**, which prevent deletion.

![[resource-manager-locks-853635fd.png]]
## References
https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/2-review-benefits

