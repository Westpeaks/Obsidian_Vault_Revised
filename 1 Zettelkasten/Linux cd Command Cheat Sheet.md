## Basic Usage

```bash
cd [directory]
```

Change the current working directory to the specified directory.

## Common Commands

### Navigate to specific directories

```bash
cd /path/to/directory     # Absolute path
cd Documents              # Relative path (subdirectory of current location)
cd ../                    # Go up one directory level
cd ../../                 # Go up two directory levels
```

### Special shortcuts

```bash
cd                        # Go to home directory
cd ~                      # Go to home directory (explicit)
cd -                      # Go to previous directory (toggle between two directories)
cd /                      # Go to root directory
```

### User directories

```bash
cd ~username              # Go to another user's home directory
cd ~/Documents            # Go to Documents in your home directory
```

## Useful Tips

### Working with spaces in directory names

```bash
cd "My Documents"         # Use quotes
cd My\ Documents          # Use backslash to escape spaces
```

### Using environment variables

```bash
cd $HOME                  # Go to home directory using variable
cd $OLDPWD                # Go to previous directory (same as cd -)
```

### Check current directory

```bash
pwd                       # Print working directory (use after cd to verify)
```

## Common Patterns

```bash
cd ~/Projects/myapp       # Navigate to a project in home directory
cd ../sibling-folder      # Move to a sibling directory
cd -                      # Quick toggle between two locations
cd && ls                  # Go home and list contents
```

## Return Codes

- `0` - Success
- `1` - Failure (directory doesn't exist or no permission)

## Quick Reference Table

|Command|Description|
|---|---|
|`cd` or `cd ~`|Home directory|
|`cd -`|Previous directory|
|`cd ..`|Parent directory|
|`cd /`|Root directory|
|`cd ../..`|Two levels up|
|`cd path/to/dir`|Relative path|
|`cd /path/to/dir`|Absolute path|

## Notes

- `cd` is a shell builtin command, not an external program
- Changes only affect the current shell session
- No output on success (silent operation)
- Use `pwd` to confirm your current location


## Links:

20260129