# Core Concepts

This document outlines some of the core concepts in Linux.

## Soft Links and Hard Links

### Soft Links (Symbolic Links)
A soft link, or symbolic link, is a type of file that points to another file or directory. It’s similar to a shortcut in Windows.

- **Creation**: Use the `ln -s` command.
- **Example**: 
  ```sh
  ln -s /path/to/target /path/to/softlink
  ```
  This command creates a symbolic link named `softlink` that points to `target`.

- **Behavior**: If the target file is deleted, the soft link becomes a "dangling" link, meaning it points to a non-existent file.

### Hard Links
A hard link is an additional name for an existing file on the same filesystem. It points directly to the inode of the file.

- **Creation**: Use the `ln` command.
- **Example**:
  ```sh
  ln /path/to/target /path/to/hardlink
  ```
  This command creates a hard link named `hardlink` that points to `target`.

- **Behavior**: If the original file is deleted, the hard link still contains the data because it points to the same inode. However, hard links cannot span across different filesystems or partitions.

### Differences
- **Soft Links**: Can link to directories and can span across different filesystems. If the target is deleted, the link is broken.
- **Hard Links**: Cannot link to directories and must be on the same filesystem. The data remains accessible as long as there is at least one link to the inode.

## Systemd vs. Initd

### Initd
Initd, also known as System V init, is one of the earliest systems and service managers for UNIX-like operating systems.

- **Scripts**: Uses shell scripts located in `/etc/init.d/` to manage services.
- **Runlevels**: Uses runlevels to define different states of the machine (e.g., single-user mode, multi-user mode).
- **Startup Sequence**: Executes startup scripts sequentially based on runlevels.

### Systemd
Systemd is a modern system and service manager for Linux, designed to provide better performance and more features than initd.

- **Units**: Uses unit files (e.g., service, socket, target units) to manage services.
- **Parallel Startup**: Starts services in parallel, which speeds up the boot process.
- **Logging**: Integrates with `journalctl` for comprehensive logging.
- **Commands**: Uses `systemctl` to manage services (e.g., start, stop, enable, disable).

- **Example**:
  ```sh
  systemctl start service_name
  systemctl stop service_name
  systemctl enable service_name
  systemctl disable service_name
  ```

### Differences
- **Performance**: Systemd offers faster boot times through parallelization.
- **Configuration**: Systemd uses declarative unit files, while initd uses shell scripts.
- **Features**: Systemd provides advanced features like on-demand starting of daemons, snapshot support, and system state tracking.

## Other Core Concepts

### Package Management
DevOps engineers must be familiar with package managers to install, update, and manage software.

- **APT**: Used in Debian-based distributions (e.g., Ubuntu).
  ```sh
  apt-get update
  apt-get install package_name
  apt-get upgrade
  ```

- **YUM/DNF**: Used in Red Hat-based distributions (e.g., CentOS, Fedora).
  ```sh
  yum install package_name
  dnf install package_name
  ```

### File Permissions
Understanding file permissions is crucial for security and proper system function.

- **Symbols**: 
  - `r` (read), `w` (write), `x` (execute)
  - `u` (user/owner), `g` (group), `o` (others)

- **Commands**:
  ```sh
  chmod 755 filename   # rwxr-xr-x
  chown user:group filename
  ```

### Networking
Knowledge of basic networking commands is essential.

- **Commands**:
  - `ifconfig` / `ip a`: View network interfaces.
  - `ping`: Test connectivity.
  - `netstat` / `ss`: View network connections.
  - `traceroute`: Trace the path to a network host.

### Monitoring and Logging
Monitoring system performance and logging are critical for maintaining system health.

- **Commands**:
  - `top` / `htop`: Real-time process monitoring.
  - `free -m`: Check memory usage.
  - `df -h`: Check disk usage.
  - `journalctl`: View systemd logs.
  - `tail -f /var/log/syslog`: Monitor log files in real-time.

### Automation and Scripting
Automation is key in DevOps for efficiency and consistency.

- **Shell Scripting**: Writing scripts to automate tasks.
  ```sh
  #!/bin/bash
  echo "Hello, World!"
  ```

- **Cron Jobs**: Schedule tasks to run at specific times.
  ```sh
  crontab -e
  # Add a cron job: 
  # * * * * * /path/to/script.sh
  ```

### Version Control
Using version control systems, especially Git, is fundamental for code and configuration management.

- **Commands**:
  ```sh
  git clone repository_url
  git status
  git add .
  git commit -m "message"
  git push
  ```
