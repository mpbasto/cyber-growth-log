# 🕸️ Networking Notes

This is a beginner-friendly cheatsheet summarising key concepts from networking fundamentals, based on TryHackMe Pre-Security learning path.

---

## 🌐 What is a Network?

A **network** is a group of two or more connected devices that can communicate and share data.

### Common Types:
- **LAN (Local Area Network)** – Small, local networks (e.g. home or office).
- **WAN (Wide Area Network)** – Connects multiple LANs over large distances (e.g. the Internet).

---

## 🧱 OSI Model (7 Layers)

The **OSI Model** is a framework for understanding how data moves through a network.

| Layer | Name             | Function                                 | Examples                     |
|-------|------------------|------------------------------------------|------------------------------|
| 7     | Application       | User interfaces and apps                 | HTTP, FTP, DNS               |
| 6     | Presentation      | Data translation, encryption, formatting| SSL, JPEG                    |
| 5     | Session           | Opens/closes sessions between devices    | NetBIOS, RPC                 |
| 4     | Transport         | Delivers data reliably or unreliably     | TCP, UDP                     |
| 3     | Network           | Routes packets across networks           | IP, ICMP, routers            |
| 2     | Data Link         | Handles frames on the same network       | MAC addresses, switches      |
| 1     | Physical          | Physical connections, signals            | Ethernet cables, Wi-Fi       |

🧠 **Mnemonic:** *All People Seem To Need Data Processing*

---

## 📨 Packets vs Frames

- **Packet:** Data unit at the Network Layer (includes IP address)
- **Frame:** Data unit at the Data Link Layer (includes MAC address)

*Packets travel across networks. Frames stay within a LAN.*

---

## 🔌 Common Devices

| Device    | Purpose                                      |
|-----------|----------------------------------------------|
| **Switch** | Forwards frames within a LAN using MACs     |
| **Router** | Connects different networks using IPs        |
| **Hub**    | Broadcasts data to all devices (outdated)    |
| **Firewall** | Controls incoming/outgoing traffic         |

---

## 🌍 IP Addressing

- **IP Address**: Unique identifier for a device on a network (e.g. `192.168.1.5`)
- **MAC Address**: Hardware address tied to a network interface (e.g. `00:1A:2B:3C:4D:5E`)
- **Default Gateway**: Router IP used to access outside networks

---

## 🧰 Key Tools & Commands

| Tool / Command      | Purpose                          |
|---------------------|----------------------------------|
| `ipconfig` / `ifconfig` | View IP and MAC addresses     |
| `ping`              | Check if a device is reachable   |
| `tracert` / `traceroute` | Trace route to a destination |
| `nslookup` / `dig`  | Look up DNS information          |
| **Wireshark**       | Network packet capture & analysis|

---

## 🔐 Bonus: Ports & Protocols

| Port | Protocol | Description                      |
|------|----------|----------------------------------|
| 20/21| FTP      | File Transfer                    |
| 22   | SSH      | Secure Shell                     |
| 23   | Telnet   | Remote access (insecure)         |
| 25   | SMTP     | Sending email                    |
| 53   | DNS      | Domain name resolution           |
| 80   | HTTP     | Web browsing (insecure)          |
| 443  | HTTPS    | Secure web browsing              |
| 110  | POP3     | Receive email (older)            |
| 143  | IMAP     | Email sync across devices        |

---

## 🗂️ Notes to Expand Later
- Subnetting
- ARP & DHCP
- VLANs
- NAT & PAT
- Public vs Private IPs
- IPv6 basics

---

✍️ *Last updated: 28-05-2025*
