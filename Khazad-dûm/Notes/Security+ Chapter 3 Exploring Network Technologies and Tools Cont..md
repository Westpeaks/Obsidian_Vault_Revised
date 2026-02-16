2024-08-17 18:35

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Network Fundamentals]] [[Network]]

# Security+ Chapter 3 Exploring Network Technologies and Tools Cont.

## Implementing Network Designs 

### Security Zones

#### Screened Subnet

A screened subnet (also called a **DMZ**) is a buffer zone between the internet and an internal network. It allows access to services while segmenting access to the internal network. Internet clients can access services hosted on servers in the screened subnet, but the screened subnet provides an extra layer of protection to the intranet (internal network).

![[sdn-dmz_network_architecture.png]]

**Note**: Systems that must bee accessed by the general public should always be placed on a screened subnet. This network is designed to be accessed by the public but can remain secure.
#### Network Address Translation Gateway

**NAT** translates public IP addresses into private IP addresses and private IP addresses back into public ones. A common form of NAT is Port Address Translation (**PAT**). Dynamic NAT uses multiple public IP addresses while static NAT uses one. 

#### Physical Isolation and Air Gaps

An air gap isolates one network from another by ensuring there is physical space between all systems and cables. 

#### Logical Separation and Segmentation

Within a network, **east-west** traffic refers to traffic between servers. Imagine looking at a network diagram of servers in a network. They usually show servers configured horizontally. In contrast, diagrams show clients above or below servers, and traffic between clients and servers is north and south.

##### Virtual Local Area Networks (VLAN)

**VLAN**s separate or segment traffic on physical networks. You can create multiple VLANs with a single switch.  A VLAN can logically group together or separate with regard to there physical location. VLANs are also used to separate traffic types. (**Ex.** voice traffic on one VLAN and data traffic on another)

### Network Appliances

#### Proxy Servers

##### Centralized vs. Agent-Based

Most organizations use centralized proxy servers. They sit on the network where they can intercept and analyze net user requests. It is also possible to perform content filtering using an agent-based method. The filter receives a policy from an org's centralized proxy server and then enforces it on the user's device at the device level. 

A proxy server forwards requests for services from a client. It provides caching to improve performance. Transparent proxy servers accept and forward requests without modifying them. Non-transparent proxy servers use URL filters to restrict access to certain sites. Both types can log user activity. 

### Unified Threat Management

A unified threat management (**UTM**) appliance combines multiple security controls into a single appliance. It can include URL filtering, malware inspection, and content inspection components. Many UTMs are also used to block Distributed Denial-of-Service (**DDoS**) attacks. 

### Jump Server

A jump server is placed between different security zones and provides secure access from devices in one zone to devices in another zone. It can provide access to devices in a screened subnet from an internal network. 

## Zero Trust 

Traditional networks set up security and authentication based on network location (intranet, extranet). Today, it is much more likely that major resources (such as the cloud) are located outside of the physical intranet of a company. **Zero Trust Network Access** (**ZTNA**) doesn't mean that nothing is trusted, but means that trusted decisions are not made based on network location, Instead, they are made based on implementing strong authentication systems and creating policy-driven access controls based on user identity.

![[zta-logical-components.webp]]

### Control Plane vs. Data Plane

The communications used to control and configure the actual network take place in the control plane. The **Policy Engine** determines whether to grant access based on the rules in place within the network. The **Policy Administrator** communicates the decisions made by the PE to the **Policy Enforcement Point**. It is important to note that the elements of the control plane exist completely on the control plane (and vice versa) and only communicate with data plane. 
## References

https://getcertifiedgetahead.com 
