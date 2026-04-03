## 📌 Overview

This repository contains lab work and notes completed as part of the **Cisco Networking Basics** course — a foundational course in understanding how networks are built, configured, and secured.

**Course:** Cisco Networking Basics
**Platform:** Cisco Skills for All (NetAcad)
**Status:** ✅ Completed

## 📁 What's Inside
Network fundamentals
Network Components, Types and Connections
Wireless and Mobile Networks
Build a Home Network
Communication Principles
Network Media
The Access Layer
Internet Protocol
IPv4 and Network Segmentation
IPv6 Addressing Formats and Rules
Dynamic Addressing Formats and Rules
Gateways to Other Networks
The ARP Process
Routing between Networks
TCP and UDP
Application Layer Services
Network Testing Utilities


## 🧪 Labs Covered

| Lab | Concepts Practiced |
|---|---|
| Basic LAN Setup | Switch config, end-device connectivity |
| IP Addressing | Subnetting, assigning static IPs |
| Router Config | Default gateway, inter-VLAN routing |
| DNS & DHCP | Automatic IP assignment, name resolution |
| Wireless Setup | SSID config, WPA2 security |


## 🗝️ Key Concepts Learned

- **OSI & TCP/IP models** — how data travels across a network layer by layer
- **IP addressing & subnetting** — calculating network ranges and host limits
- **Switches & routers** — how packets are forwarded at Layer 2 and Layer 3
- **DHCP & DNS** — how devices get addresses and resolve names
- **Basic network security** — port security, disabling unused ports

## 🛠️ Tools Used

- **Cisco Packet Tracer** — network simulation
- **Cisco IOS CLI** — device configuration commands

## 💡 Sample IOS Commands

```bash
# Basic router config
Router> enable
Router# configure terminal
Router(config)# hostname R1
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown

# Show routing table
Router# show ip route
```

## Weak Subjects
    Communication Principles
    The Access Layer

## 🔗 Course Link

[Cisco Networking Basics — Skills for All](https://www.netacad.com/courses/networking-basics)
