12-13-2024 14:29

Tags: [[Security]] [[CompTIA]] [[Fundamentals]]

# Security+ Cram Session Domain 2

## Network Segmentation

There are several ways to look at segmentation

- **Mobile device management** - in a BYOD scenario, mobile app management will keep business and personal data separate. This can prevent business data leaking.
- **Endpoints** - segment devices that have become vulnerable could be placed in its own VLAN.  
- **Applications** - Within a private subnet, VLANs can be used to carry out segmentation and traffic for sensitive apps and data. 

## Access Control 

- **Mandatory Access Control** - access policy that is determined by the system, not the object owner. Relies on classification labels that are representative of security domains and realms. 
- **Discretionary Access Control** - permits the owner or creator of an object to control and define its accessibility, owner has full control by default. (Ex. owner owed file that is shared. NTFS file permissions on Windows.)
- **Non-Discretionary Access Control** - Enables the enforcement of system-wide restrictions that override object-specific access. 
- **Rule-Based Access Control** - Defines specific functions for access to requested objects based on rules. (Ex. Firewalls)
### Rule-Based Access Control

- Routers and firewalls use rules within access control lists (ACLs).
- These rules define what traffic is allowed into the network. 

### Role-Based Access Control

- Uses a well-defined collection of named job roles to give users specific permissions. 
- Aims to ensure the users who have roles can access what is needed to perform job. (Used in Windows and the cloud platforms.)

### Application Allow List

- Enables only explicit apps to run. (Firewalls, IDS/IPS, and EDR systems can have an allow list.)

### Application Deny List 

- Anything that is not denied will be allowed. Opposite of an allow list.  

### Isolation 

- Industrial Control Systems (ICS) /OT systems are typically completely isolated or "air gapped" because of their critical nature. 


## Encryption

### Hardware Root of Trust

A line of defense against executing unauthorized firmware on a system.

- When certificates are used in FDE, they use a hardware root of trust for key storage. 
- It verifies that the keys match before the secure boot process takes place. 
- It is supported by a Trusted Platform Module (TPM), which is an implementation of a hardware root of trust. 
- TPMs store and manage keys used for FDE. They provide the OS with access to keys. 

### Disk Encryption

**FDE** - Full Disk Encryption is built into Windows using Bitlocker. DMcrypt does this in Linux. 
Key are stored on the TPM. 

**SED** - Hardware-based encryption. The drive encrypts itself. 

### Protecting Data at Rest

**FDE "under the hood"**
TPM => Hardware root of trust

SEDs are solid state drives that self encrypt and are immune to a cold boot attack.

### Hardware Security Modules

- Hardware device (server or card) used in large environments.
	- Clusters, redundant power
	- Securely stores thousands of cryptographic keys.
- High-end cryptographic hardware
	- Plug-in card or separate hardware device
- Key backup
	- secure storage in hardware

## Monitoring Privileged Operations

#### Goal 
To ensure that trusted employees do not abuse the special privileges they are granted. 

### Log Monitoring 

- Logs from various systems, services and devices record details of activity on systems and networks. 
- It takes multiple logs to get a full view of a breach. 
- By monitoring these logs, it's possible to detect security iccidents. 
- Automated log monitoring can automatically detect and investigate potential incidents.
- Centralized logging has become the standard especially in the cloud. 

## SIEM and SOAR

### Security Information Event Management (SIEM)

- System that collects data from many other sources within the network. 
- Provide real-time monitoring, analysis, correlation and notification of risks. 
### Security Orchestration Automation and Response

- Centralized alert and response automation with threat-specific playbooks.
- Response may be fully automated or single-click. 

## Configuration and Change Management 

### Configuration Management 

- Ensures that that systems are configured similarly and that configs are documented. 
- **Baselining** ensures that systems are deployed with a common bassline. Imaging is universally used for this. 
- **Mobile Device Management (MDM)** - An MDM solution can be used to push config changes to mobile devices. (Ex. Min iOS/Android verisons, six digit pins, no rooted devices, app management)
- **Content Filtering / URL Filtering** - Blocking harmful content with filtering appliances like Unified Threat Management (UTM) or Next Gen Firewalls (NGFW)
- **Update or Revoke Certificates** - Certs facilitate authentication and secure connectivity. (Ex. TLS/HTTPS web, IPSec VPN connectivity).

### Change Management

- Helps reduce outages or weakened security from changes. 

## Hardening Techniques

Know these **4 types of endpoint protection** for the exam

### Antivirus Software

-  Scans endpoints for the presence of malware. (Ex. viruses, worms, trojans, etc.)
- WHen an infection is detected, it can generally remediate though quarantine or removal of detected malware. 
- Originally relied on AV signatures (known lists), but today relies on AI and threat intelligence for detection. 
### Endpoint Detection and Response (EDR)

- A security technology that focuses on detecting and responding to threats at the endpoint level.
- It often uses behavioral analysis techniques to identify suspicious activity and contain threats before they can cause damage at the endpoint. 
- Prevents unauthorized access, tampering, and attacks. 

### Extended Detection and Response (XDR)

- A next-generation security that goes beyond endpoint to include network devices, cloud infrastructure, and IoT devices.
- Provides a broader view of IT security and enables faster, more accurate threat detection and response. 

### Host Intrusion Prevention Systems (HIPS)

- Intrusion prevention on a single host. 
- Detects and eliminates threats on the host level. 
- Software-based. may be easier to disable. 

### Host-Based Firewall 
- Host-based and network-based firewalls are together for layered defense.

## References


