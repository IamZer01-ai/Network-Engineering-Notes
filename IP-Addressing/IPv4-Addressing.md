# IPv4 Addressing

## Introduction

IPv4 (Internet Protocol Version 4) is the most widely used addressing system in computer networks. It provides a unique logical address to every device connected to a network, allowing devices to communicate with each other.

An IPv4 address is a 32-bit number represented in dotted-decimal notation.

Example:

```text
192.168.1.10
```

Each IPv4 address consists of four octets separated by periods.

```text
192.168.1.10
│   │   │   │
8b  8b  8b  8b
```

Total:

```text
8 + 8 + 8 + 8 = 32 bits
```

---

## Purpose of IP Addressing

* Identify devices on a network
* Enable communication between networks
* Support routing
* Deliver data to the correct destination

---

## Structure of an IPv4 Address

Example:

```text
192.168.1.10
```

This address contains:

### Network Portion

Identifies the network.

### Host Portion

Identifies the device within the network.

Example:

```text
192.168.1.0
        ↑
     Network

192.168.1.10
          ↑
         Host
```

---

## Binary Representation

Decimal:

```text
192.168.1.10
```

Binary:

```text
11000000.10101000.00000001.00001010
```

---

## IPv4 Address Classes

### Class A

Range:

```text
1.0.0.0 – 126.255.255.255
```

Default Mask:

```text
255.0.0.0
```

CIDR:

```text
/8
```

Example:

```text
10.1.1.1
```

Large organizations and ISPs.

---

### Class B

Range:

```text
128.0.0.0 – 191.255.255.255
```

Default Mask:

```text
255.255.0.0
```

CIDR:

```text
/16
```

Example:

```text
172.16.10.1
```

Medium-sized organizations.

---

### Class C

Range:

```text
192.0.0.0 – 223.255.255.255
```

Default Mask:

```text
255.255.255.0
```

CIDR:

```text
/24
```

Example:

```text
192.168.1.1
```

Small networks.

---

### Class D

Range:

```text
224.0.0.0 – 239.255.255.255
```

Used for:

```text
Multicast
```

---

### Class E

Range:

```text
240.0.0.0 – 255.255.255.255
```

Reserved for research.

---

## Private IP Addresses

Private addresses cannot be routed directly on the Internet.

### Class A Private Range

```text
10.0.0.0 – 10.255.255.255
```

### Class B Private Range

```text
172.16.0.0 – 172.31.255.255
```

### Class C Private Range

```text
192.168.0.0 – 192.168.255.255
```

Examples:

```text
192.168.1.100
10.0.0.5
172.16.10.20
```

---

## Public IP Addresses

Public IP addresses are globally unique and accessible over the Internet.

Example:

```text
8.8.8.8
1.1.1.1
```

Used by:

* Websites
* Servers
* Cloud Services

---

## Special IPv4 Addresses

### Loopback Address

```text
127.0.0.1
```

Used to test the local machine.

Command:

```bash
ping 127.0.0.1
```

---

### Default Route

```text
0.0.0.0
```

Represents all networks.

---

### Broadcast Address

Example:

```text
192.168.1.255
```

Used to send data to all hosts on a network.

---

### APIPA

Automatic Private IP Addressing.

Range:

```text
169.254.0.0 – 169.254.255.255
```

Assigned when DHCP fails.

Example:

```text
169.254.10.20
```

---

## Subnet Mask

A subnet mask separates the network portion from the host portion.

Example:

```text
IP Address : 192.168.1.10
Subnet Mask: 255.255.255.0
```

Binary:

```text
11111111.11111111.11111111.00000000
```

Meaning:

```text
Network = 192.168.1
Host    = 10
```

---

## Common Subnet Masks

| CIDR | Subnet Mask     |
| ---- | --------------- |
| /8   | 255.0.0.0       |
| /16  | 255.255.0.0     |
| /24  | 255.255.255.0   |
| /25  | 255.255.255.128 |
| /26  | 255.255.255.192 |
| /27  | 255.255.255.224 |
| /28  | 255.255.255.240 |
| /29  | 255.255.255.248 |
| /30  | 255.255.255.252 |

---

## Default Gateway

A gateway is the router that forwards traffic to other networks.

Example:

```text
PC IP Address: 192.168.1.10
Gateway      : 192.168.1.1
```

Without a gateway, the device cannot reach external networks.

---

## DNS Server

DNS converts domain names into IP addresses.

Example:

```text
google.com
     ↓
142.250.x.x
```

Popular DNS Servers:

Google:

```text
8.8.8.8
8.8.4.4
```

Cloudflare:

```text
1.1.1.1
1.0.0.1
```

---

## Checking IP Configuration

### Windows

```cmd
ipconfig
```

Detailed:

```cmd
ipconfig /all
```

---

### Linux

```bash
ip addr
```

or

```bash
ifconfig
```

---

## Connectivity Testing

### Ping

```bash
ping google.com
```

### Gateway Test

```bash
ping 192.168.1.1
```

### DNS Test

```bash
nslookup google.com
```

---

## Common IPv4 Problems

### Duplicate IP Address

Two devices share the same IP.

Symptoms:

* Connectivity issues
* Network conflicts

---

### Incorrect Subnet Mask

Devices cannot communicate correctly.

---

### Wrong Default Gateway

Internet access fails.

---

### DNS Issues

Websites fail to load.

---

## Interview Questions

### What is IPv4?

A 32-bit logical addressing system used to identify devices on a network.

### How many bits are in an IPv4 address?

32 bits.

### What is a private IP address?

An address used internally within private networks.

### What is the purpose of a subnet mask?

To separate network and host portions of an IP address.

### What is 127.0.0.1?

The loopback address.

### What is APIPA?

Automatic Private IP Addressing assigned when DHCP fails.

---

## Summary

IPv4 is the foundation of modern networking. It uses 32-bit addresses to uniquely identify devices and enable communication across networks. Understanding IP addressing, subnet masks, gateways, private/public addresses, and DNS is essential for network administration, cybersecurity, and cloud networking.
