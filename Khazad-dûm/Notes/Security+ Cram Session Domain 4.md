12-22-2024 22:31

Tags: [[Security]] [[CompTIA]] [[Fundamentals]]

# Security+ Cram Session Domain 4

## Attack Types

### Remote Access Trojan

- Malware posing as software that gets downloaded onto a device. This is typically downloaded onto the device via social engineering. Once the software has been installed, it gives the attacker full remote access control of the device on both hardware and software. 

## Encryption 

### Hashes

- It is a digital fingerprint that represents data that is being stored elsewhere. 
- You cannot recreate the data if all you have is a hash. (person/fingerprint analogy)
- Hashes are used for verification of data. Hashes must match to validate data. If they do not match, the data has been tampered with.
### Hashing for Provenance

- Hashing is a crucial component in establishing provenance.
- **Provenance** refers to the record of ownership, history, and authenticity of an asset. Hashing helps ensure the integrity and immutability of this record by creating a unique digital fingerprint for each asset.

### Encryption

- Encryption protects data at rest and data in transit. Converts data into strings of unintelligible text. 
#### Encrypting stored data

- Protecting data on storage devices, Full-disk and partition/volume encryption (**Ex.** Bitlocker, FileVault)
- File encryption (**Ex.** EFS on Windows)
#### Database Encryption 

- Protecting stored data using transparent encryption. 
	- Encrypt all database information with a symmetric key.
- Record-level encryption 
	- Encrypts individual columns
	- Use symmetric keys for each column
#### Transport Encryption

- Protecting data traversing the network
- Encrypting in the application 
	- Browsers can communicate via HTTPS
- VPN (Virtual Private Network)
	- Encrypts all data transmitted over the network, regardless of application 
	- Client-based VPN using SSL/TLS
	- Site-to-Site VPN using IPsec

#### Encryption Algorithms

- There are many, many different ways to encrypt data
	- The proper "formula" must be used during both encryption and decryption. 
- There are different use cases for encryption algorithms and each have their advantages and their disadvantages. (**Ex.** Security level, speed, complexity, implementation)

#### Cryptographic Keys

- The key determines the output
	- Encrypting data
	- Hash value
	- Digital Signature

##### Key Stretching

- You can make a weak key much stronger by performing multiple processes (encrypting multiple times)
	- Hash a password. Hash the hash of the password. 
- Brute force attacks would require reversing each of the hashes. 


## Wireless Security

### Wired Equivalent Privacy (WEP)

- WEP is a deprecated security protocol for wireless networks, introduced in 1999 by the IEEE (Institute of Electrical and Electronics Engineers) as part of the 802.11 standard. Its primary goal was to provide data confidentiality comparable to a traditional wired network.
- Earliest wireless security protocol. 
- Was deprecated due to security vulnerabilities. 

### Wi-Fi Protected Access (WPA)

- Stronger and better than WEP. 
- Uses **TKIP** (Temporal Key Integrity Protocol)
- Is now outdated.

### Wi-Fi Protected Access 2 (WPA2)

- Provides stronger security than WPA (stronger encryption).
- Uses **AES** (Advanced Encryption Standard) over TKIP which was found to have vulnerabilities as well. AES is the strongest encryption method. 
- Adopted by the U.S. government for its robust security and encryption. 

### Wi-Fi Protected Access 3 (WPA3)

- Introduced in 2018. Provides newest security protocols. 
- Uses more robust authentication.

### Wi-Fi Protected Setup (WPS)

- Designed to make it as easy as possible for devices to join a secure wireless network. 
- WPS pin number can be easily cracked. 

### Access Control

- You can utilize MAC address filtering to allow only devices to join your network. 
- The security issue with this is that MAC addresses can be easily spoofed. 
- This is specifically wired devices.

## Digital Forensics

### Legal Hold

- A legal technique to preserve relevant information.
	- Prepare for impending litigation. 
	- Initiated by legal counsel. 
- You should hold necessary data when a lawsuit is likely.
- Separate repository for electronically stored information (ESI)
	- Many different sources and types
	- Unique workflow and retention requirements
- Ongoing preservation
	- Once notified, there's an ongoing obligation to preserve the data

### Chain of Custody

- This process maintains the integrity of data.
- Control evidence
	- Maintain integrity
- Everyone who contacts the evidence must have permission.
	- Use hashes and digital signatures
	- Avoid tampering using these methods
- Label and catalog everything
	- Digitally tag all items for ongoing documentation 
	- Seal and store

### Acquisition

- Obtain the data
	- Disk, RAM, firmware, Os files
- Some of the data may not be on a single system
	- Servers, network data, firewall logs
- For virtual systems, get a snapshot
	- Contains all files and information about a VM
- Look for any left-behind digital items
	- Artifacts
	- Log information, recycle bin, browser bookmarks, saved logins

### Reporting

- Document the findings
	- For internal use, legal proceedings
- Summary information
	- Overview of the security event
- Detailed explanation of data acquisition
	- Step-by-step
- The findings 
	- An analysis of the data
- Conclusion 
	- Professional results given the analysis

### Preservation

- Handling evidence
	- Isolate and protect the data
	- Analyze the data without alterations
- Manage the collection process
	- Work from copies
	- Manage the data collection from mobile devices
- Live collection has become an important skill
	- Data may be encrypted or difficult to collect after powering down
- Follow best practices to ensure admissibility of data in court 
	- What happens now affects the future

### E-discovery

- Electronic discovery 
	- Collect, prepare, review, interpret, and produce electronic documents
- E-discovery gathers data required by the legal process
	- Does generally involve analysis
	- There's no consideration on intent
- Works together with digital forensics 
	- The e-discovery process obtains a storage drive 
	- Data on the drive is smaller than expected
	- Forensic experts determine that data was deleted and attempt to recover the data

## Security Content Automation Protocol (SCAP)

- Many different security tools on the market
	- NGFWs, IPS, vulnerability scanners
	- They all have their way of of evaluating and dealing with a threat
- SCAP allows tools to identify and act on the same criteria. 
	- Validate the security configuration
	- Confirm patch installs 
	- Scan for breaches
### Using SCAP

- SCAP content can be shared between tools
	- Focused on configuration compliance 
	- Easily detect applications with known vulnerabilities
- Especially useful useful in large environments
	- Many different OS's and apps
- This specification standard enables automation between tools 
- Automation types
	- Ongoing monitoring
	- Notifications and alerting 
	- Remediation of non compliant systems
## References


