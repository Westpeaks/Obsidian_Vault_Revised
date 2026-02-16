2024-10-15 23:48

Tags: [[Security]] [[Fundamentals]] [[Review]] [[Cheat Sheet]]

# Security+ Review Chapters 3 & 4

### Reviewing Basic Networking Concepts

- The OSI Model describes network communications in 7 layers: Physical, Data Link, Network, Transport, Session, Presentation, and Application.
 - **Transmission Control Protocol** (**TCP**) is a connection-oriented protocol that provides delivery guaranteed. 
- **User Datagram Protocol** (**UDP**) is a connection protocol that provides "best effort" delivery. It is used for streaming. 
- **File Transfer Protocol** (**FTP**) is used to transfer files over networks. SSH encrypts Secure Copy and Secure FTP (SFTP). TLS encrypts FTPS.
- **HTTPS** encrypts browser-based traffic with TCP using port 443. 
- Directory services use **Lightweight Directory Access Protocol** (**LDAP**) over TCP port 389 or LDAP Secure (LDAPS) over TCP port 636.
- Admins commonly connect to servers via SSH. SSH encrypts the connection. 
- Admins also use **Remote Desktop Protocol** (**RDP**) to connect to remote systems graphically using port 3389 over TCP.
- **Network Time Protocol** (**NTP**) provides time synchronization services.  
- **Domain Name System** (**DNS**) provides domain resolution. A records are for IPv4 and AAAA for IPv6. MX records are for mail servers. DNS uses port 53/TCP and 53/UDP. 
- **Domain Name System Security Extensions** (**DNSSEC**) provides validation for DNS responses by adding a Resource Record Signature (RRSIG). The RRSIG provides data integrity and authentication and prevents poisoning attacks. 

### Understanding Basic Network Devices

- **Switches** connect a computer to a local network. They map media access control (MAC) addresses to physical ports. 
- Port security limits access to switch ports. This includes limiting the number of MAC addresses per port and disabling unused ports. 
- **Routers** connect networks to each other and direct traffic based on IP addresses. Routers (and firewalls) use rules within access control lists (ACLs) to allow or block traffic. 
- The **route command** is used to view and manipulate the routing table. 
- **Implicit deny** indicates that unless something is explicitly allowed, it is denied. It is the last rule in an ACL. 
- **Host-based firewalls** filter traffic in and out of individual hosts. 
- **Network-based firewalls** filter traffic in and out of a network. They are placed at the border of a network (between the internet and the internal network).
- **Stateless firewalls** control traffic between networks using an ACL. The ACL can block all major traffic just as a firewall would. 
- **Stateful firewalls** filter traffic based on the state of a packet within a session. 
- **Web application firewalls** (**WAF**) protect a web server against web application attacks. It is typically placed in a screened subnet and alerts admin of attack. 
- **Next-generation firewalls** (**NGFW**) perform deep packet inspection, analyzing traffic at the application layer. 
- **Fail-open** is setting on a security device to allow traffic to pass when the device fails. 
- **Fail-closed** is setting on a security that doesn't allow traffic when the device fails. 

### Implementing Network Designs

- **Screened subnets** provide an extra layer of security for servers that have access to the internet.
- **Intranets** are internal networks. People use them to communicate and share data. 
- **Extranets** are parts of a network that can be accessed externally by authorized entities.
- **Network Address Translation** (**NAT**) translate public IPs into private ones, private back to public, and hides IP addresses on the internal network from users on the internet. A NAT gateway is a device that implements a NAT. 
- An **air gap** provides a physical isolation for systems or networks. They are completely isolated by literal air.
- **Forward proxy servers** forward requests for services from a client. They can also log caches and user activity. 
- **Reverse proxy servers** accept traffic from the internet and forward it to internal web servers. The reverse proxy server is placed in the screened subnet and the other servers exist in the in the internal network. 
- A **Unified threat management** (**UTM**) security device includes multiple layers of protection (Ex. URL filters, content inspection, malware inspection, DDoS mitigation).
- **Jump servers** are placed in between security zones and provide secure access between zones. They are often used to manage devices in the screened subnet.
 
## References


