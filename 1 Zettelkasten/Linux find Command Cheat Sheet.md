## Basic Usage

```bash
find [path] [options] [expression]
```

Search for files and directories in a directory hierarchy.

## Basic Commands

### Simple searches

```bash
find .                    # List all files and directories in current directory
find /path/to/search      # List all files in specified path
find . -name "file.txt"   # Find file by exact name
find . -iname "file.txt"  # Find file by name (case-insensitive)
```

## Search by Name

### Exact and pattern matching

```bash
find . -name "filename.txt"           # Exact match
find . -name "*.txt"                  # All .txt files
find . -name "file*"                  # Files starting with "file"
find . -name "*backup*"               # Files containing "backup"
find . -iname "*.TXT"                 # Case-insensitive extension
```

### Wildcards

```bash
find . -name "file?.txt"              # ? matches single character
find . -name "test[123].txt"          # Matches test1, test2, test3
find . -name "*[!backup]*"            # Files NOT containing "backup"
```

## Search by Type

```bash
find . -type f            # Files only
find . -type d            # Directories only
find . -type l            # Symbolic links only
find . -type b            # Block devices
find . -type c            # Character devices
find . -type p            # Named pipes (FIFOs)
find . -type s            # Sockets
```

## Search by Size

```bash
find . -size 100c         # Exactly 100 bytes
find . -size +100k        # Larger than 100 KB
find . -size -100M        # Smaller than 100 MB
find . -size +1G          # Larger than 1 GB
find . -size 0            # Empty files
```

### Size units

- `c` - bytes
- `k` - kilobytes (1024 bytes)
- `M` - megabytes (1024 KB)
- `G` - gigabytes (1024 MB)

## Search by Time

### Modification time (-mtime)

```bash
find . -mtime 0           # Modified in last 24 hours
find . -mtime -7          # Modified in last 7 days
find . -mtime +30         # Modified more than 30 days ago
find . -mtime 3           # Modified exactly 3 days ago
```

### Access time (-atime)

```bash
find . -atime -1          # Accessed in last 24 hours
find . -atime +90         # Not accessed in 90+ days
```

### Change time (-ctime)

```bash
find . -ctime -1          # Metadata changed in last 24 hours
```

### Minute-based times

```bash
find . -mmin -60          # Modified in last 60 minutes
find . -mmin +120         # Modified more than 120 minutes ago
find . -amin -30          # Accessed in last 30 minutes
```

### Newer/older than reference file

```bash
find . -newer reference.txt           # Modified after reference.txt
find . -newer reference.txt -type f   # Files modified after reference
find . ! -newer reference.txt         # Modified before reference
```

## Search by Permissions

```bash
find . -perm 644          # Exact permission match
find . -perm -644         # At least these permissions
find . -perm /644         # Any of these permissions
find . -perm /u+w         # User has write permission
find . -perm -g+w         # Group has write permission
find . -executable        # Executable files
find . -readable          # Readable files
find . -writable          # Writable files
```

## Search by Owner

```bash
find . -user username     # Files owned by user
find . -group groupname   # Files owned by group
find . -uid 1000          # Files with specific UID
find . -gid 1000          # Files with specific GID
find . -nouser            # Files with no valid user
find . -nogroup           # Files with no valid group
```

## Combining Conditions

### AND (default)

```bash
find . -name "*.txt" -size +1M        # .txt files AND larger than 1MB
find . -type f -mtime -7              # Files AND modified in last 7 days
```

### OR

```bash
find . -name "*.txt" -o -name "*.pdf"             # .txt OR .pdf files
find . \( -name "*.txt" -o -name "*.pdf" \)       # Grouped OR
```

### NOT

```bash
find . ! -name "*.txt"                # NOT .txt files
find . -not -name "*.log"             # Same as above
find . -type f ! -name "*.git*"       # Files NOT matching pattern
```

### Complex combinations

```bash
# .txt OR .pdf files, modified in last 7 days
find . \( -name "*.txt" -o -name "*.pdf" \) -mtime -7

# Files larger than 1MB but NOT .log files
find . -type f -size +1M ! -name "*.log"
```

## Depth Control

```bash
find . -maxdepth 1        # Current directory only (no subdirectories)
find . -maxdepth 2        # Current directory + 1 level of subdirs
find . -mindepth 2        # Start searching 2 levels deep
find . -mindepth 2 -maxdepth 3    # Search only levels 2-3
```

## Actions

### Print results (default)

```bash
find . -name "*.txt"      # Prints full path (default -print)
find . -name "*.txt" -print       # Explicit print
find . -name "*.txt" -printf "%f\n"   # Print filename only
```

### Execute commands

```bash
find . -name "*.txt" -exec cat {} \;              # Execute command on each file
find . -name "*.txt" -exec rm {} \;               # Delete each file
find . -name "*.txt" -exec chmod 644 {} \;        # Change permissions
find . -name "*.txt" -exec mv {} /backup/ \;      # Move files
```

### Execute with confirmation

```bash
find . -name "*.txt" -ok rm {} \;                 # Prompt before each execution
```

### Execute with optimization

```bash
find . -name "*.txt" -exec cat {} +               # Pass multiple files at once
find . -name "*.txt" -exec rm {} +                # More efficient batch deletion
```

