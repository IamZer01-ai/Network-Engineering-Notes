# TCP/IP Model

## Introduction

The TCP/IP Model (Transmission Control Protocol/Internet Protocol) is the foundation of modern networking and the Internet. It defines how data is transmitted between devices across networks.

Unlike the OSI Model, which is primarily a reference framework, TCP/IP is the practical model used in real-world networks.

The TCP/IP model was developed by the United States Department of Defense (DoD) and forms the basis of communication on the Internet.

---

## Purpose of TCP/IP

* Standardize communication between devices
* Enable interoperability between different systems
* Support routing across multiple networks
* Provide reliable data transmission
* Form the foundation of Internet communication

---

## TCP/IP Layers

The TCP/IP Model consists of four layers:

```text
Application Layer
Transport Layer
Internet Layer
Network Access Layer
```

---

## Layer 4 – Application Layer

### Function

Provides network services directly to applications and users.

This layer combines the functions of the OSI:

* Application Layer
* Presentation Layer
* Session Layer

### Responsibilities

* User interaction
* Data formatting
* Session management
* Authentication
* Application services

### Common Protocols

#### HTTP

Used for web communication.

Default Port:

```text
80
```

#### HTTPS

Secure web communication using SSL/TLS.

Default Port:

```text
443
```

#### DNS

Translates domain names into IP addresses.

Default Port:

```text
53
```

#### FTP

File transfer protocol.

Default Port:

```text
21
```

#### SMTP

Email sending protocol.

Default Port:

```text
25
```

#### SSH

Secure remote administration.

Default Port:

```text
22
```

---

## Layer 3 – Transport Layer

### Function

Provides end-to-end communication between devices.

### Responsibilities

* Segmentation
* Error detection
* Flow control
* Reliability
* Port addressing

---

## TCP (Transmission Control Protocol)

### Characteristics

* Connection-oriented
* Reliable
* Ordered delivery
* Error checking
* Acknowledgment-based

### Three-Way Handshake

```text
Client → SYN
Server → SYN-ACK
Client → ACK
```

Connection established.

### Common TCP Applications

* HTTPS
* SSH
* FTP
* SMTP

---

## UDP (User Datagram Protocol)

### Characteristics

* Connectionless
* Fast
* No acknowledgments
* Lower overhead

### Common UDP Applications

* DNS
* VoIP
* Video Streaming
* Online Gaming

---

## Port Numbers

### Well-Known Ports

| Service | Port  |
| ------- | ----- |
| HTTP    | 80    |
| HTTPS   | 443   |
| FTP     | 21    |
| SSH     | 22    |
| DNS     | 53    |
| SMTP    | 25    |
| DHCP    | 67/68 |

---

## Layer 2 – Internet Layer

### Function

Responsible for logical addressing and routing packets.

### Responsibilities

* Routing
* IP Addressing
* Packet forwarding
* Path determination

### Protocols

#### IPv4

Example:

```text
192.168.1.100
```

#### IPv6

Example:

```text
2001:db8::1
```

#### ICMP

Used for diagnostics.

Examples:

* Ping
* Traceroute

#### ARP

Maps IP addresses to MAC addresses.

---

## IP Packet Structure

Contains:

* Source IP Address
* Destination IP Address
* Protocol Information
* Payload Data

Example:

```text
Source IP      : 192.168.1.10
Destination IP : 8.8.8.8
```

---

## Layer 1 – Network Access Layer

### Function

Handles communication on the physical network.

This layer combines the OSI:

* Physical Layer
* Data Link Layer

### Responsibilities

* Physical transmission
* Framing
* MAC addressing
* Error detection

### Devices

* Switches
* Network Interface Cards (NICs)
* Access Points

### Technologies

* Ethernet
* Wi-Fi
* Fiber Optics

---

## Encapsulation Process

When data is sent:

```text
Application Data
      ↓
TCP/UDP Segment
      ↓
IP Packet
      ↓
Ethernet Frame
      ↓
Bits
```

When received:

```text
Bits
 ↓
Frame
 ↓
Packet
 ↓
Segment
 ↓
Application Data
```

---

## TCP/IP vs OSI Model

| TCP/IP            | OSI                   |
| ----------------- | --------------------- |
| 4 Layers          | 7 Layers              |
| Practical Model   | Reference Model       |
| Internet Standard | Educational Framework |
| Real-World Usage  | Conceptual Usage      |

### Layer Mapping

| TCP/IP Layer   | OSI Layer |
| -------------- | --------- |
| Application    | 7,6,5     |
| Transport      | 4         |
| Internet       | 3         |
| Network Access | 2,1       |

---

## Common Commands

### Check IP Address

Windows:

```cmd
ipconfig
```

Linux:

```bash
ip addr
```

---

### Test Connectivity

```bash
ping google.com
```

---

### View Routing Table

Windows:

```cmd
route print
```

Linux:

```bash
ip route
```

---

### DNS Lookup

```bash
nslookup google.com
```

---

## Troubleshooting Using TCP/IP

### No Internet Access

Check:

1. Physical connection
2. IP configuration
3. Default gateway
4. DNS server
5. Router connectivity

### Website Not Loading

Check:

1. DNS resolution
2. HTTPS port access
3. Internet connectivity
4. Firewall rules

---

## Interview Questions

### What does TCP/IP stand for?

Transmission Control Protocol / Internet Protocol.

### Which protocol provides reliable communication?

TCP.

### Which protocol is faster?

UDP.

### Which layer performs routing?

Internet Layer.

### Which protocol resolves domain names?

DNS.

### Which protocol is used by Ping?

ICMP.

---

## Summary

The TCP/IP Model is the foundation of modern networking and Internet communication. It consists of four layers: Application, Transport, Internet, and Network Access. Understanding TCP/IP is essential for Network Engineers, System Administrators, Cloud Engineers, and Cybersecurity Professionals.
