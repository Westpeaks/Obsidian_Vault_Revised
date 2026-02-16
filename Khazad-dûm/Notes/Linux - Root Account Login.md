03-13-2025 12:40

Tags: [[System Administration]] [[Linux]]

## Login

### Security Concerns with Root Access

- Much like everything within Linux is a file or a folder, Root is just another user. As such, most system will let you log into root directly. Due to security concerns, Ubuntu forbids it by default.
- Root logins have no log of what operations were performed when in the root role. 
- In essence whomever, is logged in as a root user is unable to be tracked. 
- It is generally a good idea to disable allowance of root logins on terminals, through window systems, and across the network (SSH). 
- If the root account does have a password (i.e. it has not been disabled), it needs to be a very secure password that is difficult to brute force. 

## References

[[Linux - Disable Root Login]]
[[Linux - SU Substitute User Identity]]
[[Linux - Sudo Limited SU]]

