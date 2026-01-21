# ElevateLabs_Networking_Basics_Task3
## 1.1Core Networking Concepts

Understanding core networking concepts like IP addresses, MAC addresses, DNS resolution, and TCP/UDP protocols is essential for grasping how data moves across networks. 

### 1.2 IP Addresses
- IPv4 addresses are 32-bit numbers (e.g., `192.168.1.1`)
- IPv6 addresses are 128-bit numbers (e.g., `2001:0db8:85a3::8a2e:0370:7334`)

IP addresses allow devices to locate and communicate with each other across networks.

### 1.3. MAC Addresses
- Expressed as six groups of two hexadecimal digits (e.g., `00:1A:2B:3C:4D:5E`)

### 1.4. DNS Resolution

The **Domain Name System (DNS)** translates human-readable domain names (like `www.google.com`) into IP addresses that computers use to identify each other. 
- Supports various record types:
  - **A record**: Maps domain to IPv4 address
  - **AAAA record**: Maps domain to IPv6 address
  - **PTR record**: Used for reverse DNS (IP to domain)
  - **CNAME**: Alias for one domain to another 
Without DNS, users would need to remember numerical IP addresses for every website.

### 1.5. TCP vs UDP
These are the two primary transport layer protocols in the TCP/IP suite. 
#### TCP (Transmission Control Protocol)
- **Connection-oriented** , **Reliable**
- **Ordered** , **Slower** 
- Used by HTTP, HTTPS, FTP, SMTP
- 
#### UDP (User Datagram Protocol)
- **Connectionless**
- **Unreliable**
- **Faster** 
- Suitable for real-time applications
- Used by DNS queries, VoIP, online gaming, video streaming.

## 2.Using Wireshark on Kali Linux
Wireshark is **pre-installed** on Kali Linux and functions as a powerful network protocol analyzer for capturing and inspecting traffic in real time. 

### Launch and Interface
Start Wireshark with:
```bash
sudo wireshark
```
Ensure your user is in the `wireshark` group for packet capture permissions:
```bash
sudo usermod -aG wireshark $USER
```
### Capture Traffic
- Open Wireshark and select a network interface (e.g., `eth0`, `wlan0`)
- Click the **shark icon** to begin live capture
- Generate traffic (e.g., `curl http://example.com`) to observe packets
- Stop with the **red square button** 

### Analyze Packets
Wireshark’s three-pane interface shows:
1. **Packet list**: Summary of captured packets
2. **Packet details**: Protocol layer breakdown (Ethernet, IP, TCP, etc.)
3. **Raw data**: Hexadecimal and ASCII view of packet content 

### Apply Filters
Use display filters to isolate traffic:
- `http` – Show only HTTP traffic
- `ip.addr == 192.168.1.1` – Filter by IP
- `tcp.port == 80` – Filter by port
- `dns` – View DNS queries 

Save captures in `.pcapng` format for later analysis or sharing.







