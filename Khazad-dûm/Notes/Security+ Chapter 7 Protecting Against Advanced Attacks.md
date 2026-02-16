2024-09-13 23:15

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Security Attacks]] [[SQL]] [[Database]] [[LDAP]] [[System Administration]]

# Security+ Chapter 7 Protecting Against Advanced Attacks

## Identifying Network Attacks

### Denial of Service Attacks

A **Distributed Denial-of-Service** (**DDoS**) attack is an attack of multiple computers against a single target. DDoS attacks include sustained high network traffic and usage of memory and processor time resulting in resource exhaustion. Major variants of DDoS attacks include reflected attacks, which involve using third-party servers to redirect traffic to the target, and amplified attacks, which combine reflection techniques with amplification to generate an even greater volume of traffic at the target. 

### On-Path Attack 

An **On-Path** attack is a form of active eavesdropping. It captures data from between two computers in a session. When secure channels are used, the on-path system may use certificates that aren't issued by the CA and will generate cert warnings. SSH gives a warning if previously established keys have changed.

### DNS Attack

A DNS poisoning attack attempts to modify or corrupt DNS data. Pharming is also an attack on DNS, and it manipulates the DNS name resolution process. A main indicator of both attacks is that a user attempts to access a website and is directed to a different website. 

#### Domain Hijacking

In a domain hijacking attack, an attacker changes the domain of the owner without there permission. 

### Replay Attacks

Replay attacks capture data in a session to impersonate one of the parties. Time stamps, sequence numbers, and multi-factor authentication are effective counter measures against these attacks.

## Summarizing Secure Coding Concepts

### Input Validation

The lack of input validation is one of the most common security issues on web-based applications. Input validation verifies the validity of input data before the data is executed, and server-side validation is more secure than client-side validation. Input validation protects against many attacks (**Ex**. buffer overflow, SQL Injection, dynamic link library injection, and cross-site scripting).

### Proper Error Handling

Error and exception handling helps protect the OS's integrity and controls the errors shown to users. Apps should show generic error messages to users but log detailed information.

### Analyzing and Reviewing Code

Static code analysis examines code without it running. It is a manual review going through the code line by line. Dynamic code analysis checks the code while it is running. Fuzzing techniques send random strings of data to applications looking for vulnerabilities. 

### Secure Development Environment

A secure development environment includes multiple stages. Stages are completed in separate non-production environments. Quality assurance methods are used in each of the stages. 

### Database Concepts 

Attackers use SQL injection attacks to pass queries to back-end databases through web servers. Many SQL injection attacks use the code **' or 1=1** to trick the database server into providing information. Input validation techniques and stored procedures can prevent these attacks.

## Other Application Attacks

### Memory Vulnerabilities 

#### Buffer Overflow Attacks

Buffer overflow attacks occur when an application receives more data than it can handle or receives unexpected data that exposes system memory. Buffer overflow attacks often include NOP instructions (such as OX90) followed by malicious code. When successful, the attack causes the system to execute malicious code. Input validation can resolve this. 

## Automation and Orchestration for Secure Operations 

### Automation and Scripting Use Cases

The common use cases for automation and scripting in security operations are user provisioning, guardrails, security groups, ticket creation, escalation, enabling/disabling services and access, continuous integration and testing, and use of APIs to create integrations.

### Benefits of Automation and Scripting

The key benefits of automation and scripting insecurity operations include improved efficiency and time-saving, consistent enforcement of baselines, standardization infrastructure configurations, secure scaling, increased employee retention, faster reaction times, and serving as a workforce.

### Other Considerations

When implementing automation and scripting in security operations, it is essential to consider the potential complexity, cost single points of failure, technical debt, and ongoing supportability for success.
## References


