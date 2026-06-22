# Wireless Security

## Introduction

Wireless Security refers to the technologies, policies, and practices used to protect wireless networks from unauthorized access, attacks, and data theft.

Wireless networks provide convenience and mobility, but because data travels through radio waves, they are more exposed to security risks than wired networks.

The primary goals of wireless security are:

* Confidentiality
* Integrity
* Availability
* Authentication

---

# What is a Wireless Network?

A wireless network allows devices to communicate without physical cables.

Examples:

* Home Wi-Fi
* Office Wi-Fi
* Public Hotspots
* Campus Networks

Basic Wireless Architecture:

```text
Laptop
   )))
Smartphone
   )))
Access Point
   )))
Internet
```

---

# Why Wireless Security is Important

Without proper security:

* Attackers can access networks
* Sensitive data can be intercepted
* Devices can be compromised
* Network resources can be abused

Examples:

* Password Theft
* Unauthorized Access
* Data Interception
* Rogue Access Points

---

# Wireless Security Fundamentals

## Authentication

Verifies user identity before granting access.

Examples:

* Passwords
* Certificates
* Multi-Factor Authentication

---

## Encryption

Protects wireless data from being read by attackers.

Example:

```text
Plain Text
    ↓
Encryption
    ↓
Cipher Text
```

Only authorized users can decrypt the information.

---

# Wireless Security Standards

## WEP (Wired Equivalent Privacy)

Introduced:

```text
1997
```

Features:

* Basic Encryption
* RC4 Algorithm

Problems:

* Weak Encryption
* Easily Cracked

Status:

```text
Obsolete
Not Recommended
```

---

## WPA (Wi-Fi Protected Access)

Introduced to replace WEP.

Features:

* Improved Security
* TKIP Encryption

Problems:

* Older Technology
* Less Secure Than WPA2

---

## WPA2

Most widely used wireless security standard.

Features:

* AES Encryption
* Strong Authentication
* Enterprise Support

Example:

```text
Home Wi-Fi
   ↓
WPA2-Personal
```

---

## WPA3

Latest wireless security standard.

Benefits:

* Stronger Encryption
* Better Password Protection
* Enhanced Authentication

Advantages:

* Protection Against Offline Attacks
* Improved Security for Public Networks

Recommended:

```text
WPA3
```

---

# Wireless Authentication Methods

## Open Authentication

No password required.

Example:

```text
Public Wi-Fi
```

Risks:

* Anyone Can Connect
* Data Exposure

---

## Pre-Shared Key (PSK)

Uses a shared password.

Example:

```text
WiFi Password:
Secure123!
```

Common in:

* Homes
* Small Offices

---

## Enterprise Authentication

Uses centralized authentication servers.

Example:

```text
User
  ↓
RADIUS Server
  ↓
Access Granted
```

Used in:

* Enterprises
* Universities
* Government Networks

---

# SSID Security

SSID stands for:

```text
Service Set Identifier
```

Example:

```text
Home-WiFi
Office-WLAN
```

Best Practices:

* Use Meaningful Names
* Avoid Personal Information
* Avoid Default Names

Bad Example:

```text
JohnsHomeWiFi
```

Better Example:

```text
BlueNetwork
```

---

# MAC Address Filtering

Allows only approved devices to connect.

Example:

```text
Allowed Device:
00:11:22:33:44:55
```

Advantages:

* Additional Control Layer

Disadvantages:

* MAC Addresses Can Be Spoofed

---

# Wireless Threats

## Rogue Access Point

Unauthorized wireless device connected to a network.

Example:

```text
Employee Installs
Unauthorized Router
```

Risks:

* Bypass Security Controls
* Data Exposure

---

## Evil Twin Attack

Attacker creates a fake Wi-Fi network.

Example:

```text
Real:
Office-WiFi

Fake:
Office-WiFi_Free
```

Users may unknowingly connect to the fake network.

---

## Packet Sniffing

Capturing wireless traffic.

Risks:

* Credential Theft
* Information Disclosure

Protection:

* Strong Encryption
* HTTPS
* VPN

---

## Deauthentication Attack

Attackers force devices to disconnect from Wi-Fi.

Effects:

* Service Disruption
* Reconnection Attacks

---

## Man-in-the-Middle (MITM)

Attacker intercepts communications.

Example:

```text
User
 ↓
Attacker
 ↓
Website
```

Protection:

* HTTPS
* VPN
* Secure Wi-Fi

---

# Guest Wireless Networks

Organizations often create separate guest networks.

Example:

```text
Corporate Wi-Fi
Guest Wi-Fi
```

Benefits:

* Isolation
* Reduced Risk
* Better Security

---

# Wireless Network Segmentation

Separate devices into different security zones.

Examples:

```text
Employee Network
Guest Network
IoT Network
```

Benefits:

* Limits Lateral Movement
* Reduces Attack Surface

---

# Wireless Security Best Practices

## Use WPA3

Preferred wireless security standard.

If unavailable:

```text
Use WPA2
```

---

## Strong Passwords

Example:

```text
Network@2026!Secure
```

Avoid:

```text
12345678
password
```

---

## Change Default Credentials

Default router credentials should be changed immediately.

Bad:

```text
admin/admin
```

---

## Disable Unused Features

Examples:

* WPS
* Unused SSIDs

---

## Keep Firmware Updated

Benefits:

* Security Fixes
* Bug Fixes
* Improved Stability

---

## Enable Guest Networks

Separate visitors from internal resources.

---

## Use VPN for Public Wi-Fi

Benefits:

* Encrypted Communication
* Improved Privacy

---

# Wireless Security Devices

## Wireless Access Point (WAP)

Provides Wi-Fi connectivity.

---

## Wireless Controller

Manages multiple access points.

Benefits:

* Centralized Management
* Policy Enforcement

---

## RADIUS Server

Provides centralized authentication.

Example:

```text
User
 ↓
RADIUS
 ↓
Authentication
```

---

# Monitoring Wireless Networks

Monitor:

* Connected Devices
* Failed Logins
* Signal Strength
* Rogue Devices

Tools:

* Wireshark
* Wireless Controllers
* SIEM Platforms

---

# Wireless Troubleshooting

## Cannot Connect

Check:

```text
SSID
Password
Signal Strength
```

---

## Slow Wi-Fi

Possible Causes:

* Interference
* Weak Signal
* Too Many Users

---

## Frequent Disconnects

Check:

* Distance
* Access Point Health
* Channel Congestion

---

# Wireless Security Architecture

Example:

```text
Internet
    ↓
Firewall
    ↓
Wireless Controller
    ↓
Access Points
    ↓
Users
```

Security Layers:

* Firewall
* Authentication
* Encryption
* Monitoring

---

# Interview Questions

### What is Wireless Security?

Protecting wireless networks from unauthorized access and attacks.

### Why is WPA3 recommended?

It provides stronger authentication and encryption than WPA2.

### What is an SSID?

The name of a wireless network.

### What is a Rogue Access Point?

An unauthorized wireless device connected to a network.

### What is an Evil Twin Attack?

A fake wireless network designed to trick users.

### What is the purpose of a Guest Network?

To isolate visitors from internal resources.

### What protocol is commonly used for enterprise wireless authentication?

RADIUS.

---

# Summary

Wireless Security protects Wi-Fi networks, devices, and data from unauthorized access and cyber threats. Key concepts include WPA2, WPA3, Authentication, Encryption, SSIDs, Guest Networks, Network Segmentation, Rogue Access Points, and Wireless Security Best Practices. Strong wireless security helps ensure confidentiality, integrity, and availability while supporting secure mobile connectivity.
