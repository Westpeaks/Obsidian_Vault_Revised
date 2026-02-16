2024-08-20 23:43

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Network Fundamentals]] [[Network]]

# Security+ Chapter 4 Securing Your Network

## Exploring Advanced Security Devices

### Understanding Intrusion Detection Systems and Intrusion Prevention Systems

#### Host-Based Intrusion Detection System (HIDS)

A **HIDS** can monitor all traffic on a single host system (**Ex.** a server or workstation). In some cases, it can detect malicious activity better than antivirus software.

#### Network Intrusion Detection System 

A **NIDS** console is installed on network appliances and functions similarly to a HIDS. Sensors are installed on network devices (**Ex.** routers, switches) to monitor and detect network-based attacks. You use taps and port mirrors to capture traffic. It will not monitor encryption or individual hosts. 

![[NIDSHIDS.jpg]]

#### Detection Methods

##### Signature-Based Detection and Trend-Based Detection

Signature-based detection identifies issues on known attacks and vulnerabilities. Signature-based detection systems detect known attack types. Trend-based IDSs (also known as anomaly-based) can detect unusual activity.  They start with a performance baseline and compare that against network traffic to detect anomalies. 

##### SYN Flood Attack 

A **Synchronize** (**SYN**) flood attack is a common denial-of-service (**DoS**) attack One system sends a SYN packet. The second system responds with a SYN/ACK packet. The first system then completes the handshake (exchange) with an ACK packet. However, in a SYN flood attack the third ACK packet is never sent. This builds up and  and consumes resources on the second system and can in many cases cause it to crash. 

#### Alert Response and Validation

A false-positive incorrectly indicates an attack on a system is occurring. A high incidence of these increases an admin's workload. A false-negative is when an attack occurs and system fails to detect it. Admins often set the threshold high enough on an IDS (Intrusion Detection System) to minimize false-positives but low enough to detect false-negatives.

### IPS vs IDS

An intrusion prevention system (IPS) is a preventative control. It is placed in-line with network traffic and can prevent an attack. IPSs can monitor data streams, detect malicious content, and stop attacks.

![[NIPS.png]]

An IPS is placed in-line with the traffic and can detect, react to, and prevent attacks. An IDS monitors network traffic for an attack and reports when attacks occur. It is passive.

### Honey Pots, Nets, Files, and Tokens

Honey pots and honeynets attempt to deceive attackers and disrupt them. They divert attackers from live networks and allow security professionals to observe attack methodologies. Honey files work much the same but use files to attract attackers. Honeytokens are fake records inserted into a database used to detect data theft.

## Securing Wireless Networks

![https://www.cables-solutions.com/wp-content/uploads/2017/01/Wireless-Access-Point.jpg](https://www.cables-solutions.com/wp-content/uploads/2017/01/Wireless-Access-Point.jpg)

#### MAC Filtering

**MAC filtering** can restrict wireless network access to specific clients. However, an attacker can easily get around this filter by using a sniffer to get a list of MAC addresses on the network. They can then spoof the addresses and gain access.

### Site Surveys and Heat Maps

A site survey examines a wireless environment for potential issues. A heat map shows wireless coverage and dead spots. Wireless footprinting gives you a detailed view of wireless APs, hotspots, and dead spots. 

### Wireless Cryptographic Protocols

**Wifi Protected Access 2** - **PSK**  uses a pre-shared key (PSK) and does not provide individual authentication. Open mode does not provide any security. Enterprise mode is the most secure of standard encryption providing strong authentication. Enterprise mode uses an 802.1X server (implemented as a RADIUS server) to add authentication. 
#### WPA3 and Simultaneous Authentication of Equals

WPA2 supports CCMP (based on Advanced Encryption Standard) and replaced earlier wireless cryptographic protocols. WPA3 uses Simultaneous Authentication of Equals (SAE) instead of a pre-shared key (PSK) as used in WPA2. 

### Authentication Protocols and IEEE 802.1X Security

Enterprise mode requires an 802.1X server. EAP-FAST supports Protected Access Credentials (**PACs**) instead of certificates. PEAP and EAP-TTLS require a certificate on the 802.1X server. EAP-TLS uses TLS, but requires a cert on both the server and client devices. An 802.1X server provides port-based authentication ensuring that only authorized devices can connect to a network. 

![[802.1RADIUS 1.png]]

## Understanding Wireless Attacks

### Dissociation Attacks and WiFi-Protected Setup

A dissociation attack removes a wireless client from a wireless network, forcing the client to re-authenticate. **WPS** allows users to configure a wireless device without authentication. Instead, they enter an eight-digit PIN and press buttons on the device. A WPS attack guesses all possible pins until it finds the connecting pin. This makes the WPS method vulnerable to attacks. 

### Rogue Access Points

Rogue access points are often used to capture and exfiltrate data. An **Evil Twin** is a rogue access point that uses the same SSID or similar SSID to a legitimate access point on the network. A secure AP blocks users, but a rogue access point provides access to unauthorized users. 

### Bluetooth Attacks

Bluejacking is unauthorized sending of messages to a nearby Bluetooth device. Bluesnarfing is unauthorized access to, or information theft from a Bluetooth device. Ensuring that devices cannot be paired without manual user intervention prevents these attacks. 

Admins use war driving techniques as part of a wireless audit. A wireless audit checks a wireless signal footprint, power levels, antenna placement, and encryption of wireless traffic. Wireless audits using war driving can detect rogue access points and identify unauthorized users. War flying uses drones or planes. 

## References

[[Network Fundamentals]]


