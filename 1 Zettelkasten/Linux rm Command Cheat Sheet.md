## Basic Usage

```bash
rm [options] file/directory
```

Remove (delete) files or directories.

## ⚠️ CRITICAL WARNING

**`rm` is PERMANENT - there is no undo and no trash/recycle bin!**

- Deleted files cannot be recovered easily
- Always double-check before pressing Enter
- Consider using `rm -i` for interactive confirmation
- Test with `ls` first to verify what will be deleted

## Basic Commands

### Remove files

```bash
rm file.txt               # Delete a single file
rm file1.txt file2.txt    # Delete multiple files
rm *.txt                  # Delete all .txt files in current directory
rm *                      # Delete all files in current directory (DANGEROUS!)
```

### Remove directories

```bash
rm -r directory/          # Remove directory and its contents recursively
rm -rf directory/         # Force remove directory (no prompts)
rmdir directory/          # Remove empty directory only (safer alternative)
```

## Common Options

### Safety options

```bash
rm -i file.txt            # Interactive - prompt before each deletion
rm -I files*              # Prompt once before removing more than 3 files
rm -v file.txt            # Verbose - show what's being deleted
```

### Force and recursive

```bash
rm -f file.txt            # Force - ignore nonexistent files, never prompt
rm -r directory/          # Recursive - remove directories and contents
rm -rf directory/         # Force recursive (VERY DANGEROUS!)
```

## Common Combinations

```bash
rm -rf directory/         # Remove directory forcefully (most common, most dangerous)
rm -riv directory/        # Remove directory with confirmation and verbose output
rm -f *.tmp               # Force remove all .tmp files
rm -ri folder/            # Remove directory with confirmation for each file
```

## Safe Practices

### Always verify first

```bash
ls file.txt               # Check file exists
ls *.log                  # See what matches pattern before deleting
ls -la directory/         # Inspect directory contents first
```

### Use interactive mode when unsure

```bash
rm -i *.txt               # Confirm each file deletion
rm -rI directory/         # Confirm once before removing directory
```

### Preview what will be deleted

```bash
echo *.txt                # Show matching files without deleting
find . -name "*.tmp"      # Preview files to delete
```

## Removing Specific File Types

```bash
# Remove by extension
rm *.txt                  # All .txt files
rm *.log *.tmp            # Multiple extensions

# Remove by pattern
rm file*                  # Files starting with "file"
rm *backup*               # Files containing "backup"
rm ?????.txt              # Files with exactly 5 characters + .txt

# Remove hidden files
rm .*.swp                 # Hidden files matching pattern
```

## Advanced Usage

### Remove with find

```bash
# Safer than rm -rf for complex deletions
find . -name "*.tmp" -type f -delete
find . -name "*.log" -type f -exec rm {} \;
find . -type f -mtime +30 -delete        # Files older than 30 days
```

### Remove everything except certain files

```bash
# Using extended globbing (bash)
shopt -s extglob
rm !(keep.txt|important.doc)             # Remove all except specified files

# Using find
find . -type f -not -name "*.txt" -delete
```

### Remove empty directories

```bash
find . -type d -empty -delete            # Remove all empty directories
rmdir */                                 # Remove empty subdirectories
```

## Protection Techniques

### Create alias for safety

```bash
alias rm='rm -i'          # Add to ~/.bashrc for interactive mode by default
alias rm='rm -I'          # Prompt only for 3+ files
```

### Use trash instead of rm

```bash
# Install trash-cli
sudo apt install trash-cli

# Use trash instead
trash file.txt            # Moves to trash instead of deleting
trash-list                # List trashed files
trash-restore             # Restore from trash
trash-empty               # Empty trash
```

### Create a safety wrapper

```bash
# Add to ~/.bashrc
rm() {
    echo "Files to be deleted:"
    ls -l "$@"
    read -p "Continue? (y/n) " -n 1 -r
    echo
    if [[ $REPLY =~ ^[Yy]$ ]]; then
        command rm "$@"
    fi
}
```

## Common Mistakes to AVOID

```bash
# DANGEROUS - Don't do these!
rm -rf /                  # Deletes entire system (requires --no-preserve-root)
rm -rf /*                 # Deletes everything in root
rm -rf ~/*                # Deletes everything in home directory
rm -rf ./*                # Deletes everything in current directory
rm -rf . / file.txt       # Space causes deletion of current directory!

# Accidental patterns
rm * .txt                 # Space before .txt deletes everything + file named ".txt"
rm *.log *.txt *.doc      # Make sure you're in the right directory!
```

## Practical Examples

```bash
# Remove old log files
rm *.log

# Remove backup files safely
rm -i *~

# Clean temporary files
rm -f /tmp/*.tmp

# Remove directory and contents
rm -r old_project/

# Remove with confirmation for large deletion
rm -rI large_folder/

# Remove files older than 7 days
find . -type f -mtime +7 -exec rm {} \;

# Remove broken symbolic links
find . -type l ! -exec test -e {} \; -delete
```

## Quick Reference Table

|Option|Description|
|---|---|
|`-r` or `-R`|Recursive - remove directories and contents|
|`-f`|Force - ignore nonexistent files, no prompts|
|`-i`|Interactive - prompt before every removal|
|`-I`|Prompt once before removing 3+ files|
|`-v`|Verbose - show what's being removed|
|`-d`|Remove empty directories|
|`--preserve-root`|Do not remove '/' (default)|
|`--no-preserve-root`|Do not treat '/' specially (DANGEROUS)|

## Alternatives to rm

```bash
trash file.txt            # trash-cli - moves to trash
gio trash file.txt        # GNOME trash
mv file.txt ~/.trash/     # Manual move to trash folder
shred file.txt            # Securely delete (overwrite before removal)
```

## Recovery Options (Limited)

If you accidentally deleted files:

```bash
# Stop writing to disk immediately!
# For ext3/ext4 filesystems
extundelete /dev/sdXN --restore-all

# For any filesystem (must act quickly)
photorec                  # File recovery tool
testdisk                  # Partition and file recovery

# Commercial options
# - R-Studio
# - EaseUS Data Recovery
```

## Return Codes

- `0` - Success
- `1` - Minor problems
- `2` - Serious problems (file doesn't exist, permission denied)

## Notes

- `rm` does not move files to trash - deletion is immediate and permanent
- Root privileges (`sudo rm`) are especially dangerous
- Always use absolute paths when using `sudo rm -rf`
- Consider enabling `-i` or `-I` by default in your shell configuration
- When in doubt, move files to a temporary location instead of deleting
- The `unlink` command is similar to `rm` for single files


## Links:

20260129