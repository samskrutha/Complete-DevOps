# Most Used Commands

This file provides the details of some of the most used Linux commands.

## 1. `ls`
Lists directory contents.
- `ls -l`: Detailed list including file permissions, ownership, size, and modification date.
- `ls -a`: Includes hidden files.

## 2. `cd`
Changes the current directory.
- `cd /path/to/directory`: Moves to the specified directory.
- `cd ..`: Moves up one directory level.

## 3. `pwd`
Prints the current working directory.

## 4. `mkdir`
Creates a new directory.
- `mkdir directory_name`: Creates a single directory.
- `mkdir -p /path/to/directory`: Creates nested directories.

## 5. `rm`
Removes files or directories.
- `rm filename`: Deletes a file.
- `rm -r directory_name`: Recursively deletes a directory and its contents.
- `rm -f filename`: Forces deletion without confirmation.

## 6. `cp`
Copies files or directories.
- `cp source destination`: Copies a file.
- `cp -r source_directory destination_directory`: Recursively copies a directory.

## 7. `mv`
Moves or renames files or directories.
- `mv old_name new_name`: Renames a file or directory.
- `mv file_name /path/to/directory`: Moves a file to a new directory.

## 8. `touch`
Creates an empty file or updates the timestamp of an existing file.
- `touch filename`: Creates an empty file.

## 9. `cat`
Concatenates and displays file contents.
- `cat filename`: Displays the content of a file.

## 10. `echo`
Displays a line of text.
- `echo "text"`: Prints the text to the terminal.
- `echo $VARIABLE_NAME`: Prints the value of a variable.

## 11. `grep`
Searches for patterns in files.
- `grep 'pattern' filename`: Searches for a pattern in a file.
- `grep -r 'pattern' directory_name`: Recursively searches within a directory.

## 12. `find`
Searches for files in a directory hierarchy.
- `find /path -name filename`: Finds files with a specific name.
- `find /path -type d`: Finds directories.

## 13. `chmod`
Changes file permissions.
- `chmod 755 filename`: Sets read, write, and execute permissions for the owner, and read and execute for others.

## 14. `chown`
Changes file owner and group.
- `chown user:group filename`: Changes the owner and group of a file.

## 15. `ps`
Reports a snapshot of current processes.
- `ps aux`: Detailed list of all processes.
- `ps -ef`: Another format for displaying processes.

## 16. `top`
Displays real-time system information, including running processes.

## 17. `kill`
Terminates a process by PID.
- `kill PID`: Sends the default TERM signal to terminate a process.
- `kill -9 PID`: Forcefully kills a process.

## 18. `wget`
Retrieves files from the web.
- `wget URL`: Downloads a file from the specified URL.

## 19. `curl`
Transfers data from or to a server.
- `curl -O URL`: Downloads a file.
- `curl -I URL`: Fetches the headers only.

## 20. `tar`
Archives files.
- `tar -cvf archive_name.tar directory_name`: Creates an archive.
- `tar -xvf archive_name.tar`: Extracts an archive.

## 21. `zip`
Compresses files.
- `zip archive_name.zip filename`: Compresses a file.
- `zip -r archive_name.zip directory_name`: Compresses a directory.

## 22. `unzip`
Extracts files from a zip archive.
- `unzip archive_name.zip`: Extracts the archive.

## 23. `df`
Displays disk space usage.
- `df -h`: Human-readable format.

## 24. `du`
Estimates file space usage.
- `du -h`: Human-readable format.
- `du -sh directory_name`: Summary for a directory.

## 25. `mount`
Mounts a filesystem.
- `mount /dev/sdX /mnt`: Mounts a device.

## 26. `umount`
Unmounts a filesystem.
- `umount /mnt`: Unmounts a device.

## 27. `ifconfig`
Configures network interfaces.
- `ifconfig eth0`: Displays the configuration of the eth0 interface.

## 28. `ip`
Shows/manipulates routing, devices, policy routing, and tunnels.
- `ip a`: Displays all IP addresses.
- `ip link set eth0 up`: Brings up the eth0 interface.

## 29. `netstat`
Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
- `netstat -tuln`: Lists all listening ports.

## 30. `ss`
Utility to investigate sockets.
- `ss -tuln`: Lists all listening ports.

## 31. `ssh`
Opens an SSH connection to a remote machine.
- `ssh user@hostname`: Connects to a remote machine.

## 32. `scp`
Copies files over SSH.
- `scp file user@hostname:/path/to/destination`: Copies a file to a remote machine.
- `scp user@hostname:/path/to/source file`: Copies a file from a remote machine.

## 33. `rsync`
Synchronizes files and directories between two locations.
- `rsync -avz source destination`: Archives files, compresses during transfer, and preserves permissions.

## 34. `crontab`
Schedules commands to run at specific times.
- `crontab -e`: Edits the current user's crontab.
- `crontab -l`: Lists the current user's crontab.

## 35. `systemctl`
Controls the systemd system and service manager.
- `systemctl start service_name`: Starts a service.
- `systemctl stop service_name`: Stops a service.
- `systemctl restart service_name`: Restarts a service.
- `systemctl status service_name`: Checks the status of a service.

## 36. `journalctl`
Views systemd logs.
- `journalctl -u service_name`: Views logs for a specific service.

## 37. `docker`
Manages Docker containers.
- `docker ps`: Lists running containers.
- `docker images`: Lists images.
- `docker run image_name`: Runs a container.
- `docker stop container_id`: Stops a running container.

## 38. `kubectl`
Controls Kubernetes clusters.
- `kubectl get pods`: Lists all pods.
- `kubectl describe pod pod_name`: Describes a pod.
- `kubectl logs pod_name`: Shows logs for a pod.

## 39. `ansible`
Manages Ansible automation.
- `ansible-playbook playbook.yml`: Runs an Ansible playbook.
- `ansible -m ping all`: Pings all managed hosts.

## 40. `git`
Version control system for tracking changes in source code.
- `git clone repository_url`: Clones a repository.
- `git status`: Shows the working tree status.
- `git add .`: Adds all changes to staging.
- `git commit -m "message"`: Commits changes.
- `git push`: Pushes changes to the remote repository.

## 41. `vim`
Text editor.
- `vim filename`: Opens a file in vim.
- `:w`: Saves changes.
- `:q`: Quits vim.

## 42. `nano`
Text editor.
- `nano filename`: Opens a file in nano.
- `Ctrl+O`: Saves changes.
- `Ctrl+X`: Exits nano.

## 43. `htop`
Interactive process viewer.

## 44. `hostname`
Shows or sets the system’s hostname.
- `hostname`: Displays the current hostname.
- `hostname new_hostname`: Sets a new hostname.

## 45. `useradd`
Creates a new user.
- `useradd username`: Adds a new user.
- `useradd -m username`: Adds a new user with a home directory.

## 46. `usermod`
Modifies a user account.
- `usermod -aG groupname username`: Adds a user to a group.

## 47. `passwd`
Changes a user’s password.
- `passwd username`: Changes the password for a user.

## 48. `ufw`
Uncomplicated Firewall, a front-end for managing iptables firewall rules.
- `ufw enable`: Enables the firewall.
- `ufw disable`: Disables the firewall.
- `ufw allow port_number`: Allows traffic on a specific port.

## 49. `iptables`
Configures the IP packet filter rules of the Linux kernel firewall.
- `iptables -L`: Lists the current rules.
- `iptables -A INPUT -p tcp --dport 22 -j ACCEPT`: Allows SSH traffic.

## 50. `df`
Reports file system disk space usage.
- `df -h`: Displays in human-readable format.


