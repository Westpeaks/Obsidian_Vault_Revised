2024-06-01 15:15

Tags: [[Khazad-dûm/Tags/Azure]] [[Fundamentals]] [[Cloud]] [[Engineering]]

# Azure Resource Manager Unit 6-10


## Reorganize Azure Resources Unit 6

- Sometimes you may need to move resources to either a new subscription or a new resource group in the same subscription.

![[move-resources-1ce2912e.png]]

- You can't add, update, or delete resources in the resource groups when the resources are being moved. They can still be used. 

### Implementation

- To move resources, select the resource group containing those resources, and then select the **Move** button. Select the resources to move and the destination resource group. Acknowledge that you need to update scripts.

![[move-resource-groups-aae58bce.png]]

## Remove resources and resource groups Unit 7

- Use caution when deleting a resource group. Deleting a resource group deletes all the resources contained within it. That resource group might contain resources that resources in other resource groups depend on.

### Powershell command for deleting resource groups

`Remove-AzResourceGroup -Name "ContosoRG01"`

### Removing Resources

- You can also delete individual resources within a resource group.

## Determine resource limits Unit 8

- Azure lets you view resource usage against limits. This is helpful to track current usage, and plan for future use.

![[check-resource-limits-4f522428.png]]

- The limits shown are the limits for your subscription.
- When you need to increase a default limit, there is a Request Increase link.
- All resources have a maximum limit listed in Azure [limits](https://learn.microsoft.com/en-us/azure/azure-subscription-service-limits?toc=%2fazure%2fnetworking%2ftoc.json).
- If you are at the maximum limit, the limit can't be increased.

## Knowledge Check Unit 9
![[Screenshot 2024-06-01 at 3.32.45 PM.png]]

## Summary Unit 10 

Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features, like access control, locks, and tags, to secure and organize your resources after deployment.

You should now be able to:

- Identify the features and usage cases for Azure Resource Manager.
- Describe each Azure Resource Manager component and its usage.
- Organize your Azure resources with resource groups.
- Apply Azure Resource Manager locks.
- Move Azure resources between groups, subscriptions, and regions.
- Remove resources and resource groups.
- Apply and track resource limits.

## References
https://learn.microsoft.com/en-us/training/modules/use-azure-resource-manager/

https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/move-support-resources

[Azure Resource Manager documentation](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)

[Learn - Control and organize Azure resources with Azure Resource Manager](https://learn.microsoft.com/en-us/training/modules/control-and-organize-with-azure-resource-manager/)

