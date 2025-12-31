## Basic Script Structure

```bash
#!/bin/bash
# This is a comment

echo "Hello, World!"
```

## Variables

```bash
# Variable assignment (no spaces around =)
name="John"
age=25

# Using variables
echo "My name is $name"
echo "I am ${age} years old"

# Command substitution
current_date=$(date)
files=$(ls)

# Read user input
read -p "Enter your name: " username
```

## Special Variables

```bash
$0    # Script name
$1-$9 # First 9 arguments
$#    # Number of arguments
$@    # All arguments as separate strings
$*    # All arguments as single string
$?    # Exit status of last command
$$    # Process ID of current shell
```

## Conditionals

```bash
# If statement
if [ condition ]; then
    # code
elif [ condition ]; then
    # code
else
    # code
fi

# File tests
[ -f file ]    # File exists
[ -d dir ]     # Directory exists
[ -r file ]    # File is readable
[ -w file ]    # File is writable
[ -x file ]    # File is executable
[ -s file ]    # File is not empty

# String comparison
[ "$a" = "$b" ]   # Equal
[ "$a" != "$b" ]  # Not equal
[ -z "$a" ]       # String is empty
[ -n "$a" ]       # String is not empty

# Numeric comparison
[ $a -eq $b ]  # Equal
[ $a -ne $b ]  # Not equal
[ $a -lt $b ]  # Less than
[ $a -le $b ]  # Less than or equal
[ $a -gt $b ]  # Greater than
[ $a -ge $b ]  # Greater than or equal

# Logical operators
[ condition1 ] && [ condition2 ]  # AND
[ condition1 ] || [ condition2 ]  # OR
[ ! condition ]                   # NOT
```

## Loops

```bash
# For loop
for i in 1 2 3 4 5; do
    echo "Number: $i"
done

# For loop with range
for i in {1..5}; do
    echo $i
done

# C-style for loop
for ((i=0; i<5; i++)); do
    echo $i
done

# For loop over files
for file in *.txt; do
    echo "Processing $file"
done

# While loop
counter=0
while [ $counter -lt 5 ]; do
    echo $counter
    ((counter++))
done

# Until loop
until [ $counter -eq 5 ]; do
    echo $counter
    ((counter++))
done

# Loop through array
arr=("apple" "banana" "cherry")
for item in "${arr[@]}"; do
    echo $item
done
```

## Functions

```bash
# Define function
function greet() {
    echo "Hello, $1!"
}

# Alternative syntax
greet() {
    echo "Hello, $1!"
}

# Call function
greet "Alice"

# Return value (0-255)
function add() {
    return $(($1 + $2))
}

# Output and capture
function get_name() {
    echo "John Doe"
}
result=$(get_name)
```

## Arrays

```bash
# Define array
fruits=("apple" "banana" "cherry")

# Access elements
echo ${fruits[0]}        # First element
echo ${fruits[@]}        # All elements
echo ${#fruits[@]}       # Array length

# Add element
fruits+=("date")

# Loop through array
for fruit in "${fruits[@]}"; do
    echo $fruit
done
```

## String Operations

```bash
string="Hello World"

# Length
${#string}

# Substring
${string:6:5}      # "World" (start at 6, length 5)

# Replace
${string/World/Bash}    # Replace first occurrence
${string//o/0}          # Replace all occurrences

# Upper/lowercase
${string^^}        # HELLO WORLD
${string,,}        # hello world

# Concatenation
str1="Hello"
str2="World"
result="$str1 $str2"
```

## Input/Output Redirection

```bash
command > file      # Redirect stdout to file (overwrite)
command >> file     # Redirect stdout to file (append)
command 2> file     # Redirect stderr to file
command &> file     # Redirect both stdout and stderr
command < file      # Read input from file
command1 | command2 # Pipe output of command1 to command2
```

## Command Operators

```bash
command1 && command2  # Run command2 only if command1 succeeds
command1 || command2  # Run command2 only if command1 fails
command1 ; command2   # Run commands sequentially
command &             # Run command in background
```

## Arithmetic Operations

```bash
# Using $(())
result=$((5 + 3))
result=$((10 - 2))
result=$((4 * 3))
result=$((10 / 2))
result=$((10 % 3))   # Modulo

# Increment/Decrement
((counter++))
((counter--))
((counter += 5))

# Using let
let result=5+3
```

## Useful Commands

```bash
# File operations
cat file           # Display file content
head -n 10 file    # First 10 lines
tail -n 10 file    # Last 10 lines
grep "pattern" file # Search for pattern
sed 's/old/new/g' file  # Replace text
awk '{print $1}' file   # Print first column

# File system
ls -la             # List files with details
pwd                # Print working directory
cd directory       # Change directory
mkdir directory    # Create directory
rm file            # Remove file
cp source dest     # Copy file
mv source dest     # Move/rename file

# Process management
ps aux             # List processes
kill PID           # Kill process
jobs               # List background jobs
fg                 # Bring job to foreground
bg                 # Send job to background
```

## Best Practices

```bash
# Always quote variables to handle spaces
echo "$variable"

# Use shellcheck to validate scripts
# Install: apt-get install shellcheck

# Exit on error
set -e

# Exit on undefined variable
set -u

# Print commands as executed (debugging)
set -x

# Combine all
set -euxo pipefail

# Use meaningful variable names
user_name="John"  # Good
un="John"         # Bad

# Add error handling
if ! command; then
    echo "Error occurred" >&2
    exit 1
fi
```


## Links:

[[Who and Where You Are (Linux CLI)]]

#linuxcli

2025112814