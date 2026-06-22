# Networking Labs

## Introduction

This section contains hands-on networking labs designed for beginners and intermediate learners. These labs help reinforce concepts learned in networking theory by applying them in practical environments.

Recommended Tools:

* Cisco Packet Tracer
* GNS3
* EVE-NG
* VMware Workstation
* VirtualBox
* Wireshark

---

# Lab 01 – Verify Network Connectivity

## Objective

Learn how to test connectivity between devices.

## Topology

```text id="lab1a"
PC1 -------- Router -------- PC2
```

## Steps

### Windows

```cmd id="lab1b"
ipconfig
```

Check:

* IP Address
* Subnet Mask
* Default Gateway

### Ping Localhost

```cmd id="lab1c"
ping 127.0.0.1
```

Expected:

```text id="lab1d"
Reply from 127.0.0.1
```

### Ping Gateway

```cmd id="lab1e"
ping 192.168.1.1
```

### Ping Google DNS

```cmd id="lab1f"
ping 8.8.8.8
```

### Ping Domain

```cmd id="lab1g"
ping google.com
```

---

# Lab 02 – IP Address Configuration

## Objective

Configure a static IP address.

### Windows

Open:

```text id="lab2a"
Control Panel
↓
Network and Sharing Center
↓
Adapter Settings
```

Configure:

```text id="lab2b"
IP Address : 192.168.1.10
Subnet Mask: 255.255.255.0
Gateway    : 192.168.1.1
DNS        : 8.8.8.8
```

Verify:

```cmd id="lab2c"
ipconfig
```

---

# Lab 03 – Subnetting Practice

## Objective

Calculate network information.

Given:

```text id="lab3a"
IP Address: 192.168.10.100
Subnet: /24
```

Find:

* Network Address
* Broadcast Address
* Usable Hosts

Solution:

```text id="lab3b"
Network Address : 192.168.10.0
Broadcast       : 192.168.10.255
Usable Range    : 192.168.10.1
                  to
                  192.168.10.254
```

---

# Lab 04 – DNS Testing

## Objective

Understand DNS resolution.

### Command

```cmd id="lab4a"
nslookup google.com
```

Output:

```text id="lab4b"
Server: dns.google
Address: 8.8.8.8
```

Try:

```cmd id="lab4c"
nslookup github.com
```

```cmd id="lab4d"
nslookup microsoft.com
```

---

# Lab 05 – DHCP Verification

## Objective

Verify DHCP assignment.

### Windows

```cmd id="lab5a"
ipconfig /all
```

Look for:

```text id="lab5b"
DHCP Enabled : Yes
```

Release Lease:

```cmd id="lab5c"
ipconfig /release
```

Renew Lease:

```cmd id="lab5d"
ipconfig /renew
```

---

# Lab 06 – Traceroute

## Objective

View packet path through the network.

### Windows

```cmd id="lab6a"
tracert google.com
```

### Linux

```bash id="lab6b"
traceroute google.com
```

Observe:

* Number of hops
* Latency
* Routing path

---

# Lab 07 – ARP Table Analysis

## Objective

View MAC-to-IP mappings.

### Windows

```cmd id="lab7a"
arp -a
```

Example:

```text id="lab7b"
192.168.1.1
00-aa-bb-cc-dd-ee
```

Learn:

* Gateway MAC
* Local device entries

---

# Lab 08 – Routing Table Inspection

## Objective

View routes used by the system.

### Windows

```cmd id="lab8a"
route print
```

### Linux

```bash id="lab8b"
ip route
```

Identify:

```text id="lab8c"
Default Route
Gateway
Local Routes
```

---

# Lab 09 – Wireshark Packet Capture

## Objective

Capture and analyze packets.

### Steps

1. Install Wireshark
2. Start Capture
3. Browse a website
4. Stop Capture

Filter DNS:

```text id="lab9a"
dns
```

Filter HTTP:

```text id="lab9b"
http
```

Filter TCP:

```text id="lab9c"
tcp
```

Observe:

* Source IP
* Destination IP
* Protocols
* Ports

---

# Lab 10 – Port Identification

## Objective

Identify active network services.

### Windows

```cmd id="lab10a"
netstat -ano
```

### Linux

```bash id="lab10b"
ss -tulnp
```

Common Ports:

```text id="lab10c"
21  FTP
22  SSH
23  Telnet
25  SMTP
53  DNS
80  HTTP
443 HTTPS
```

---

# Lab 11 – Cisco Packet Tracer LAN

## Objective

Build a simple LAN.

## Topology

```text id="lab11a"
PC1
  \
   Switch
  /
PC2
```

### Configure

PC1:

```text id="lab11b"
192.168.1.10
255.255.255.0
```

PC2:

```text id="lab11c"
192.168.1.20
255.255.255.0
```

Test:

```text id="lab11d"
ping 192.168.1.20
```

Expected:

```text id="lab11e"
Successful Replies
```

---

# Lab 12 – Router Configuration (Packet Tracer)

## Objective

Connect two networks.

### Network A

```text id="lab12a"
192.168.1.0/24
```

### Network B

```text id="lab12b"
192.168.2.0/24
```

Router Interfaces:

```text id="lab12c"
G0/0 = 192.168.1.1
G0/1 = 192.168.2.1
```

Cisco Commands:

```text id="lab12d"
enable

configure terminal

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown

interface g0/1
ip address 192.168.2.1 255.255.255.0
no shutdown
```

Test connectivity using ping.

---

# Lab 13 – VLAN Configuration

## Objective

Create network segmentation.

### VLAN 10

```text id="lab13a"
HR Department
```

### VLAN 20

```text id="lab13b"
IT Department
```

Cisco Commands:

```text id="lab13c"
enable

configure terminal

vlan 10
name HR

vlan 20
name IT
```

Assign ports accordingly.

---

# Lab 14 – Wireless Network Lab

## Objective

Analyze Wi-Fi configuration.

Check:

```text id="lab14a"
SSID
Channel
Security Type
Signal Strength
```

Verify:

```text id="lab14b"
WPA2 or WPA3 Enabled
```

---

# Lab 15 – Troubleshooting Challenge

## Scenario

User reports:

```text id="lab15a"
Internet not working
```

Checklist:

1. Check cable
2. Check IP address
3. Check gateway
4. Check DNS
5. Ping gateway
6. Ping 8.8.8.8
7. Ping google.com

Identify where communication fails.

---

# Lab Completion Checklist

After completing these labs, you should understand:

✅ IP Addressing

✅ Subnetting

✅ DNS

✅ DHCP

✅ Routing

✅ Switching

✅ VLANs

✅ Wireshark

✅ Network Troubleshooting

✅ Basic Cisco Configuration

---

# Final Goal

By completing all labs, you will gain practical networking experience useful for:

* Network Engineering
* System Administration
* Cloud Engineering
* DevOps
* Cybersecurity
* CCNA Preparation
* Network+ Preparation

The more you practice these labs, the easier it becomes to understand real-world enterprise networks.
