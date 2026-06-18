# OSI Model

## Introduction

The Open Systems Interconnection (OSI) Model is a conceptual framework developed by the International Organization for Standardization (ISO) to standardize network communication. It divides the communication process into seven layers, making it easier to understand, design, and troubleshoot networks.

The OSI model helps network engineers identify where communication problems occur and provides a common language for discussing networking technologies.

---

## Purpose of the OSI Model

* Standardize network communication
* Enable interoperability between different vendors
* Simplify troubleshooting
* Provide a structured approach to networking
* Assist in network design and implementation

---

## The Seven Layers of the OSI Model

```text
7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. Data Link
1. Physical
```

Data moves from Layer 7 to Layer 1 when sending and from Layer 1 to Layer 7 when receiving.

---

## Layer 1 – Physical Layer

### Function

The Physical Layer is responsible for transmitting raw bits over a physical medium.

### Responsibilities

* Electrical signals
* Physical cabling
* Connectors
* Data transmission
* Signal conversion

### Devices

* Hubs
* Repeaters
* Cables
* Fiber optics

### Protocols/Standards

* Ethernet Physical Standards
* USB
* DSL

### Data Unit

**Bits**

---

## Layer 2 – Data Link Layer

### Function

Provides node-to-node communication and handles error detection.

### Responsibilities

* MAC addressing
* Framing
* Error detection
* Switching

### Devices

* Switches
* Bridges

### Protocols

* Ethernet
* PPP
* Frame Relay

### Address Used

**MAC Address**

Example:

```text
00:1A:2B:3C:4D:5E
```

### Data Unit

**Frame**

---

## Layer 3 – Network Layer

### Function

Responsible for logical addressing and routing packets between networks.

### Responsibilities

* IP addressing
* Routing
* Packet forwarding
* Path selection

### Devices

* Routers
* Layer 3 Switches

### Protocols

* IPv4
* IPv6
* ICMP
* OSPF
* BGP

### Address Used

**IP Address**

Example:

```text
192.168.1.10
```

### Data Unit

**Packet**

---

## Layer 4 – Transport Layer

### Function

Provides reliable data transfer between devices.

### Responsibilities

* Segmentation
* Flow control
* Error recovery
* End-to-end communication

### Protocols

#### TCP

Features:

* Reliable
* Connection-oriented
* Error checking
* Acknowledgments

Examples:

* HTTPS
* SSH
* FTP

#### UDP

Features:

* Fast
* Connectionless
* No acknowledgments

Examples:

* DNS
* VoIP
* Online Gaming

### Address Used

**Port Numbers**

Examples:

```text
HTTP  = 80
HTTPS = 443
SSH   = 22
DNS   = 53
FTP   = 21
```

### Data Unit

**Segment**

---

## Layer 5 – Session Layer

### Function

Establishes, manages, and terminates communication sessions.

### Responsibilities

* Session creation
* Session maintenance
* Session termination
* Authentication support

### Examples

* Remote Desktop Sessions
* SQL Sessions
* NetBIOS

### Data Unit

**Data**

---

## Layer 6 – Presentation Layer

### Function

Translates data between applications and the network.

### Responsibilities

* Encryption
* Decryption
* Compression
* Data formatting

### Examples

* SSL/TLS
* JPEG
* PNG
* ASCII
* Unicode

### Data Unit

**Data**

---

## Layer 7 – Application Layer

### Function

Provides network services directly to users and applications.

### Responsibilities

* User interaction
* Network services
* Application communication

### Protocols

* HTTP
* HTTPS
* FTP
* DNS
* SMTP
* POP3
* IMAP
* SSH

### Examples

* Web Browsers
* Email Clients
* File Transfer Applications

### Data Unit

**Data**

---

## OSI Encapsulation Process

When sending data:

```text
Application Data
       ↓
Presentation Data
       ↓
Session Data
       ↓
Transport Segment
       ↓
Network Packet
       ↓
Data Link Frame
       ↓
Physical Bits
```

When receiving:

```text
Bits
 ↓
Frame
 ↓
Packet
 ↓
Segment
 ↓
Data
```

---

## OSI Troubleshooting Examples

### Cannot Access Website

Check:

* Layer 1: Cable connected?
* Layer 2: Switch functioning?
* Layer 3: IP address configured?
* Layer 4: Port 443 open?
* Layer 7: Web server running?

---

### No Internet Access

Check:

* Physical connection
* Default gateway
* DNS settings
* Router configuration

---

## Memory Trick

### Top to Bottom

```text
All
People
Seem
To
Need
Data
Processing
```

### Bottom to Top

```text
Please
Do
Not
Throw
Sausage
Pizza
Away
```

---

## OSI vs TCP/IP

| OSI Model        | TCP/IP Model     |
| ---------------- | ---------------- |
| 7 Layers         | 4 Layers         |
| Reference Model  | Practical Model  |
| Developed by ISO | Developed by DoD |
| More Detailed    | Simpler          |

---

## Interview Questions

### What is the OSI Model?

A seven-layer framework used to understand and standardize network communication.

### Which layer uses IP addresses?

Layer 3 – Network Layer.

### Which layer uses MAC addresses?

Layer 2 – Data Link Layer.

### Which layer handles routing?

Layer 3 – Network Layer.

### Which layer handles encryption?

Layer 6 – Presentation Layer.

### Which layer interacts with users?

Layer 7 – Application Layer.

---

## Summary

The OSI Model divides network communication into seven layers. Each layer performs specific functions that enable reliable communication between devices. Understanding the OSI model is essential for network design, troubleshooting, cybersecurity, and professional networking certifications such as CCNA, Network+, and CCNP.
