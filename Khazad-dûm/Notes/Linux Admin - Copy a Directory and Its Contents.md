03-15-2025 22:30

Tags: [[System Administration]] [[Linux]]  


## Copying a Directory to a New Directory 

```cp -r source_folder destination_folder```

```-r```  This designator (r is for recursive) signifies all the contents of a directory and can be used with multiple commands.

## Copying a Directory to an Existing Directory

```cp -r source_folder/* existing_folder/```

## Copying a Directory to a Remote Server

```scp -r /path/to/source_folder username@remote_host:/path/to/destination_folder```

## References

[[Linux Admin -  Basic Commands for System Administration]]

