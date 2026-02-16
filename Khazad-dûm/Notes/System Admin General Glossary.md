2024-06-26 16:31

Tags: [[System Administration]] [[Linux]]

# System Admin General Glossary

**Software Daemon** - a type of computer program that runs in the background, performing various tasks without direct interaction from the user.

***Ex.*** *Web server daemons such as Apache or Nginx, system management daemons such as Init*

**Systemd** - not a single daemon but a collection of programs, daemons, libraries, technologies, and kernel components that initialize when a system bootstraps or boots.  

**Systemctl** - systemctl is an all-purpose command for investigating the status of systemd and making changes to its configuration. Systemctl's first argument is typically a subcommand followed by subsequent arguments that are specific to that subcommand. 

***Ex.*** 
`systemctl list-unit-files --type=service`

## References

[Unix and Linux System Administration Handbook](https://mog.dog/files/SP2019/2017%20Nemeth%20Evi%20etal%20-%20UNIX%20and%20Linux%20System%20Administration%20Handbook%5B5thED%5D_Rell.pdf)