### Delete files

```bash
find . -name "*.tmp" -delete          # Delete files directly (faster than -exec rm)
```

## Practical Examples

### Find and delete

```bash
# Delete .tmp files older than 7 days
find . -name "*.tmp" -mtime +7 -delete

# Delete empty files
find . -type f -empty -delete

# Delete empty directories
find . -type d -empty -delete
```

### Find large files

```bash
# Files larger than 100MB
find . -type f -size +100M

# Top 10 largest files
find . -type f -exec ls -lh {} \; | sort -k5 -hr | head -10

# Or using printf
find . -type f -printf "%s %p\n" | sort -nr | head -10
```

### Find and copy

```bash
# Copy all .txt files to backup directory
find . -name "*.txt" -exec cp {} /backup/ \;

# Copy with directory structure
find . -name "*.txt" -exec cp --parents {} /backup/ \;
```

### Find and compress

```bash
# Create archive of all .log files
find . -name "*.log" -exec tar -czf logs.tar.gz {} +

# Compress files individually
find . -name "*.txt" -exec gzip {} \;
```

### Find duplicate files

```bash
# Find duplicate filenames
find . -type f -printf "%f\n" | sort | uniq -d

# Find files with same size
find . -type f -printf "%s %p\n" | sort -n
```

### Find by content

```bash
# Find files containing specific text (combined with grep)
find . -type f -name "*.txt" -exec grep -l "search_text" {} \;

# Find and replace text in files
find . -type f -name "*.txt" -exec sed -i 's/old/new/g' {} \;
```

### Find recently modified files

```bash
# Files modified today
find . -type f -mtime 0

# Files modified in last hour
find . -type f -mmin -60

# Most recently modified file
find . -type f -printf '%T+ %p\n' | sort -r | head -1
```

### Find files by extension

```bash
# All image files
find . -type f \( -name "*.jpg" -o -name "*.png" -o -name "*.gif" \)

# All code files
find . -type f \( -name "*.py" -o -name "*.js" -o -name "*.java" \)
```

### Clean up old files

```bash
# Delete log files older than 30 days
find /var/log -name "*.log" -mtime +30 -delete

# Delete cache files older than 7 days
find ~/.cache -type f -mtime +7 -delete
```

## Advanced Usage

### Use with xargs (more efficient)

```bash
find . -name "*.txt" | xargs cat                  # Better for many files
find . -name "*.txt" -print0 | xargs -0 rm        # Handle filenames with spaces
find . -type f -print0 | xargs -0 grep "search"   # Search within files
```

### Count results

```bash
find . -name "*.txt" | wc -l                      # Count matching files
```

### Exclude directories

```bash
find . -path ./node_modules -prune -o -name "*.js" -print
find . -not -path "*/node_modules/*" -name "*.js"
find . -path ./git -prune -o -type f -print
```

### Find broken symbolic links

```bash
find . -type l ! -exec test -e {} \; -print
find . -xtype l                                   # Simpler alternative
```

### Custom output format

```bash
find . -type f -printf "%p\t%s\t%TY-%Tm-%Td\n"   # Path, size, date
find . -type f -printf "%f\n"                     # Filename only
find . -type f -printf "%h\n" | sort -u           # Directories only
```

## Quick Reference Table

|Option|Description|
|---|---|
|`-name`|Search by filename (case-sensitive)|
|`-iname`|Search by filename (case-insensitive)|
|`-type f`|Files only|
|`-type d`|Directories only|
|`-size +10M`|Larger than 10MB|
|`-mtime -7`|Modified in last 7 days|
|`-mmin -60`|Modified in last 60 minutes|
|`-user`|By owner|
|`-perm`|By permissions|
|`-maxdepth`|Limit directory depth|
|`-exec`|Execute command on results|
|`-delete`|Delete found files|
|`-o`|OR operator|
|`-not` or `!`|NOT operator|

## Common Patterns

```bash
# Find all hidden files
find . -name ".*"

# Find world-writable files (security check)
find . -type f -perm -002

# Find SUID/SGID files (security check)
find / -perm /6000 -type f

# Find files with no owner
find / -nouser -o -nogroup

# Find core dump files
find / -name core -type f

# Find configuration files
find /etc -name "*.conf"

# Find recently installed packages (logs)
find /var/log -name "*.log" -mtime -1
```

## Performance Tips

1. **Specify path**: Use specific paths instead of searching from root
2. **Use -maxdepth**: Limit search depth when possible
3. **Type first**: Put `-type` early in the expression
4. **Use -delete**: Faster than `-exec rm`
5. **Use -print0 with xargs -0**: For filenames with spaces
6. **Avoid -exec for large results**: Use `xargs` instead
7. **Use locate**: For simple name searches (faster, uses database)

## Notes

- `find` is recursive by default
- Expressions are evaluated left to right
- `-name` is case-sensitive, `-iname` is not
- Use quotes around patterns to prevent shell expansion
- `{}` in `-exec` is replaced with the filename
- `\;` ends the `-exec` command (for each file)
- `+` at the end passes multiple files to one command
- `find` doesn't follow symbolic links by default (use `-L` to follow)


## Links:

20260129