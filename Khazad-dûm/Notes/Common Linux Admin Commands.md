12-28-2024 12:47

Tags: [[Linux]] [[System Administration]] [[Fundamentals]]

# Common Linux Admin Commands

## Linux Admin Commands
### 1. ls

The `ls` command lists files and directories in the current directory. Useful options include:

- `ls -l`: Shows detailed information including permissions, owner, size, and modification date.
- `ls -a`: Displays hidden files and directories.
- `ls -R`: Lists sub-directories recursively.

### 2. cd

The `cd` command is used to change the current working directory. Common usage includes:

- `cd /path/to/directory`: Changes to the specified directory.
- `cd ..`: Moves up one directory level.
- `cd ~`: Changes to the user's home directory.
- `cd -` Switches to the previous directory. This is a convenient feature that allows you to easily navigate back to the directory you were in before changing to a different one.

### 3. pwd

The `pwd` command prints the current working directory path, useful for confirming your location in the file system.

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


## References
