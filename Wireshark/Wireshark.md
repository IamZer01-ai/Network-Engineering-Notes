# Wireshark

## Introduction

Wireshark is one of the most popular network protocol analyzers used by Network Engineers, System Administrators, Security Analysts, and Cybersecurity Professionals.

It allows users to capture, inspect, and analyze network traffic in real time.

Wireshark helps understand:

* Network Communication
* Troubleshooting Issues
* Protocol Analysis
* Performance Monitoring
* Security Investigations

---

# What is Wireshark?

Wireshark is an open-source packet analysis tool.

Functions:

* Capture Network Traffic
* Analyze Packets
* Inspect Protocols
* Troubleshoot Networks

Example:

```text
Laptop
   ↓
Network Traffic
   ↓
Wireshark
   ↓
Packet Analysis
```

---

# Why Use Wireshark?

Benefits:

* Network Troubleshooting
* Protocol Learning
* Security Monitoring
* Performance Analysis
* Packet Inspection

Used by:

* Network Engineers
* Security Analysts
* SOC Teams
* Penetration Testers
* System Administrators

---

# Packet Basics

A packet is a unit of data transmitted across a network.

Example:

```text
Application Data
      ↓
TCP/UDP Header
      ↓
IP Header
      ↓
Ethernet Header
      ↓
Packet Sent
```

Wireshark captures these packets for analysis.

---

# Installing Wireshark

## Windows

1. Download Wireshark
2. Install Npcap
3. Complete Installation
4. Launch Wireshark

---

## Linux

Ubuntu/Debian:

```bash
sudo apt update
sudo apt install wireshark
```

Verify:

```bash
wireshark --version
```

---

# Wireshark Interface Overview

Main Sections:

```text
Packet List Pane
       ↓
Packet Details Pane
       ↓
Packet Bytes Pane
```

---

## Packet List Pane

Displays captured packets.

Information:

* Packet Number
* Time
* Source
* Destination
* Protocol
* Length

Example:

```text
No.  Time     Source      Destination   Protocol
1    0.001    PC1         DNS Server    DNS
2    0.005    DNS Server  PC1           DNS
```

---

## Packet Details Pane

Displays protocol information.

Example:

```text
Ethernet
IP
TCP
HTTP
```

---

## Packet Bytes Pane

Displays raw packet data in hexadecimal format.

Example:

```text
45 00 00 54 ...
```

---

# Starting a Packet Capture

Step 1:

Select a network interface.

Examples:

```text
Ethernet
Wi-Fi
VPN Adapter
```

Step 2:

Click:

```text
Start Capture
```

Step 3:

Generate network traffic.

Example:

```text
Open Browser
Visit Website
```

Step 4:

Stop capture.

---

# Capture Filters

Capture filters reduce the amount of captured traffic.

Example:

Capture only DNS:

```text
port 53
```

Capture only HTTP:

```text
port 80
```

Capture specific host:

```text
host 192.168.1.10
```

---

# Display Filters

Display filters help analyze captured packets.

---

## Filter DNS Traffic

```text
dns
```

---

## Filter HTTP Traffic

```text
http
```

---

## Filter HTTPS Traffic

```text
tls
```

---

## Filter TCP Traffic

```text
tcp
```

---

## Filter UDP Traffic

```text
udp
```

---

## Filter ICMP Traffic

```text
icmp
```

---

## Filter Specific IP

```text
ip.addr == 192.168.1.10
```

---

## Filter Source IP

```text
ip.src == 192.168.1.10
```

---

## Filter Destination IP

```text
ip.dst == 192.168.1.20
```

---

# Common Protocols in Wireshark

## ARP

Used for IP-to-MAC resolution.

Example:

```text
Who has 192.168.1.1?
```

---

## ICMP

Used by Ping.

Example:

```text
Echo Request
Echo Reply
```

---

## DNS

Resolves domain names.

Example:

```text
google.com
    ↓
IP Address
```

---

## TCP

Reliable communication protocol.

Features:

* Connection-Oriented
* Error Recovery
* Ordered Delivery

---

## UDP

Fast communication protocol.

Features:

