2024-08-10 14:03

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[User Identity and Access]]

# Security+ - Chapter 2 Understanding Identity and Access Management Cont.

## Comparing Authentication Services

### Single Sign On (SSO)
#### SAML
**SAML** is an XML-based standard to exchange authentication and authorization between two parties. SAML provides SSO for web-based applications.

SSO does not provide authorization. SAML and SSO can transfer authorization data between systems. 

### OAuth

OAuth is used to give authorization to certain data resources often between applications. The *Auth* in OAuth stands for authorization not aunthentication.

## Authorization Models

### Role-Based Access Control (role-BAC)

A role-BAC control scheme uses roles based on jobs and functions. A roles and permissions matrix is a planning document that summarizes the roles with the required privileges.

#### Access with Group-Based Privileges

Group-based privileges reduce the admin workload of access management. Admins can put users into security groups and add access privileges. Users will automatically inherit the privileges of that group once assigned.

### Rule-Based Access Control (rule-BAC)

Rule-BAC is based on a set of approved instructions such as an access control list (ACL). Some rule-BAC systems use rules that trigger a response based on an event (**Ex**. modifying ACLs after detecting an attack).  

### Discretionary Access Control 

The DAC scheme specifies that every object has an owner, and the owner has full, explicit control of the object. Microsoft NTFS uses the DAC scheme.

### Mandatory Access Control

The MAC scheme uses sensitivity labels for users and data. It is commonly used when access is restricted on a need-to-know basis. Sensitivity labels often reflect classification levels of data and clearances granted to individuals

### Attribute-Based Access Control (ABAC)

The ABAC scheme uses attributes defined in policies to grant access to resources. It's commonly used in software-defined networks (SDNs).


## References


