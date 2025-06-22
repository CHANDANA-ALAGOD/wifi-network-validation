# wifi-network-validation
# WiFi Network Validation

In this project, I set up and validated Wi-Fi network connectivity on Linux (Ubuntu). I used several core networking tools to test network behavior, examine routing paths, and capture live packet data with Wireshark. The goal was to build practical experience in Linux-based network configuration and troubleshooting.

---

## System Details

- **Laptop:** Dell Vostro 3400  
- **Operating System:** Ubuntu Linux (dual-boot with Windows 11)  
- **Wi-Fi Interface:** wlp3s0  
- **Internet Provider:** ACT Fibernet  
- **Public IP:** Dynamic (example: 49.205.72.39)  

---

## Tools and Commands Used

| Tool / Command   | Purpose                          |
|-----------------|----------------------------------|
| ping            | Check packet delivery and latency |
| traceroute      | Visualize the network path to a destination |
| netstat -rn     | View the system routing table     |
| ip addr         | Display network interface details |
| Wireshark       | Capture and analyze network traffic |

---

## Tasks Performed

### 1. Checked Network Interface

```bash
ip addr
```
- Verified IP address, interface status, and configuration.

### 2. Performed Ping Test to Google DNS

```bash
ping -c 10 8.8.8.8
```
- 0% packet loss  
- Average round-trip time: ~8–12 ms  
- Confirmed stable network connectivity.

### 3. Ran Traceroute

```bash
traceroute 8.8.8.8
```
- Traced the network path to Google DNS.  
- Identified about 8 hops through ISP and upstream routers.

### 4. Viewed Kernel Routing Table

```bash
netstat -rn
```
- Verified default gateway and local network routes.

### 5. Captured Live Packets with Wireshark

- Interface monitored: `wlp3s0` (Wi-Fi)  
- Captured:
  - ICMP Echo Requests and Replies
  - ARP traffic for device discovery
- Packet capture saved as: `wifi_ping_test.pcapng`

---

## Project Structure

```text
wifi-network-validation/
├── README.md
├── wifi_ping_test.pcapng
└── screenshots/
    ├── ip_addr.png
    ├── ping_result.png
    ├── traceroute.png
    ├── netstat_rn.png
    └── wireshark_capture.png
```

---

## Conclusion

By completing this project, I gained practical experience in configuring and testing network connectivity on Linux. I successfully verified Wi-Fi operation, analyzed routing paths, and captured live traffic to better understand how network communications work. This hands-on learning will help in future networking and troubleshooting scenarios.