* Connectionless
* Low Overhead

Examples:

* DNS
* Streaming
* VoIP

---

## HTTP

Used for web traffic.

Default Port:

```text
80
```

---

## HTTPS

Secure web traffic.

Default Port:

```text
443
```

---

# TCP Three-Way Handshake

Wireshark commonly displays:

```text
Client → SYN
Server → SYN-ACK
Client → ACK
```

Example:

```text
Client
   ↓ SYN
Server
   ↑ SYN-ACK
Client
   ↓ ACK
Connection Established
```

---

# DNS Analysis

Capture:

```text
dns
```

Example:

```text
Query:
github.com
```

Response:

```text
140.82.x.x
```

Information Available:

* Domain Name
* Response Time
* DNS Server

---

# HTTP Analysis

Display Filter:

```text
http
```

Shows:

* Requests
* Responses
* Methods

Example:

```text
GET /index.html
```

---

# HTTPS Analysis

Display Filter:

```text
tls
```

Shows:

* TLS Handshake
* Certificates
* Encryption Negotiation

---

# Following TCP Streams

Useful for analyzing conversations.

Steps:

```text
Right Click Packet
      ↓
Follow
      ↓
TCP Stream
```

Displays:

* Client Requests
* Server Responses

---

# Exporting Captures

Save capture files:

```text
.pcap
.pcapng
```

Uses:

* Incident Analysis
* Troubleshooting
* Evidence Collection

---

# Network Troubleshooting with Wireshark

## DNS Problems

Filter:

```text
dns
```

Check:

* Queries
* Responses
* Errors

---

## Connectivity Problems

Filter:

```text
icmp
```

Verify:

```text
Ping Requests
Ping Replies
```

---

## Slow Applications

Analyze:

* Retransmissions
* Latency
* Packet Loss

---

# Security Analysis

Wireshark can help identify:

* Suspicious Traffic
* Malware Communication
* Unexpected Connections
* Unauthorized Devices

Indicators:

```text
Unknown IPs
Repeated Connections
High Traffic Volume
```

---

# Statistics Tools

Useful Menus:

```text
Statistics → Protocol Hierarchy
Statistics → Conversations
Statistics → Endpoints
```

Benefits:

* Traffic Analysis
* Bandwidth Usage
* Protocol Distribution

---

# Useful Display Filters Cheat Sheet

DNS:

```text
dns
```

HTTP:

```text
http
```

HTTPS/TLS:

```text
tls
```

TCP:

```text
tcp
```

UDP:

```text
udp
```

ICMP:

```text
icmp
```

Specific IP:

```text
ip.addr == 192.168.1.10
```

Specific Port:

```text
tcp.port == 443
```

Failed TCP:

```text
tcp.analysis.retransmission
```

---

# Best Practices

## Capture Only Needed Traffic

Use capture filters.

---

## Save Important Captures

Store:

```text
.pcapng
```

files securely.

---

## Analyze Methodically

Start with:

```text
DNS
↓
TCP
↓
Application Layer
```

---

## Document Findings

Record:

* Problem
* Evidence
* Solution

---

# Interview Questions

### What is Wireshark?

A network protocol analyzer used to capture and analyze packets.

### What is a packet?

A unit of network data transmitted across a network.

### Difference Between Capture Filter and Display Filter?

Capture Filter:

```text
Filters traffic before capture.
```

Display Filter:

```text
Filters traffic after capture.
```

### What protocol does Ping use?

```text
ICMP
```

### What filter displays DNS traffic?

```text
dns
```

### What is the TCP Three-Way Handshake?

```text
SYN
SYN-ACK
ACK
```

### What file formats does Wireshark save?

```text
.pcap
.pcapng
```

---

# Summary

Wireshark is a powerful network protocol analyzer used for packet capture, troubleshooting, protocol analysis, and security investigations. By understanding packet structures, filters, TCP handshakes, DNS analysis, HTTP/HTTPS traffic, and network statistics, professionals can diagnose issues and gain deep visibility into network communications. Wireshark is an essential tool for Network Engineers, Security Analysts, SOC Teams, and IT Administrators.
