
12-14-2024 15:38

Tags: [[Security]] [[CompTIA]] [[Fundamentals]]

# Security+ Cram Session Domain 3

## Logical Segmentation

### VLANs 

- Logically segment a local area network into sub networks.

### VPNs

- Creating an encrypted tunnel between devices or networks to pass traffic, using protocols like IPSec. 

### Virtual Routing and Forwarding

- Allows a single router or switch to function as multiple virtual routers or switches. 

- Subnets divide larger IP ranges into smaller ranges which routers can segment using access control lists (ACLs).

### Software Defined Networks (SDN)

- Supports IaC, CI/CD, and DevOps practices. Used in the cloud. 
- A network architecture approach that enables the network to be intelligently and centrally controlled using software. It has the capacity to reprogram the data plane at any time. Use cases include SD-LAN and SD-WAN. 
- Separating the control plane and the data plane opens up a number of security challenges. 
- SDN vulnerabilities can in man-in-the-middle attacks and denial of service (DoS). 

![[SDN2.png]]

## Modern Compute and Security

### Containerization 

A lightweight, granular, and portable way to package applications for multiple platforms.

- Reduces overhead of server virtualization by enabling containerized apps to run on a shared OS kernel.
- Many of the same issues occur as with server virtualization: isolation at host, process, network, and storage levels. 

## Methods of Securing Data

#### How is hashing different from encryption?

### Encryption 

- Encryption is a two-way function. What is encrypted can be decrypted with a proper key. 
	- **Common Uses** - Bulk data encryption (symmetric), secure transactions and digital signatures (asymmetric).
### Hashing

- A one-way function that scrambles plain text to produce a unique message digest. 
- Conversion of a string of characters into a shorter fixed-length value. 
	- **Common Uses** - File / data integrity verification, digital signature integrity/authenticity, password storage. 

## Incident Response

### Attack Response 
- Attackers perform reconnaissance to formulate an attack. 
- When an attack is performed, the time between its occurrence and detection is called the **Mean Time to Detect (MTTD)**.
- MTTD on average can be 200 days. 
- The **Mean Time to Remediate** can be an average of 90 days. 

#### What can be done to reduce these times? 

- To mitigate MTTD we can utilize threat hunting. 
- To mitigate MTTR, **Security Orchestration Automation Response (SOAR)** can be implemented. 
- SOAR automates response to threats that have been seen before.
- Orchestration can also be used to respond to first-of-a-kind events. 
- For both automated and manual responses, a SOAR playbook is implemented to assist in remediating the attack. A Security Playbook defines the roles, responsibilities, procedures, and tools required for each incident scenario.
- SOAR systems also use a SOAR runbook. A runbook is a predefined procedure that automates and orchestrates tasks and actions involved in incident response, such as data enrichment, threat containment, and sending notifications. Runbooks automate repetitive and manual tasks, reducing the workload of SOC analysts and improving response times.

#### Good SOAR System will have:

- Ticketing system that automates tickets based on alerts (Ex. alerts from an XDR)
- A good dashboard where an analyst can take actionable steps. 

### Extended Detection and Response (XDR)

- A centralized system to correlates, analyzes, investigates, and responds events that it receives from several systems. 
- It can receive data from several sources (Ex. EDR, NDR, SIEM, Threat analysis systems)
- It then correlates, analyzes, investigates, and responds to incidents that are discovered. 
- Response is handled through a SOAR. 
- XDR are designed to create a Single Pane of Glass (SPoG) system for a SOC analyst. 

### SIEM, SOAR, and XDR are all used to reduce times for detection and response to attacks. They are often used as alternatives to one another or are used together. 

- SIEM is primarily used for detection and lightweight response. 
- SOAR is used in the response. They manage alerts and streamline responses.
- XDR is the newest attempt to streamline and improve these processes. They are supposed to provide a comprehensive implementation for detection and response. 
## References


