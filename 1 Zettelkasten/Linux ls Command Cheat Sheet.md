## Basic Usage

```bash
ls [options] [file/directory]
```

List directory contents.

## Common Commands

### Basic listing

```bash
ls                        # List current directory
ls /path/to/directory     # List specific directory
ls file.txt               # Check if file exists
```

### Most used options

```bash
ls -l                     # Long format (detailed)
ls -a                     # Show all files (including hidden)
ls -h                     # Human-readable file sizes
ls -t                     # Sort by modification time (newest first)
ls -r                     # Reverse order
ls -S                     # Sort by file size (largest first)
ls -R                     # Recursive (list subdirectories)
```

## Common Combinations

```bash
ls -la                    # Long format with hidden files
ls -lh                    # Long format with human-readable sizes
ls -ltr                   # Long format, sorted by time, reversed (oldest first)
ls -lSh                   # Long format, sorted by size, human-readable
ls -latr                  # All files, long format, by time, reversed
ls -ld */                 # List only directories in long format
```

## Understanding Long Format (-l)

```
-rw-r--r-- 1 user group 4096 Jan 15 10:30 file.txt
│          │ │    │     │    │           └─ filename
│          │ │    │     │    └─ modification time
│          │ │    │     └─ file size (bytes)
│          │ │    └─ group owner
│          │ │─ user owner
│          └─ number of hard links
└─ permissions
```

### Permission format

```
- rw- r-- r--
│ │   │   │
│ │   │   └─ others (read)
│ │   └─ group (read)
│ └─ owner (read, write)
└─ file type (- = file, d = directory, l = link)
```

## Useful Options

### Display options

```bash
ls -1                     # One file per line
ls -m                     # Comma-separated list
ls -d */                  # List directories only
ls -F                     # Append indicator (*/=>@|)
ls -i                     # Show inode numbers
ls --color=auto           # Colorize output (usually default)
```

### Filtering and sorting

```bash
ls -t                     # Sort by modification time
ls -tu                    # Sort by access time
ls -tc                    # Sort by change time
ls -S                     # Sort by size
ls -X                     # Sort by extension
ls -v                     # Natural sort of version numbers
```

### File type filtering

```bash
ls -d */                  # Directories only
ls -p                     # Append / to directories
ls *.txt                  # Files matching pattern
ls -l | grep ^d           # Directories only (alternative)
ls -l | grep ^-           # Files only
```

## Advanced Usage

### Human-readable sizes

```bash
ls -lh                    # KB, MB, GB format
ls -l --block-size=M      # Show sizes in megabytes
```

### Time options

```bash
ls -l --time-style=long-iso     # ISO 8601 format
ls -l --time-style=full-iso     # Full ISO format
ls -lu                          # Show access time instead
ls -lc                          # Show change time instead
```

### Recursive listing

```bash
ls -R                     # Recursive, all subdirectories
ls -R | grep ":$"         # List subdirectory names only
```

## Practical Examples

```bash
# Find largest files in directory
ls -lhS

# Show hidden files only
ls -ld .*

# List files modified in last 24 hours
ls -lt | head

# Count files in directory
ls -1 | wc -l

# List files with full path
ls -d $PWD/*

# Show newest 10 files
ls -lt | head -11

# List files by size, smallest first
ls -lSr

# Show directory size with du
ls -ld */ | awk '{print $9}' | xargs du -sh
```

## Quick Reference Table

|Option|Description|
|---|---|
|`-l`|Long format (detailed)|
|`-a`|All files (including hidden)|
|`-h`|Human-readable sizes|
|`-t`|Sort by modification time|
|`-r`|Reverse sort order|
|`-S`|Sort by file size|
|`-R`|Recursive listing|
|`-1`|One entry per line|
|`-d`|List directories themselves|
|`-F`|Append indicator to entries|
|`-i`|Show inode numbers|
|`-n`|Numeric UID/GID instead of names|

## Common Aliases

Many systems have these aliases by default:

```bash
ll='ls -l'                # Long format
la='ls -A'                # Almost all (exclude . and ..)
l='ls -CF'                # Columns with indicators
```

## File Type Indicators (-F)

```
/   directory
*   executable
@   symbolic link
|   FIFO (named pipe)
=   socket
>   door (Solaris)
```

## Notes

- Output varies by system and configuration
- Color coding (when enabled) helps identify file types
- Hidden files start with a dot (.)
- `.` = current directory, `..` = parent directory
- Use `--help` for full options list: `ls --help`


## Links:

20260129