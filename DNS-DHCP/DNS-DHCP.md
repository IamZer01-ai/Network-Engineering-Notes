# DNS & DHCP

## Introduction

DNS (Domain Name System) and DHCP (Dynamic Host Configuration Protocol) are two of the most important services in modern networking.

* **DNS** translates domain names into IP addresses.
* **DHCP** automatically assigns IP addresses and network settings to devices.

Without DNS, users would need to remember IP addresses. Without DHCP, network administrators would have to manually configure every device.

---

# What is DNS?

DNS stands for **Domain Name System**.

It acts like the Internet's phonebook.

Example:

```text
google.com
      ↓
142.250.190.78
```

Instead of remembering an IP address, users type a domain name.

---

# Why DNS is Important

Benefits:

* Easy-to-remember names
* Faster access to resources
* Centralized name management
* Supports websites, email, and cloud services

Example:

```text
www.google.com
www.github.com
www.microsoft.com
```

Much easier than remembering:

```text
142.250.x.x
140.82.x.x
20.x.x.x
```

---

# DNS Components

## Domain Name

Example:

```text
www.example.com
```

Parts:

```text
www      = Hostname
example  = Domain
com      = Top-Level Domain (TLD)
```

---

## DNS Server

A DNS server stores DNS records and responds to queries.

Examples:

Google DNS:

```text
8.8.8.8
8.8.4.4
```

Cloudflare DNS:

```text
1.1.1.1
1.0.0.1
```

---

# DNS Resolution Process

When a user visits:

```text
www.google.com
```

The process is:

```text
User
 ↓
Local DNS Cache
 ↓
DNS Resolver
 ↓
Root Server
 ↓
TLD Server (.com)
 ↓
Authoritative DNS Server
 ↓
IP Address Returned
 ↓
Website Opens
```

---

# Common DNS Record Types

## A Record

Maps a hostname to an IPv4 address.

Example:

```text
example.com → 192.168.1.10
```

---

## AAAA Record

Maps a hostname to an IPv6 address.

Example:

```text
example.com → 2001:db8::1
```

---

## CNAME Record

Alias for another hostname.

Example:

```text
www.example.com
      ↓
example.com
```

---

## MX Record

Mail Exchange Record.

Used for email routing.

Example:

```text
example.com
      ↓
mail.example.com
```

---

## NS Record

Specifies authoritative name servers.

Example:

```text
ns1.example.com
ns2.example.com
```

---

## TXT Record

Stores text information.

Commonly used for:

* SPF
* DKIM
* Domain verification

---

# DNS Commands

## Windows

```cmd
nslookup google.com
```

Example Output:

```text
Name: google.com
Address: 142.250.x.x
```

---

## Linux

```bash
dig google.com
```

or

```bash
nslookup google.com
```

---

# Common DNS Problems

## DNS Server Unreachable

Symptoms:

* Websites fail to load
* Internet partially works

---

## Incorrect DNS Records

Symptoms:

* Website points to wrong server

---

## DNS Cache Issues

Fix:

Windows:

```cmd
ipconfig /flushdns
```

Linux:

```bash
sudo systemd-resolve --flush-caches
```

---

# What is DHCP?

DHCP stands for:

```text
Dynamic Host Configuration Protocol
```

DHCP automatically assigns:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

to devices joining a network.

---

# Why DHCP is Important

Without DHCP:

Every device must be configured manually.

With DHCP:

Devices automatically receive settings.

Benefits:

* Easier administration
* Reduced errors
* Faster deployment

---

# DHCP Components

## DHCP Server

Responsible for assigning network information.

Examples:

* Windows Server DHCP
* Linux DHCP Server
* Home Router DHCP

---

## DHCP Client

Device requesting network settings.

Examples:

* Laptop
* Desktop
* Smartphone
* Printer

---

# DHCP DORA Process

The DHCP process consists of four steps:

```text
DORA
```

---

## Discover

Client broadcasts:

```text
DHCP Discover
```

Meaning:

```text
"Is there a DHCP server available?"
```

---

## Offer

DHCP Server responds:

```text
DHCP Offer
```

Meaning:

```text
"I can provide this IP address."
```

Example:

```text
192.168.1.100
```

---

## Request

Client requests the offered IP.

```text
DHCP Request
```

Meaning:

```text
"I would like to use this address."
```

---

## Acknowledge

Server confirms assignment.

```text
DHCP ACK
```

Meaning:

```text
"IP address assigned successfully."
```

---

# DHCP DORA Diagram

```text
Client
  ↓ Discover
Server
  ↑ Offer
Client
  ↓ Request
Server
  ↑ Acknowledge
Client Connected
```

---

# DHCP Lease

A DHCP lease is the time a device may use an assigned IP address.

Example:

```text
24 Hours
7 Days
30 Days
```

When the lease expires:

The client requests renewal.

---

# DHCP Scope

A scope defines available addresses.

Example:

```text
192.168.1.100
to
192.168.1.200
```

DHCP assigns addresses only from this range.

---

# Reserved IP Addresses

Specific devices may always receive the same IP.

Examples:

* Servers
* Printers
* Cameras

Example:

```text
Printer
MAC: 00:11:22:33:44:55

Reserved IP:
192.168.1.10
```

---

# Common DHCP Problems

## DHCP Server Down

Symptoms:

```text
No IP Address Assigned
```

---

## APIPA Address

Windows automatically assigns:

```text
169.254.x.x
```

Meaning:

```text
DHCP Failed
```

---

## Address Pool Exhausted

No available addresses remain.

Result:

```text
New devices cannot connect
```

---

# Useful Commands

## Windows

View Configuration:

```cmd
ipconfig /all
```

Renew DHCP Lease:

```cmd
ipconfig /renew
```

Release Current Lease:

```cmd
ipconfig /release
```

---

## Linux

View Address:

```bash
ip addr
```

Renew DHCP:

```bash
sudo dhclient
```

---

# DNS vs DHCP

| DNS             | DHCP                    |
| --------------- | ----------------------- |
| Resolves names  | Assigns IP addresses    |
| Domain → IP     | Automatic IP assignment |
| Uses Port 53    | Uses Ports 67/68        |
| Name Resolution | Network Configuration   |

---

# Real-World Example

User opens:

```text
www.github.com
```

### Step 1

DHCP assigns:

```text
IP Address
Subnet Mask
Gateway
DNS Server
```

### Step 2

DNS translates:

```text
www.github.com
        ↓
140.82.x.x
```

### Step 3

Browser connects to the website.

---

# Interview Questions

### What is DNS?

A system that translates domain names into IP addresses.

### What port does DNS use?

Port 53.

### What is DHCP?

A protocol that automatically assigns network settings to devices.

### What ports does DHCP use?

Ports 67 and 68.

### What does DORA stand for?

* Discover
* Offer
* Request
* Acknowledge

### What is APIPA?

Automatic Private IP Addressing (169.254.x.x) assigned when DHCP fails.

---

# Summary

DNS and DHCP are critical networking services. DNS provides name resolution by converting domain names into IP addresses, while DHCP automates network configuration by assigning IP addresses and other settings. Together, they make modern network communication efficient, scalable, and easy to manage.
