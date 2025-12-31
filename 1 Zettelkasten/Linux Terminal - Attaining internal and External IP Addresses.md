1. To attain an internal IP address on a device:
   ```bash
   ip addr
   ```
   - Look for a line starting with `inet` to identify your IPv4 address (e.g., 192.168.1.15) and `inet6` for IPv6 addresses.
   - You can also use `hostnet -i` for a quick display of only IP addresses.
   
2. To attain the external IP of a device:
   ```bash
   curl icanhazip.com
   ```
   

## Links:

[[How IP Addresses are Assigned]]

2025110558