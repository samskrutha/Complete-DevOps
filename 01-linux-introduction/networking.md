# Linux Networking Commands 

## Introduction to Networking

Networking is a crucial aspect of IT, enabling technologies like the internet. Linux engineers need to understand network technologies and communication methods, focusing on the fundamentals rather than an expert-level comprehension.

### Key Networking Models
1. **OSI Model**: Comprises seven layers
    - Application Layer
    - Presentation Layer
    - Session Layer
    - Transport Layer
    - Network Layer
    - Data Link Layer
    - Physical Layer

2. **TCP/IP Model**: Simplified into four layers
    - Application Layer
    - Transport Layer
    - Network Layer (or Internet Layer)
    - Network Access Layer

## OSI Model Layers and Examples

1. **Application Layer**: Interfaces directly with end-users.
    - **Examples**: Web browsers, email clients, FTP clients, HTTP servers.

2. **Presentation Layer**: Handles data format, encryption, and decryption.
    - **Examples**: SSL/TLS, JPEG, GIF, MPEG, ASCII, EBCDIC.

3. **Session Layer**: Manages sessions, including setup, maintenance, and teardown.
    - **Examples**: NetBIOS, RPC (Remote Procedure Call), PPTP (Point-to-Point Tunneling Protocol).

4. **Transport Layer**: Ensures complete data transfer.
    - **Examples**: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).

5. **Network Layer**: Determines how data is sent to the receiver.
    - **Examples**: Routers, IP (Internet Protocol), ICMP (Internet Control Message Protocol).

6. **Data Link Layer**: Transmits data frames between nodes on the same network.
    - **Examples**: Switches, bridges, Ethernet, MAC (Media Access Control) addresses.

7. **Physical Layer**: Transmits raw bitstream over a physical medium.
    - **Examples**: Hubs, repeaters, cables (Ethernet cables, fiber optics), network interface cards (NICs).

## TCP/IP Model Layers and Examples

1. **Application Layer**: Provides network services to applications.
    - **Examples**: HTTP, FTP, SMTP, DNS.

2. **Transport Layer**: Manages end-to-end communication, using protocols like TCP and UDP.
    - **Examples**: TCP, UDP.

3. **Internet Layer**: Routes packets across networks using IP addresses.
    - **Examples**: IP (Internet Protocol), ICMP, IGMP (Internet Group Management Protocol).

4. **Network Access Layer**: Manages the hardware addressing and defines protocols for the physical transmission of data.
    - **Examples**: Ethernet, Wi-Fi, ARP (Address Resolution Protocol), PPP (Point-to-Point Protocol).

## Data Transmission

- **Bits**: Transmitted at the Physical Layer using electrical voltage or light.
- **Frames**: Transmitted at the Data Link Layer ensuring frames don't exceed the Maximum Transmission Unit (MTU).
- **Packets**: Transmitted at the Network Layer using logical IP addresses.
- **Segments**: Transmitted at the Transport Layer using protocols like TCP and UDP.

## Important Networking Concepts

### TCP (Transmission Control Protocol)
- Connection-oriented and reliable.
- Establishes a connection using a three-way handshake (SYN, SYN-ACK, ACK).
- Uses windowing for efficient data transfer.

### UDP (User Datagram Protocol)
- Connectionless and less reliable.
- No acknowledgment of received segments.
- Primed for speed and performance, suitable for real-time applications like video calls.

### ICMP (Internet Control Message Protocol)
- Used by tools like `ping` for network diagnostics.

### Common Network Ports
- **FTP**: Port 20, 21
- **SSH**: Port 22
- **Telnet**: Port 23
- **SMTP**: Port 25
- **DNS**: Port 53
- **HTTP**: Port 80
- **NTP**: Port 123
- **SNMP**: Port 161, 162
- **HTTPS**: Port 443

### Configuration File for Network Services
- Located at `/etc/services`

## Practical Tips for System Administrators
- Understand and use tools like `ping`, `traceroute`, and `netstat` for network troubleshooting.
- Familiarize with network configuration files and logs to diagnose and fix network issues.
- Always ensure secure connections, preferring protocols like SSH over Telnet.

## Common Networking Commands and Their Usage

### `ping`
- Used to test the connectivity between two nodes.
- Syntax: `ping [hostname/IP address]`
- Example: `ping google.com`

### `traceroute`
- Used to trace the path packets take to reach the destination.
- Syntax: `traceroute [hostname/IP address]`
- Example: `traceroute google.com`

### `netstat`
- Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
- Syntax: `netstat [options]`
- Example: `netstat -tuln` (Displays listening ports)

### `ifconfig`
- Used to configure, control, and query TCP/IP network interface parameters.
- Syntax: `ifconfig [interface] [options]`
- Example: `ifconfig eth0`

### `ip`
- Used for network and routing management.
- Syntax: `ip [options]`
- Example: `ip addr show` (Displays IP addresses)

### `nslookup`
- Queries DNS servers to find out domain names or IP addresses.
- Syntax: `nslookup [hostname/IP address]`
- Example: `nslookup google.com`

### `dig`
- Queries DNS servers for information about host addresses, mail exchanges, name servers, and related information.
- Syntax: `dig [options] [hostname/IP address]`
- Example: `dig google.com`

### `route`
- Displays or modifies the IP routing table.
- Syntax: `route [options]`
- Example: `route -n` (Displays the routing table)

### `iptables`
- Administers the IP packet filter rules of the Linux kernel.
- Syntax: `iptables [options]`
- Example: `iptables -L` (Lists all rules)

### `curl`
- Transfers data from or to a server using various protocols.
- Syntax: `curl [options] [URL]`
- Example: `curl http://www.google.com`

### `wget`
- Retrieves files from the web.
- Syntax: `wget [options] [URL]`
- Example: `wget http://www.google.com/index.html`

### `tcpdump`
- Captures network packets and displays them.
- Syntax: `tcpdump [options]`
- Example: `tcpdump -i eth0`

## Debugging Network Issues

### Using `ping`
- **Command**: `ping google.com`
- **Use**: Check if the host is reachable.
- **Debug**: If no response, check the network connection and DNS settings.

### Using `traceroute`
- **Command**: `traceroute google.com`
- **Use**: Identify where the connection fails in the network path.
- **Debug**: Investigate the hops where the connection times out.

### Using `netstat`
- **Command**: `netstat -tuln`
- **Use**: Check open ports and listening services.
- **Debug**: Ensure the necessary services are running and listening on the correct ports.

### Using `ifconfig` or `ip addr show`
- **Command**: `ifconfig eth0` or `ip addr show`
- **Use**: Check the IP address and network interface status.
- **Debug**: Verify the interface has the correct IP address and is up.

### Using `nslookup` or `dig`
- **Command**: `nslookup google.com` or `dig google.com`
- **Use**: Resolve DNS issues.
- **Debug**: Ensure the correct DNS server is configured and the domain resolves properly.

### Using `route`
- **Command**: `route -n`
- **Use**: Check the routing table.
- **Debug**: Ensure the default gateway and routes are correctly configured.

### Using `iptables`
- **Command**: `iptables -L`
- **Use**: Check firewall rules.
- **Debug**: Ensure the firewall rules are not blocking necessary traffic.

### Using `tcpdump`
- **Command**: `tcpdump -i eth0`
- **Use**: Capture and analyze network traffic.
- **Debug**: Identify unusual traffic patterns or errors.
