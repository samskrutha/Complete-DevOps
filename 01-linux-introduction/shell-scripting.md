# Shell Scripting

```markdown
# Introduction to Shell Scripting

This guide will help you understand how to write shell scripts, provide examples of different types of shell scripts, and explain the differences between various types of shells.

## What is a Shell Script?

A shell script is a text file containing a series of commands that are executed by a shell interpreter. Shell scripts can automate repetitive tasks, manage system operations, and simplify complex commands.

## How to Write a Shell Script

1. **Create a New File**: Use a text editor to create a new file with a `.sh` extension.
2. **Add the Shebang Line**: The first line of the script should specify the interpreter.
    ```sh
    #!/bin/bash
    ```
3. **Write Commands**: Add the commands you want to execute.
4. **Save and Close the File**.
5. **Make the Script Executable**: Use the `chmod` command to make the script executable.
    ```sh
    chmod +x script.sh
    ```
6. **Run the Script**: Execute the script by typing its path.
    ```sh
    ./script.sh
    ```

## Examples of Shell Scripts

### 1. Hello World Script

This is the simplest shell script that prints "Hello, World!" to the terminal.

```sh
#!/bin/bash
# A simple Hello World script
echo "Hello, World!"
```

### 2. Backup Script

This script creates a backup of a specified directory.

```sh
#!/bin/bash
# Backup script
SOURCE_DIR="/path/to/source"
DEST_DIR="/path/to/backup"
DATE=$(date +%Y%m%d%H%M%S)

tar -czf ${DEST_DIR}/backup-${DATE}.tar.gz -C ${SOURCE_DIR} .
echo "Backup of ${SOURCE_DIR} completed successfully."
```

### 3. User Input Script

This script asks for user input and prints a message.

```sh
#!/bin/bash
# User input script
echo "Enter your name:"
read name
echo "Hello, $name!"
```

### 4. System Information Script

This script displays system information such as the current user, hostname, and system uptime.

```sh
#!/bin/bash
# System information script
echo "Current User: $(whoami)"
echo "Hostname: $(hostname)"
echo "System Uptime: $(uptime -p)"
```

### 5. Loop Script

This script prints numbers from 1 to 10 using a loop.

```sh
#!/bin/bash
# Loop script
for i in {1..10}
do
  echo "Number: $i"
done
```

## Types of Shells and Differences

### 1. Bash (Bourne Again Shell)
- **File**: `/bin/bash`
- **Features**: Command history, command-line editing, job control, functions, and arrays.
- **Usage**: Most popular and widely used shell in Linux systems.

### 2. Sh (Bourne Shell)
- **File**: `/bin/sh`
- **Features**: Basic shell with less functionality compared to Bash. It's the original Unix shell.
- **Usage**: Used for scripting in Unix and early Linux systems. Provides basic scripting features.

### 3. Csh (C Shell)
- **File**: `/bin/csh`
- **Features**: C-like syntax, job control, and interactive features.
- **Usage**: Less common, used in academic environments for learning shell scripting with a C-like syntax.

### 4. Ksh (Korn Shell)
- **File**: `/bin/ksh`
- **Features**: Combines features of the Bourne Shell and C Shell, including scripting and interactive use.
- **Usage**: Used in commercial Unix systems and by users who require advanced scripting features.

### 5. Zsh (Z Shell)
- **File**: `/bin/zsh`
- **Features**: Advanced scripting, command-line editing, spelling correction, and plugin support.
- **Usage**: Popular among power users and developers for its extensive customization and feature set.
