2024-08-30 16:36

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Network]] [[System Administration]] [[Cloud]]

# Security+ Chapter 5 Securing Hosts and Data Cont.

## Summarizing Cloud Concepts

### Cloud Delivery Models

Applications such as web-based email provided over the internet are **Software as a Service** (**Saas**) cloud-based technologies. **Platform as a Service** (**PaaS**) provides customers with a fully managed platform, including hardware, OSs, and limited apps. The vendor keeps the system up to date. **Infrastructure as a Service** (**IaaS**) provides customers with hardware in a self-managed platform. 

### Cloud Deployment Models

Public cloud services are available to the public. Private cloud services are only available to one organization. Two are more organizations with shared concerns or resources can share a community cloud. A hybrid cloud environment is a combination of two or more cloud deployment models.

### Managed Security Service Provider

A **Managed Security Service Provider** (**MSSP**) is a third-party vendor that provides security services to an organization. A **Managed Service Provider** (**MSP**) provides IT services an organization needs, including security services provided by an MSSP (you get both).

### Cloud Service Provider Responsibilities

The responsibility matrix shows how responsibilities are divided between the customer and the CSP for IaaS, PaaS, and Saas models. 

**IaaS** (**Infrastructure as a Service**) 

**PaaS** (**Platform as a Service**)

Saas (**Software as a Service**) 

![[CSPR.png]]

### Hardening Cloud Environments 

#### Cloud Based DLP

A **Cloud Based DLP** can enforce security policies for data stored in the cloud. It can prevent storing sensitive data such as **Personally Identifiable Information** (**PII**). It does this by alerting a security admin, blocking attempts to save data, or quarantining the data. 

#### Next-Generation Secure Web Gateway

A **Cloud Access Security Broker** (**CASB**) is a software tool or service deployed between a network and its cloud provider. It provides security by monitoring traffic and enforcing security policies. A **Next Generation Secure Web Gateway** (**SWG**) provides proxy services for traffic from clients to Internet sites, such as filtering URLs and scanning for malware. 

CASB - between the network and the cloud. 

SWG - between network and internet. Typically a cloud-based service

### Cloud Security Alliance

The **Cloud Security Alliance** (**CSA**) is a not-for-profit that promotes best practices related to the cloud. It is a member-based organization that is also volunteer-based working on research and other projects. 

## Deploying Mobile Devices Securely

### Mobile Device Deployment Models

**Corporate Owned, Personally Enabled** (**COPE**) devices are owned by an organization, but employees can use them for personal use. **Bring Your Own Device** (**BYOD**) policies allow employees to connect personal devices to the corporate network. **Choose Your Own Device** (**CYOD**) policies allow employees to choose from an approved list that employees purchase and use on the network. 

### Connection Methods and Receivers

#### Mobile Device Management

**Mobile Device Management** (**MDM**) tools help enforce security policies on mobile devices. This includes storage segmentation, containerization, and full device encryption to protect data. Containerization is useful when using the BYOD model. They also include strong authentication methods to prevent unauthorized access. 

**Remote Wipe** sends a signal to a lost or stolen device to erase all data. Geolocation uses **Global Positioning System** (**GPS**) and can help locate a lost or stolen device. Geofencing creates a virtual fence or geographic boundary and can be used to detect when a device is within that boundary. GPS tagging adds geographical data to files. Context-aware authentication uses multiple elements to authenticate a user and a mobile device. 

### Hardening Mobile Devices

#### Unauthorized Connections

Tethering and mobile hotspots allow services to access the Internet and bypass network security controls and policies. Wi-Fi Direct is a standard that allows devices to connect without a wireless access point or router. MDM can block access to tethering, mobile hotspots, or Wi-Fi direct access. 

## Exploring Embedded Systems

### ICS and SCADA Systems

A **Supervisory Control and Data Acquisition** (**SCADA**) system has embedded systems that control an **Industrial Control System** (**ICS**), such as one used in a power plant or water treatment facility. Embedded systems are also used for many special purposes (**Ex**. medical devices, cars, aircraft, and unmanned aerial vehicles (UAVs)).

### Embedded System Components

An Embedded system is any device that has a dedicated function and uses a computer system to perform that function. It includes any devices included in the **Internet of Things** (**IoT**) category, such as wearables and home automated systems. Some embedded systems use a **System on Chip** (**SoC**).

## References


