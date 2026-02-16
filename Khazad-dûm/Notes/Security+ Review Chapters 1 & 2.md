2024-10-12 11:42

Tags: [[Security]] [[Fundamentals]] [[Review]] [[Cheat Sheet]]

# Security+ Review Chapters 1 & 2

### Understanding Core Security Goals

- **Confidentiality** is ensuring that data is only viewed by the intended viewers. Encryption is the best form of protection to ensure this. 
- **Integrity** is assuring that the data has not been modified or tampered with. Hashing is a common method of ensuring integrity. 
- **Availability** is ensuring that the data is available when it needs to be accessed. One of the most common goals in availability is removing single points of failure. Fault tolerance and redundancy are the most common ways to support high availability. 
- Systems scale up by improving and increasing hardware capabilities (Ex. storage, memory, processing). Systems scale out by adding additional nodes and servers. They scale down by removing these. 
- **Scalability** is the ability to scale up or scale out to handle increased workloads. This is done manually by admins. 
- **Elasticity** is the ability to handle scalability dynamically as the increased workload occurs. This is handled through cloud resources. 
- **Resiliency** methods help systems heal themselves or recover from faults with minimal downtime. 
- Organizations balance resource availability and security controls. Money and resources vs. security measures. 

### Introducing  Basic Risk Concepts

- **Risk** is the possibility of a threat exploiting a vulnerability and resulting in a loss or failure.
- A **threat** is any circumstance that has the potential to compromise **CIA**.
- A **vulnerability** is a weakness in hardware, software, or users that can result in a loss or failure. 
- **Risk mitigation** reduces risk by reducing the chance and impact of a threat exploiting a vulnerability. 
- **Security controls** utilize and encompass risk mitigation (Ex. antivirus software is a security control). One of the core jobs of a security professional is to select an effective set of security controls. 

### Understanding Security Controls

#### 4 Categories, 6 Types

- The four security-control categories are **managerial**, **operational**, **technical**, and **physical**. 
- Managerial controls are administrative and deal with risk and vulnerability. 
- **Operational controls** are focused on the day-to-day operations of an org (Ex. training, configuration management, change management).
- **Technical controls** use technology to reduce vulnerabilities (Ex. encryption, antivirus software, IDSs, firewalls, principal of least privilege).
- **Physical controls** are any controls that you can touch (Ex. cameras, lighting, barricades, signs, fences, access control vestibules).
- There are six control types, preventive, deterrent, detective, corrective, compensating, and directive.
- **Preventive controls** attempt to prevent security incidents. This could be anything that accomplishes this goal. 
- **Detective controls** attempt to detect when a vulnerability has been exploited. 
- **Deterrent controls** attempt to prevent incidents by discouraging threats (Ex. signs, locks, warning screens).
- **Corrective controls** attempt to reverse the impact of an incident after it has occurred.
- **Compensating controls** are alternative controls used when the use of a primary control is not feasible.
- **Directive controls** provide instruction to individuals to prevent incidents (Ex. training and testing). 

#### Access Control Process

- **Identification**, **authentication**, and **authorization** are the three access control processes. They function in that order. 

### Network Time Protocol

- **NTP** is used to synchronize system clocks with a centralized time source. 

## CH. 2 

### Exploring Authentication Management

- **Identification** occurs when a user professes an identity (Ex. username and password). 
- **Authentication** allows users to prove their identity by using credentials known to another entity (Ex. fingerprint, face scan).
- **Authorization** provides access based on the proven identity. Resources are granted after ID is proven. 
- **Accounting methods** track user activity and stores them in log. 
- **Four factors of Authentication** are something you know (username and password), something you have (token), something you are (biometrics), and somewhere you are (location ID).
- **Push notifications** are used for 2FA. Non-disruptive way to authenticate. 
- **Default password**s are a vulnerability and should be changed as soon as possible. 
- **False acceptance rate** identifies the percentage of times false acceptance occurs. 
- **False rejection rate** identifies the percentage of time a false rejection occurs. 
- **Crossover error rate** indicates the biometrics system's efficacy rate. 
- **Hashed One-Time Passwords** generate one-time passwords that do not expire until they are used. 
- **Time-Based One-Time Passwords** generate one-time passwords that will expire after a specific period of time. 
- **Single-factor authentication** uses one or more of the same factors of authentication (Ex. password and PIN)
- **Dual-factor authentication** uses two different factors to authenticate (Ex. token key and a PIN). 
- **Multi-factor authentication** uses two or more. 

### Managing Accounts

- **Privileged access management** (**PAM**) implements strict security controls over accounts with elevated privileges. This includes passwordless access, time limits in admin accounts, and logging all activity. 
- Admins should have two accounts, an admin and user account. escalated privilege should only be used when necessary to perform admin tasks. 
- **Time-based logins** prevent users from logging in and accessing resources during certain times of day. 
- An **account audit** audits user accounts and privileges to help enforce the least privilege principle. 
### Comparing Authentication Services

- **Single sign-on** (**SSO**) allows users to authenticate with a single user account and access multiple resources on a network.  
- SSO can provide a central authentication on the Internet with a federated database. A federated ID links users' creds from different networks and OSs. 
- **SAML** is an **XML**-based standard used to exchange authentication and authorization information between two parties. 
- **OAuth** allows authorization via another trusted account (Ex. Google, Paypal, Microsoft).

### Comparing Access Schemes 

- **Role-based access control** (**RBAC**) uses roles to grant access based on the access level that they need. This is usually reflected by jobs or groups. Orgs can plan for RBAC by using documentation such as a permissions matrix. 
- **Group-based privileges** are from RBAC. Admins can add multiple users to a group without having to assign individual permissions. 
- **Rule-based access control** (**rule-BAC**) is based on a set of approved instructions. Ex. Some rule-BAC implementations use rules that trigger when an attack occurs. 
- **Discretionary access control** (**DAC**) Discretionary access control (DAC) is a type of security access control that grants or restricts object access via an access policy determined by an object’s owner group and/or subjects. DACs are discretionary because the subject (owner) can transfer authenticated objects or information access to other users (Ex. File owned by original user).
- **Mandatory access control** (**MAC**) uses labels to identify objects (what will be secured) with subjects (users). It is often used when access needs to be restricted based on a need to know (Ex. Files marked top secret or confidential).
- **Attribute-based access control** (**ABAC**) evaluates attributes and grants access based on attribute value. Used in **software-defined networks** (**SDN**s).


## References


