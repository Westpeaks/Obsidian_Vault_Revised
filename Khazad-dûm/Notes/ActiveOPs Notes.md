
## Linux Admin Commands
### 1. ls

The `ls` command lists files and directories in the current directory. Useful options include:

- `ls -l`: Shows detailed information including permissions, owner, size, and modification date.
- `ls -a`: Displays hidden files and directories.
- `ls -R`: Lists subdirectories recursively.

### 2. cd

The `cd` command is used to change the current working directory. Common usage includes:

- `cd /path/to/directory`: Changes to the specified directory.
- `cd ..`: Moves up one directory level.
- `cd ~`: Changes to the user's home directory.

### 3. pwd

The `pwd` command prints the current working directory path, useful for confirming your location in the filesystem.

### 4. mkdir

The `mkdir` command creates new directories. For example:

- `mkdir new_directory`: Creates a directory named "new_directory."
- `mkdir -p parent/child`: Creates nested directories.

### 5. rm

The `rm` command removes files and directories. Use with caution as deleted items cannot be easily recovered. Common usage:

- `rm file.txt`: Deletes a file.
- `rm -r directory`: Recursively deletes a directory and its contents.
- `rm -i file.txt`: Prompts for confirmation before deleting.

### 6. cp

The `cp` command copies files and directories. For example:

- `cp file.txt /path/to/destination`: Copies a file to a new location.
- `cp -r source_dir destination_dir`: Recursively copies a directory.

### 7. mv

The `mv` command moves or renames files and directories. Usage includes:

- `mv old_name.txt new_name.txt`: Renames a file.
- `mv file.txt /path/to/new_location`: Moves a file.

### 8. grep

The `grep` command searches for patterns in files or command output, powerful for text processing:

- `grep "pattern" file.txt`: Searches for "pattern" in file.txt.
- `command | grep "pattern"`: Filters command output for lines containing "pattern."

### 9. sudo

The `sudo` command allows users to run commands with superuser privileges, essential for tasks requiring elevated permissions.

### 10. systemctl

The `systemctl` command manages system services and is crucial for modern Linux distributions. Common usage:

- `systemctl start service_name`: Starts a service.
- `systemctl stop service_name`: Stops a service.
- `systemctl status service_name`: Checks the status of a service.

These commands are fundamental for effective Linux system administration and will enhance your ability to manage and troubleshoot Linux systems efficiently.

### 11. journalctl, sudo less /var/log/syslog, sudo cat /var/log/syslog

This allows you to view logs. 

`sudo journalctl -u service-name.service` for service-related logs. 

`sudo grep "error" /var/log/application.log` for application-specific logs. 


## Database SQL Commands

![[SQL CS.jpeg]]


## Common Networking Ports

1. **Port 80: HTTP (Hypertext Transfer Protocol)**
    
    - Used for unsecured web browsing.
    
2. **Port 443: HTTPS (Hypertext Transfer Protocol Secure)**
    
    - Used for secure web browsing.
    
3. **Port 21: FTP (File Transfer Protocol)**
    
    - Used for file transfers.
    
4. **Port 22: SSH (Secure Shell)**
    
    - Used for secure remote access and file transfers.
    
5. **Port 25: SMTP (Simple Mail Transfer Protocol)**
    
    - Used for sending email.
    
6. **Port 53: DNS (Domain Name System)**
    
    - Used for domain name resolution.
    
7. **Port 110: POP3 (Post Office Protocol version 3)**
    
    - Used for retrieving email.
    
8. **Port 143: IMAP (Internet Message Access Protocol)**
    
    - Used for retrieving email with more features than POP3.
    
9. **Port 3306: MySQL**
    
    - Used for MySQL database connections.
    
10. **Port 3389: RDP (Remote Desktop Protocol)**
    
    - Used for remote desktop connections to Windows machines.

## Leadership Qualities

### Serving and Teamwork

- The most important quality is supporting and serving your team. In a sense your team members become your clients. It is your responsibility to mentor where needed and foster team work. 
	- The times that I have seen support engineers fall off are when they became siloed and expectations become vague. 
	
- inter-department collaboration is key. The same must apply to the larger team. 
- Ex. Fostering teamwork at Zoom and Onspring even with difficult team members and low performers. 
- You have to be willing to do whatever you are asking others to do and then more. The team you work with will emulate what they see you doing and the passion and excellence you show. 
- You have to determine and nurture talent within your team. This includes providing development opportunities. 
- Also, be authentic but stay positive. Your attitude will wear off on your team. 

### Implementing Efficiency

- Processes and guidelines have to be in place for success. 
- Documentation and Knowledge bases are keys for success. 
	a. Zoom Knowledge base
	b. Illuminate development of metrics, implementation of Jira and documentation (Processes and knowledge base). Generation of data to provide KPIs and metrics. Support retros for introspection and improvements. 

### Resiliency and Priority

- You are the front line of customer care. Customer care affects all aspects of business. 
- It is leadership's responsibility to maintain priority of customer care. You must keep track of priority of issues and clients. You have to fight for customers in certain cases. 
- You are the bridge between customers and the technical team. You are the liaison between those two worlds. You have to help handle the hardest customers and cases or support your team through it. 

### Accountability

- There has to be a set standard for performance. This includes more than KPIs. 
- Metrics to drive improvement. 
- Taking responsibility. You are ultimately accountable for your team. 

## Questions 

1. What is the culture of the support team? 
2. What are the things you wish support could do? 
3. What is the measure of success for support within the organization?
4. What does services hope support can do moving forward? 