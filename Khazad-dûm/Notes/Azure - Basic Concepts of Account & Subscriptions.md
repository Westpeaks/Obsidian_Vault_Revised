2024-07-06 23:00

Tags: [[Khazad-dûm/Tags/Azure]] [[Cloud]] [[Fundamentals]] [[DevOps]] 

# Azure - Basic Concepts of Account & Subscriptions

- ACCOUNT
- TENANT
- SUBSCRIPTION
- RESOURCE GROUP

### Account/User

**A person or a program**
- Person - i.e. Joe Smith - joe@example.com
	- User name, password, MFA
- App - Managed Identity
	- Represents a program or service

**The basis for authentication**
- More than one account can be the owner in a tenant 

### Tenant

A representation of an organization

Usually represented by a public domain name - i.e. example.com
Will be assigned to a domain if not specified - i.e. example.onmicrosoft.com
A dedicated instance of Azure AD
Every Azure account is part of at least one tenant

### Subscription

An agreement with Microsoft to use Azure services, and how you're going to pay for that.

All Azure resource usage gets billed to the payment method of the subscription
- Free subs
- Pay as you go
- Enterprise agreements

### Resource

An entity managed by Azure

**Expected:** 
Virtual machine, web app, storage account

**Unexpected:**
Public IP address, network interface card, network security group

- Accounts can be given read, update, and owner rights to resources

### Resource Group

A way of organizing resources in a subscription
Can be viewed as a folder structure
All resources must belong to only one resource group
Resource groups can be deleted (which deletes the resource inside)
A way to separating out projects, keeping unrelated things separate. 

## References

https://www.udemy.com/course/70533-azure/learn/lecture/21622852#overview

