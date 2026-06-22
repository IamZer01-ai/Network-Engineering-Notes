# Switching

## Introduction

Switching is the process of forwarding data frames between devices within a Local Area Network (LAN). A network switch connects computers, servers, printers, access points, and other devices, enabling efficient communication within a network.

Unlike hubs, switches intelligently forward traffic only to the intended destination, improving performance and security.

---

# What is a Switch?

A switch is a Layer 2 (Data Link Layer) networking device that uses MAC addresses to forward frames between devices.

Example:

```text
PC1 ──┐
       │
PC2 ── Switch ── Server
       │
PC3 ──┘
```

Functions:

* Connect devices in a LAN
* Learn MAC addresses
* Forward frames
* Reduce collisions
* Support VLANs

---

# Why Switching is Important

Benefits:

* Faster communication
* Better network performance
* Reduced network congestion
* Improved security
* Efficient traffic forwarding

---

# How Switching Works

When a device sends data:

1. Frame arrives at switch.
2. Switch reads destination MAC address.
3. Switch checks MAC Address Table.
4. Switch forwards frame to correct port.

Example:

```text
PC1 → Switch → PC2
```

Instead of sending traffic to all devices, the switch sends it only to PC2.

---

# MAC Address

A MAC (Media Access Control) Address is a unique identifier assigned to a network interface card (NIC).

Example:

```text
00:1A:2B:3C:4D:5E
```

Characteristics:

* 48-bit address
* Layer 2 identifier
* Assigned by manufacturer
* Unique per device

---

# MAC Address Table

Switches maintain a MAC Address Table.

Example:

| MAC Address       | Port  |
| ----------------- | ----- |
| 00:11:22:33:44:55 | Fa0/1 |
| 00:AA:BB:CC:DD:EE | Fa0/2 |
| 00:FF:EE:DD:CC:BB | Fa0/3 |

Purpose:

* Learn device locations
* Forward traffic efficiently

---

# MAC Learning Process

### Step 1

PC1 sends data.

```text
Source MAC:
00:11:22:33:44:55
```

Switch learns:

```text
00:11:22:33:44:55 → Fa0/1
```

---

### Step 2

PC2 sends data.

Switch learns:

```text
00:AA:BB:CC:DD:EE → Fa0/2
```

---

### Step 3

Switch builds MAC Table.

Traffic is now forwarded efficiently.

---

# Frame Forwarding

## Known Unicast

Destination MAC exists in table.

Example:

```text
PC1 → PC2
```

Switch forwards frame only to PC2.

---

## Unknown Unicast

Destination MAC not in table.

Switch floods traffic to all ports except incoming port.

---

## Broadcast

Broadcast Address:

```text
FF:FF:FF:FF:FF:FF
```

Switch sends frame to all ports.

Examples:

* ARP Requests
* DHCP Discover

---

## Multicast

Traffic sent to a specific group of devices.

Examples:

* Video Streaming
* IPTV

---

# Collision Domains

A collision occurs when multiple devices transmit simultaneously.

Switches create separate collision domains.

Example:

```text
PC1 → Port1
PC2 → Port2
PC3 → Port3
```

Each port has its own collision domain.

Benefits:

* Better Performance
* Reduced Network Issues

---

# Broadcast Domain

A broadcast domain is a group of devices receiving broadcast traffic.

Without VLANs:

```text
All Devices
     ↓
One Broadcast Domain
```

With VLANs:

```text
VLAN 10
VLAN 20
VLAN 30
```

Separate broadcast domains.

---

# Switching Methods

## Store-and-Forward

Switch receives entire frame before forwarding.

Advantages:

* Error checking
* Reliable

Disadvantages:

* Slightly slower

---

## Cut-Through

Switch forwards frame immediately after reading destination MAC.

Advantages:

* Faster

Disadvantages:

* May forward corrupted frames

---

## Fragment-Free

Checks first 64 bytes before forwarding.

Provides balance between speed and reliability.

---

# VLAN (Virtual Local Area Network)

A VLAN logically separates devices within the same switch.

Example:

```text
VLAN 10 → HR
VLAN 20 → IT
VLAN 30 → Finance
```

Benefits:

* Security
* Segmentation
* Reduced Broadcast Traffic

---

# VLAN Example

Without VLANs:

```text
All PCs
    ↓
One Network
```

With VLANs:

```text
HR PCs      → VLAN 10
IT PCs      → VLAN 20
Finance PCs → VLAN 30
```

---

# Access Port

An access port belongs to one VLAN.

Example:

```text
Fa0/1 → VLAN 10
```

Connected Devices:

* PC
* Printer
* IP Phone

---

# Trunk Port

A trunk port carries multiple VLANs.

Example:

```text
Switch1 ←→ Switch2
```

Allows VLAN traffic between switches.

---

# Spanning Tree Protocol (STP)

STP prevents Layer 2 loops.

Problem:

```text
Switch A
 ↕      ↕
Switch B
```

Loops can cause:

* Broadcast Storms
* Network Failure

Solution:

```text
STP blocks redundant paths
```

---

# Port States in STP

### Blocking

Does not forward traffic.

### Listening

Preparing to forward traffic.

### Learning

Learning MAC addresses.

### Forwarding

Actively forwarding traffic.

### Disabled

Administratively shut down.

---

# EtherChannel

Combines multiple links into one logical link.

Example:

```text
Link1
Link2
Link3
 ↓
EtherChannel
```

Benefits:

* Increased Bandwidth
* Redundancy
* Load Balancing

---

# Common Switch Commands (Cisco)

View MAC Table:

```bash
show mac address-table
```

View VLANs:

```bash
show vlan brief
```

View Interfaces:

```bash
show interfaces status
```

View STP Information:

```bash
show spanning-tree
```

View EtherChannel:

```bash
show etherchannel summary
```

---

# Basic VLAN Configuration

Create VLAN:

```bash
enable

configure terminal

vlan 10
name HR
```

Assign Port:

```bash
interface fa0/1

switchport mode access

switchport access vlan 10
```

Verify:

```bash
show vlan brief
```

---

# Troubleshooting Switching Issues

## Port Down

Check:

```bash
show interfaces status
```

---

## Wrong VLAN Assignment

Verify:

```bash
show vlan brief
```

---

## MAC Address Learning Issues

Check:

```bash
show mac address-table
```

---

## STP Blocking Unexpected Ports

Verify:

```bash
show spanning-tree
```

---

# Interview Questions

### What is a Switch?

A Layer 2 device that forwards frames using MAC addresses.

### What is a MAC Address?

A unique hardware address assigned to a network interface.

### What is a VLAN?

A logical separation of devices into different networks.

### What is a Trunk Port?

A port that carries multiple VLANs.

### What is STP?

Spanning Tree Protocol prevents Layer 2 loops.

### What is EtherChannel?

A technology that bundles multiple links into a single logical connection.

### Difference Between Hub and Switch?

Hub broadcasts to all devices.

Switch forwards only to the intended destination.

---

# Summary

Switching is a fundamental networking technology that enables efficient communication within Local Area Networks. Switches use MAC addresses and switching tables to forward frames intelligently. Key concepts include MAC learning, VLANs, Trunking, STP, EtherChannel, Collision Domains, and Broadcast Domains. Mastering switching is essential for Network Engineers, CCNA candidates, Cybersecurity professionals, and IT administrators.
