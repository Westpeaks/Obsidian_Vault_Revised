2024-05-15 10:48

Tags: [[Troubleshooting]] [[Network]]

# Atlassian Interview Questions Network Troubleshooting Commands

**Linux Commands:**

1. **ping**:
    
    - Command: `ping [hostname/IP]`
    - Purpose: Tests connectivity to a remote host by sending ICMP echo requests and waiting for ICMP echo replies.
    - Example: `ping google.com`
2. **traceroute/tracert**:
    
    - Command: `traceroute [hostname/IP]` (Linux), `tracert [hostname/IP]` (Windows)
    - Purpose: Traces the route packets take from your computer to a destination host, showing the IP addresses of intermediate routers.
    - Example: `traceroute google.com`
3. **netstat**:
    
    - Command: `netstat -an`
    - Purpose: Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
    - Example: `netstat -an`
4. **ifconfig/ip**:
    
    - Command: `ifconfig` (for older Linux distributions), `ip addr show` (for newer distributions)
    - Purpose: Displays information about network interfaces, including IP addresses, MAC addresses, and interface status.
    - Example: `ifconfig` or `ip addr show`
5. **arp**:
    
    - Command: `arp -a`
    - Purpose: Displays the ARP cache, which maps IP addresses to MAC addresses on the local network.
    - Example: `arp -a`
6. **dig/nslookup**:
    
    - Command: `dig [hostname]` (Linux), `nslookup [hostname]` (Windows)
    - Purpose: Performs DNS queries to retrieve information about domain names, such as IP addresses and DNS records.
    - Example: `dig google.com`

**PowerShell Commands:**

1. **Test-Connection**:
    
    - Command: `Test-Connection [hostname/IP]`
    - Purpose: Similar to the `ping` command in Linux, tests connectivity to a remote host by sending ICMP echo requests.
    - Example: `Test-Connection google.com`
2. **Test-NetConnection**:
    
    - Command: `Test-NetConnection [hostname/IP]`
    - Purpose: Tests network connectivity to a specified destination by performing various network layer checks (TCP, UDP, ICMP, etc.).
    - Example: `Test-NetConnection google.com`
3. **Get-NetIPAddress**:
    
    - Command: `Get-NetIPAddress`
    - Purpose: Retrieves information about IP addresses configured on network interfaces.
    - Example: `Get-NetIPAddress`
4. **Get-NetRoute**:
    
    - Command: `Get-NetRoute`
    - Purpose: Retrieves information about routing tables, including destination networks, gateways, and interface indexes.
    - Example: `Get-NetRoute`
5. **Resolve-DnsName**:
    
    - Command: `Resolve-DnsName [hostname]`
    - Purpose: Performs DNS resolution to retrieve information about domain names, such as IP addresses and DNS records.
    - Example: `Resolve-DnsName google.com`


## References


