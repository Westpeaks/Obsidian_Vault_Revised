2024-08-27 14:51

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Network]] [[Virtualization]] [[System Administration]]

# Security+ Chapter 5 Securing Hosts and Data

## Virtualization

Virtualization allows multiple virtual servers to operate on a single physical server providing increased cybersecurity resilience and lower operating costs. Keeping systems up to date with current patches is the best protection from VM escape attacks.

## Implementing Secure Systems

### Using Master Images For Baseline Configurations

A master images provides secure starting points for systems. Admin sometimes create them with templates or with other tools to create secure baselines. They then use integrity measurements to discover when a system deviates from the baseline. 

### Patching and Patch Management

Patch management procedures ensure that the operating systems, applications, and firmware are up to date with current patches. This protects systems against vulnerabilities. Change Management is the process and accounting structure for handling modifications and upgrades. Change management exists to reduce risks in making changes to a system. The changes are documented and prevent unintended outages. 

### Application Allow and Block Lists

An application allow list is a list of authorized software that can be installed within an organization. Users are unable to install applications and software if it is not on the list. Application block lists function in the opposite way. They block certain apps and software to prevent users from installing and running whatever is on the list.

### Disk Encryption

Full disk encryption (FDE) protects all of the contents of a disk using encryption. This may be done with specialized software or come included in specialized hardware known self-encrpting drives (SED).

### Trusted Platform Module

A **Trusted Platform Module** (**TPM**) is a hardware chip that provides full encryption to disks and features a secure boot process and remote attestation. The endorsement key is a unique asymmetric key pair burned into the TPM chip that provides a hardware root of trust.

### Hardware Security Module

A **Hardware Security Module** (**HSM**) is a removable or external device that can generate, store, and manage keys used in asymmetric encryption. Many server-based apps use an HSM to protect keys. a microSD HSM is an HSM device installed on a microSD card and can be installed on any device with an appropriate slot. 

#### Symmetric vs Asymmetric Encryption

Symmetric encryption uses a single shared key.
- Encrypt and decrypt with the same key. 
- Because the key has to be shared it raises security concerns.
- It doesn't scale very well for the same reasons. 
- Symmetric encryption is still used semi-often because it is so fast and requires mush less overhead than asymmetric. It is often used in conjunction with asymmetric. 
Asymmetric encryption 
- Also referred to as public key cryptography. There are two keys.
- A private key and public key is used. Private keys are yours and should not be shared. The public key can be shared responsibly. 
- The public key allows people to send you encrypted information and only your private key can decrypt it. 

## Protecting Data

### Data Loss Prevention

Data exfiltration is the unauthorized transfer of data out of a network.**Data Loss Prevention** (**DLP**) techniques and technologies attempt to prevent this from happening. They can block USB devices and monitor outgoing network traffic.  

### Database Security

The primary methods of protecting the confidentiality of data is with encryption and strong access controls. Database column encryption protects individual fields within a database. Database field (column) protection protects sensitive data but doesn't waste valuable processing power encrypting data that isn't sensitive.
## References


