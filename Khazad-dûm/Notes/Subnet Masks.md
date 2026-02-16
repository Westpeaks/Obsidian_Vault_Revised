2024-05-16 20:55

Tags: [[Network]] [[Subnet Mask]]

# Subnet Masks

A subnet mask is a 32-bit number used in conjunction with an IP address to identify the network portion and the host portion of the address. It helps determine which part of an IP address belongs to the network and which part identifies individual hosts on that network.

Here are some key points about subnet masks:

1. **IPv4 Addressing**: In IPv4, an IP address is a 32-bit number represented in dotted-decimal notation (e.g., 192.168.1.1). The subnet mask is also a 32-bit number represented in the same format.
    
2. **Binary Representation**: Internally, both IP addresses and subnet masks are represented in binary format. Each bit in the subnet mask corresponds to a bit in the IP address, indicating whether that bit represents the network portion (1) or the host portion (0) of the address.
    
3. **Network and Host Portions**: The subnet mask divides the IP address into two parts: the network portion and the host portion. The network portion identifies the specific network to which the device belongs, while the host portion identifies individual devices on that network.
    
4. **Network Addressing**: When sending data over a network, devices use the network portion of the IP address and the subnet mask to determine whether the destination IP address is on the same network or a different network. If the destination IP address is on the same network, the data is sent directly to the destination; otherwise, it is forwarded to a router for further routing.
    
5. **Common Subnet Mask Values**: Common subnet mask values include:
    
    - 255.0.0.0 (/8) - Class A networks
    - 255.255.0.0 (/16) - Class B networks
    - 255.255.255.0 (/24) - Class C networks
6. **CIDR Notation**: Subnet masks are often expressed using Classless Inter-Domain Routing (CIDR) notation, which specifies the number of network bits in the mask (e.g., /24 indicates that the first 24 bits represent the network portion).
    

Understanding subnet masks is essential for network administrators and engineers when designing, configuring, and troubleshooting IP networks. They help ensure proper addressing and routing of network traffic within complex network environments.

- Every IP address has a subnet mask. 

- Subnets tell us how big a network is and how many IOP addresses are available. 

- Subnet masks can tell us many things about a network. For example, 

![[Screenshot 2024-05-16 at 8.59.24 PM.png]]
If the subnet mask starts with 255, then the starting IP address will always be 192. 

If you break the subnet mask into binary, the number of network bits (2^number of 0's) in the fourth octet can be calculated to tell us how many IP addresses the network can have. In this example, 256. 

## References

https://www.youtube.com/watch?v=oZGZRtaGyG8&t=54s&ab_channel=NetworkChuck
