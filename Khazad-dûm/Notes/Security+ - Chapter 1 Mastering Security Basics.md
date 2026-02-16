2024-07-30 18:09

Tags: [[Security]] [[CompTIA]] [[Fundamentals]]

# Security+ - Chapter 1 Mastering Security Basics

## Understanding Core Security Goals

![[cyber-triad-1.png|300]]

#### Confidentiality 
Prevents unauthorized disclosure of information.

#### Integrity
Prevents unauthorized of information or systems. 

#### Availability 
Ensures authorized users can access information and systems when they need to. 

> [!Remember]
> The CIA triad is the foundation of cybersecurity. It is one of the essential concepts for the Security+ exam. Security threats and controls should be related back to one or more of the three goals. 

#### Confidentiality 
Confidentiality ensures that the data is only viewable by authorized users. The best way to protect confidential data is to encrypt it (**Ex.** E2EE). Access controls help protect confidentiality by restricting access (**Ex.** User and password, 2FA).

#### Integrity
Integrity verifies if the data has not been modified. Loss of integrity can occur through unauthorized or unintended changes. Hashing algorithms (**Ex.** SHA) calculate hashes to verify integrity. A **hash** in an alphanumeric string created by applying a hashing algorithm to a file or message. Hashes can be compared to ensure integrity. If hashes are the same between the sender and receiver, the data is unchanged. If the hash has changed, the data has been changed.

#### Availability
Availability ensures that systems are up and operational when needed and often addresses single points of failure. You can increase availability by adding fault tolerance and redundancies.

**Redundancy and Fault Tolerance**
Redundancy and fault tolerance methods increase the availability of systems and data. Scability refers to manually adding servers to a service or resources to a system to meet new demand. Elasticity refers to being able to do this automatically. 

## Introducing Basic Risk Concepts

#### Threat
A threat is any circumstance or event that has the ability to compromise CIA (confidentiality, integrity, and availability).

#### Vulnerability
A vulnerability is any point of weakness. A weakness can be software, hardware, configuration, and even users operating the system. 

#### Security Incident
A security incident (SI) is an adverse event or series that negatively affects the **CIA** of an organization's information technology (**IT**).

> [!Remember]
> Risk is the likelihood that a threat will exploit a vulnerability. **Risk Mitigation** reduces the chances that a threat will exploit a vulnerability or reduces the risk's impact by implementing **security controls**. 

## Selecting Effective Security Controls
Every Control you encounter will belong to at least one category and at least one type of control. **Ex.** A firewall is a technical control because it uses technology. It is also a preventative control because it can stop unwanted traffic from entering the network. 
 ![[Screenshot 2024-08-19 at 7.40.03 PM.png]]
### Control Categories
A control category describes how a control works.
#### Technical Controls
Technical controls use technology such as software, hardware, and firmware to reduce vulnerabilities. (**Ex.** Encryption, Antivirus software, Intrusion Detection and Prevention Systems, Firewalls)

#### Managerial Controls
Managerial controls are administrative in function and documented in security policies. (**Ex.** Risk and Vulnerability assessments)

#### Operational Controls
Operational controls are implemented by people who perform the day-to-day operations to comply with an organization's overall security plan. These controls are implemented by people. (**Ex.** Training, Configuration management, Media Protection)

#### Physical Controls 
Physical controls are controls that you can physically touch. (**EX.** barricades, lighting, signs, fences, sensors)

### Control Types
A control type describes the goal of the control. 
#### Preventive Controls
Preventive or Preventative controls attempt to prevent security incidents. Hardening systems modifies the configuration to increase security. Security guards can prevent unwanted access to secure areas. Change management can ensure configuration changes do not cause an outage. Account disablement ensure that accounts a disabled when an individual leaves an organization. (**Ex.** Hardening, Training, Security Guards, Account Disablement Process, Intrusion Prevention System (IPS)) 

#### Deterrent Controls
Deterrent controls attempt to discourage a threat. These can also work a a preventative control. (**Ex.** Warnings Signs, Login Banners, Security Guards)

#### Detective Controls
Detective controls attempt to detect when vulnerabilities have been exploited resulting in an SI. Detective controls discover an event after it has occurred. (**Ex.** Log Monitoring, Security Information and Event Management Systems (SIEM), Security Audit, Video Surveillance, Motion Detection, Intrusion Detection System (IDS))

#### Corrective Controls
Corrective controls attempt to reverse the impact of an incident. Their purpose is to restore previous functionality as quickly as possible after an incident takes place. They restore the CIA that was affected by the incident. (**Ex.** Backups and System Recovery, Incident Handling Process)

#### Compensating Controls
Compensating controls are used as alternative controls instead of a primary control. Their purpose is to still provide a strong option of authentication. (**Ex.** Time-Based One-Time Password used for a new employee instead of a smart card)

#### Directive Controls
Directive controls are providing instruction to individuals on how they should handle security-related situations and incidents. They are generally written documents that provide instruction. (**Ex.** Policies, Standards, Procedures, Guidelines, and Change Management)

### Encryption

A technical-preventative control would be encryption. Encryption is a tool that can be used to securely transmit data between individuals or devices. 

#### Hashing

Hashing in encryption is a process used to convert data of any size into a fixed-length string of characters, known as a hash value, through a mathematical algorithm called a hash function.

![[Hashing 1.png]]

When someone receives a hashed message, they cannot retrieve the original message from it. Instead, hashing is used to verify that the message has not been altered. For example, if two parties have the same hash function, they can independently hash the original message and compare the hash values. If the hash values match, it confirms that the message has not been tampered with during transmission.

To decode a hashed message for verification purposes, specific procedures are used, such as those involving cryptographic message functions in Windows applications. These procedures allow for the verification of the hash to ensure the integrity of the data, but they do not retrieve the original message.

![[HashingDataInteg.png]]
## References

https://getcertifiedgetahead.com

https://www.codecademy.com/resources/blog/what-is-hashing/

https://learn.microsoft.com/en-us/windows/win32/seccrypto/encoding-and-decoding-a-hashed-message