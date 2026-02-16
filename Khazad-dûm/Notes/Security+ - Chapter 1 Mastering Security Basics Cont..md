2024-07-31 19:50

Tags: [[Security]] [[CompTIA]] [[Fundamentals]]

# Security+ - Chapter 1 Mastering Security Basics Cont.

## Logging and Monitoring

Log Entries help admins and security investigators determine what happened, when, where, and who or what did it. 

### Operating System (OS) / Endpoint Logs
Every operating system provides the ability to generate and store log entries. These logs provide important information about what occurs on endpoint systems.
#### Windows Logs
Windows systems have several logs that record events on a Windows computer system. Primary Windows logs are: **Security log**, **System log**, **Application log**.
#### Linux Logs
Linux systems store logs in the */var/log/* directory. You can view logs using the system log viewer on Linux systems or the **cat** command from the terminal. 

**cat** command **Ex.**
`cat /var/log/auth.log`

Common Linux logs at */var/log/*: **syslog**, **messages**, **secure**.

### Network Logs
Network logs record traffic on the network. These logs are on a variety such as routers, firewalls, web servers, and network intrusion/prevention systems. (**Ex**. Firewall logs, IDS/IPS logs, Packet Captures)

### Application Logs
Some applications will store logs in system logs (**Ex.** Widows Application log). Many applications also manage their own log files. (**Ex**. Webservers typically host log requests to the web server for pages.)
#### Metadata 
Metadata is data that provides information about other data. Email and image files contain metadata that provides a significant amount of information. For a photo, it can be information such as location, date, and time.

### Centralized Logging and Monitoring
Checking all logs of systems , applications, and infrastructure can be quite challenging. A standard solution is to use a centralized system to collect log entries. This is where Security Information and Event Management (SIEM) systems come in.

#### SIEM Systems
SEIM systems provide a centralized solution for collecting, analyzing, and managing data from systems. 

## References
https://getcertifiedgetahead.com

