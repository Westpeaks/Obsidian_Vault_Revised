2024-08-24 22:34

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Network Fundamentals]] [[Network]]

# Security+ Chapter 4 Securing Your Network Cont.

## Using VPNs for Remote Access

### VPNs and VPN Concentrators

A virtual private network (**VPN**) provides remote access to a private network via a public network. VPN concentrators are dedicated devices used for VPNs. They include all the services needed to create a secure VPN supporting any clients. 

![[remotevpn.jpg]]

#### IPsec and Split Tunnel vs Full Tunnel

**IPsec** is a secure encryption protocol used with VPNs. **Encapsulating** **Security Protocol** (**ESP**) provides confidentiality, integrity, and authentication for VPN traffic. IPsec uses Tunnel mode for VPN traffic and can be identified with protocol 50 for ESP. It uses IKE over port 500. A full tunnel encrypts all traffic after a user has connected via a VPN. A split tunnel only encrypts traffic destined for the VPN's private network.  

### Network Access Control 

**Network access control** (**NAC**) includes methods to inspect connecting clients for health. This includes up-to-date antivirus software and can restrict access to unhealthy clients. You can use NAC for VPN clients and internal ones. 

### Authentication and Authorization Methods

#### Password Authentication Protocol and Challenge Handshake Authentication Protocol (PAP and CHAP)

PAP authentication uses a password but contains inherent weaknesses as the PAP sends information via plaintext. CHAP is more secure because it encrypts the data traveling over the network. 

#### Remote Authentication Dial-In User Service and Terminal Access Controller Access-Control System Plus (RADIUS and TACACS+) 

RADIUS and **TACACS+** provide centralized authentication, RADIUS only encrypts the password. It can be used with EAP to encrypt entire sessions. TACACS+ encrypts the entire session by default and can be used with Kerberos. 

## References


