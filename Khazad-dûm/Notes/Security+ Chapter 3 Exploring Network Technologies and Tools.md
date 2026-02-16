2024-08-13 16:53

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Network Fundamentals]] [[Network]]

# Security+ Chapter 3 Exploring Network Technologies and Tools

## Reviewing Basic Networking Concepts

### OSI Model (Open Systems Interconnection)

**OSI** is the theoretical way to describe all of the different activities that happen on a network. The model has seven layers. 

| 1   | Physical     | Please  |
| --- | ------------ | ------- |
| 2   | Data Link    | Do      |
| 3   | Network      | Not     |
| 4   | Transport    | Throw   |
| 5   | Session      | Sausage |
| 6   | Presentation | Pizza   |
| 7   | Application  | Away    |
### Basic Networking Protocols
#### Data in Transit Use Cases

##### SSL vs. TLS

**SSL** (Secure Sockets Layer) has been compromised and is not recommended for use. This is due to vulnerabilities in the protocol that are not maintained or patched. **TLS** (Transport Layer Security) is the recommended replacement. TLS was designed so that in almost any implementation that previously used SSL.
##### SSH, TLS, SFTP, and FTP Secure

Secure Shell (**SSH**) encrypts traffic over TCP port 22 and is used to transfer encrypted files over a network. TLS is a replacement for SSL and is used to encrypt many different protocols, including browser-based connections using HTTPS. Secure File Transfer Protocol (**SFTP**) uses SSH to encrypt traffic. FTP Secure (**FTPS**) uses TLS to encrypt traffic.

##### Simple Management Network Protocol (SNMPv3)

SNMP v3 is a secure protocol that collects information and monitors network devices. It includes strong authentication mechanisms to protect the confidentiality of credentials. 

#### Email and Web Use Cases
##### SMTP, POP3 and IMAP4

All of these are primary email protocols. Here is a list of well-known ports for each:

| **Protocol**                             | **Common Port**                           |
| ---------------------------------------- | ----------------------------------------- |
| Simple Mail Transfer Protocol (SMTP)     | TCP port 25, Port 587 adds TLS Encryption |
| Post Office Protocol (POP3)              | TCP 110 and 995                           |
| Internet Message Access Protocol (IMAP4) | TCP 143 and 993                           |
| Hypertext Transfer Protocol (HTTP)       | TCP port 80 and 443 for HTTPS             |
#### Directory Use Cases

Directory services, such as Microsoft Active Directory Domain Service (**AD DS**), provide authentication and authorization for a network. AD DS uses LDAP, encrypted with TLS when querying the directory. 

#### Remote Access Use Case

Admins connect to servers remotely using protocols such as SSH and RDP. In some cases, admins use Virtual Private Networks (**VPN**s) to connect to remote systems.  

##### OpenSSH

**OpenSSH** is a suite of tools that simplifies the use of SSH to connect to remote servers securely. The ssh-keygen command creates a public/private key pair , and the ssh-copy-id command copies the public key to a remote server. The private must remain private. 

#### Time Synchronization Use Case

##### Network Time Protocol (NTP)

**NTP** is the most commonly used protocol for time synchronization. It allows systems to synchronize their time to within tens of milliseconds.

### Understanding Basic Network Structure

#### Switches

##### Hardening Switches - Comparing Port and Ports

A physical port used by a network device, such as a switch or a router, is entirely different from a logical port (virtual). A logical port is a number embedded in a packet and identifies a specific service, service connection endpoint, process or protocol.

Port security includes disabling unused ports and limiting the number of MAC addresses per port. A more advanced implementation is to restrict each physical port to only a single specific MAC Address.

###### Broadcast Storm and Loop Prevention

Broadcast storm and loop prevention such as Tree Protocol (**STP**) and Rapid STP (**RSTP**) is necessary to protect against switching loop problems, such as connecting two physical ports of a switch. 

#### Routers
##### Hardening Routers 

Routers and stateless firewalls (or packet filtering firewalls) perform basic filtering with an access control list (**ACL**). ACLs identify what traffic is allowed and what traffic is blocked. ACLs can control traffic based on networks, subnets, IP addresses, ports, and some protocols. Implicit deny blocks all traffic unless specifically granted. Routers and firewalls use implicit deny.

#### Simple Network Management Protocol

Admins use **SNMPv3** to manage and monitor network devices, and SNMP uses UDP ports 161 and 162. SNMPv3 uses encryption when communicating across the network and is more secure than previous versions.

#### Firewalls

Host-based firewalls protect individual hosts on a network. Network-based firewalls run on dedicated hardware and protect an entire network. These should be used together to achieve a defense-in-depth approach to network security.

Firewalls use a deny any any, deny any, or a drop all statement at the end of the ACL to enforce an implicit deny strategy. The statement forces the firewall to block any traffic that wasn't previously allowed in the ACL. The implicit deny strategy provides a secure starting point for firewalls and routers. 

A stateless firewall blocks traffic using only an ACL. Stateful firewalls use ACLs as well but also consider the state of the packet within a session. Web application firewalls provide strong protection for web servers. They focus on web application attacks. 

## References


