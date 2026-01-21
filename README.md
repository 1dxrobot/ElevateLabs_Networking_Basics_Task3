# ElevateLabs_Networking_Basics_Task3
## Core Networking Concepts

Understanding core networking concepts like IP addresses, MAC addresses, DNS resolution, and TCP/UDP protocols is essential for grasping how data moves across networks. 



### 1. IP Addresses

An **IP address** (Internet Protocol address) is a numerical label assigned to each device connected to a network using the Internet Protocol.  It serves two main functions: **host or network interface identification** and **location addressing**. 

- IPv4 addresses are 32-bit numbers (e.g., `192.168.1.1`)
- IPv6 addresses are 128-bit numbers (e.g., `2001:0db8:85a3::8a2e:0370:7334`)

IP addresses allow devices to locate and communicate with each other across networks.



### 2. MAC Addresses

A **MAC address** (Media Access Control address) is a unique identifier assigned to a network interface controller (NIC) for communication at the **data link layer** (Layer 2) of a network. 

- Expressed as six groups of two hexadecimal digits (e.g., `00:1A:2B:3C:4D:5E`)
- Assigned by the manufacturer and typically hardcoded
- Used for communication within the same local network segment 

When data is sent on a local network, the **Address Resolution Protocol (ARP)** resolves an IP address to its corresponding MAC address.



### 3. DNS Resolution

The **Domain Name System (DNS)** translates human-readable domain names (like `www.google.com`) into IP addresses that computers use to identify each other. 

- Acts as the "phonebook" of the internet
- Uses distributed servers to resolve names efficiently
- Supports various record types:
  - **A record**: Maps domain to IPv4 address
  - **AAAA record**: Maps domain to IPv6 address
  - **PTR record**: Used for reverse DNS (IP to domain)
  - **CNAME**: Alias for one domain to another 

Without DNS, users would need to remember numerical IP addresses for every website.



### 4. TCP vs UDP

These are the two primary transport layer protocols in the TCP/IP suite. 

#### TCP (Transmission Control Protocol)
- **Connection-oriented**: Establishes a session before data transfer
- **Reliable**: Ensures delivery via acknowledgments and retransmissions
- **Ordered**: Guarantees data arrives in sequence
- **Slower** due to overhead
- Used by HTTP, HTTPS, FTP, SMTP 

#### UDP (User Datagram Protocol)
- **Connectionless**: Sends data without establishing a session
- **Unreliable**: No delivery guarantees
- **Faster** and lower overhead
- Suitable for real-time applications
- Used by DNS queries, VoIP, online gaming, video streaming 

$$
\text{Use TCP when reliability matters; use UDP when speed matters.}
$$



