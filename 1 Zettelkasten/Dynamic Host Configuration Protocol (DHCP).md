- Devices on a network cna ne assigned a static IP or a dynamic one. 
- **Static IPs** are assigned manually by a user. This process can be cumbersome in large networks.
- **Dynamic IPs** are assigned to a device from a DHCP server. 

- A **DHCP server** automatically assigns a device an: 
	- IP address
	- Subnet mask
	- Default gateway
	- DNS server

- A DHCP server can provide a limited number of IP addresses. The limited number is referred to as its **scope**. The range can be increased or decreased based in network needs. 
- IP addresses are provided by the server on a lease. This allows the server to utilize an IP address when not in use. 
- Devices will request the extension of their current lease when in use. 
- When configuring a static IP, DHCP servers can be configured to provide an address reservation. This reservation ensures that the same IP is assigned to the requested device (via MAC adress) everytime it connects or remains connected to the network. 

## Links:

[[How IP Addresses are Assigned]]