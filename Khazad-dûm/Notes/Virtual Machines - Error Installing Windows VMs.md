03-10-2025 17:11

Tags: [[Virtualization]] [[Windows]]

## Error 

- When installing a Windows VM, the following error occurs: 

```Windows cannot read the ProductKey from the unattend answer file```

## Solution

1. Power of the VM machine
    
2. Go to the settings of your VM - System - Boot Order - **Uncheck Floppy**
    
3. Press OK
    
4. Go to the folder where your VM is stored (default is Home - VirtualBox VMs)
    
5. Delete any files that start with "Unattended"
    
6. Power on the VM machine
## References

[Error Installing Windows on VM](https://www.reddit.com/r/virtualbox/comments/1c1o605/error_installing_windows_windows_cannot_read_the/)

