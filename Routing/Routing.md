# Network Security

## Introduction

Network Security is the practice of protecting networks, devices, applications, and data from unauthorized access, misuse, modification, or destruction.

The primary goal of network security is to ensure:

* Confidentiality
* Integrity
* Availability

These three principles are known as the **CIA Triad**.

Modern organizations rely on network security to protect sensitive information, maintain business operations, and defend against cyber threats.

---

# CIA Triad

## Confidentiality

Ensures information is accessible only to authorized users.

Examples:

* Encryption
* Access Controls
* Password Protection

Example:

```text
User Login
    ↓
Authentication
    ↓
Access Granted
```

---

## Integrity

Ensures data remains accurate and unchanged.

Methods:

* Hashing
* Digital Signatures
* Checksums

Example:

```text
Original File
      ↓
SHA-256 Hash
      ↓
Verification
```

---

## Availability

Ensures systems and data remain accessible.

Methods:

* Redundant Systems
* Backup Links
* Load Balancing

Example:

```text
Server A
   ↓
Load Balancer
   ↓
Users
```

---

# Common Network Threats

## Malware

Malicious software designed to damage systems.

Types:

* Virus
* Worm
* Trojan
* Spyware
* Ransomware

---

## Phishing

Attempts to trick users into revealing sensitive information.

Example:

```text
Fake Email
     ↓
Login Page
     ↓
Credential Theft
```

---

## Denial of Service (DoS)

Attempts to overwhelm a system with traffic.

Goal:

```text
Legitimate Users
      ↓
Cannot Access Service
```

---

## Distributed Denial of Service (DDoS)

Multiple systems attack a target simultaneously.

Example:

```text
Botnet
  ↓↓↓↓↓
Target Server
```

---

## Man-in-the-Middle (MITM)

An attacker intercepts communication between two parties.

Example:

```text
User
  ↓
Attacker
  ↓
Website
```

Risk:

* Data Theft
* Session Hijacking

---

## Password Attacks

Examples:

* Password Guessing
* Credential Stuffing
* Brute Force Attacks

Protection:

* Strong Passwords
* MFA
* Account Lockout Policies

---

# Authentication

Authentication verifies identity.

Factors:

### Something You Know

Examples:

* Password
* PIN

### Something You Have

Examples:

* Security Token
* Mobile Device

### Something You Are

Examples:

* Fingerprint
* Face Recognition

---

# Multi-Factor Authentication (MFA)

Uses two or more authentication factors.

Example:

```text
Password
    +
Mobile OTP
```

Benefits:

* Stronger Security
* Reduced Account Takeovers

---

# Firewalls

A firewall monitors and filters network traffic.

Functions:

* Allow Authorized Traffic
* Block Unauthorized Traffic

Example:

```text
Internet
    ↓
Firewall
    ↓
Internal Network
```

---

## Types of Firewalls

### Packet Filtering Firewall

Filters traffic using:

* Source IP
* Destination IP
* Ports
* Protocols

---

### Stateful Firewall

Tracks active connections.

Advantages:

* Better Security
* Connection Awareness

---

### Next-Generation Firewall (NGFW)

Features:

* Application Awareness
* Intrusion Prevention
* Malware Detection
* Deep Packet Inspection

---

# Access Control Lists (ACLs)

ACLs control traffic flow.

Example:

```text
Allow:
TCP 443

Deny:
All Others
```

Benefits:

* Traffic Control
* Network Segmentation

---

# Intrusion Detection System (IDS)

Monitors network traffic for suspicious activity.

Types:

### Network IDS

Monitors entire network traffic.

### Host IDS

Monitors individual systems.

---

# Intrusion Prevention System (IPS)

Similar to IDS but can automatically block threats.

Example:

```text
Attack Detected
      ↓
Traffic Blocked
```

---

# Virtual Private Network (VPN)

A VPN creates an encrypted connection between devices.

Example:

```text
Remote User
      ↓
Encrypted Tunnel
      ↓
Corporate Network
```

Benefits:

* Privacy
* Secure Remote Access

---

# Encryption

Encryption converts readable data into unreadable ciphertext.

Example:

```text
HELLO
  ↓
Encrypted
  ↓
XK72P9
```

Only authorized users can decrypt the data.

---

## Symmetric Encryption

Uses the same key for encryption and decryption.

Examples:

* AES
* DES

---

## Asymmetric Encryption

Uses two keys:

```text
Public Key
Private Key
```

Examples:

* RSA
* ECC

---

# Secure Network Protocols

| Insecure | Secure |
| -------- | ------ |
| HTTP     | HTTPS  |
| FTP      | SFTP   |
| Telnet   | SSH    |

Common Secure Ports:

```text
HTTPS : 443
SSH   : 22
SFTP  : 22
```

---

# Network Segmentation

Network segmentation divides networks into smaller sections.

Methods:

* VLANs
* Subnets
* Security Zones

Example:

```text
HR VLAN
IT VLAN
Finance VLAN
Guest VLAN
```

Benefits:

* Improved Security
* Reduced Attack Surface

---

# Security Monitoring

Organizations continuously monitor networks.

Tools:

* SIEM Platforms
* IDS/IPS
* Log Analysis
* Threat Intelligence

Monitoring helps detect:

* Unauthorized Access
* Malware
* Suspicious Activity

---

# Security Best Practices

## Strong Passwords

Example:

```text
Length > 12 Characters
Mix of Letters, Numbers, Symbols
```

---

## Enable MFA

Protect critical accounts.

---

## Keep Systems Updated

Install:

* Security Patches
* Firmware Updates
* Application Updates

---

## Least Privilege Principle

Users receive only required permissions.

---

## Regular Backups

Protect against:

* Hardware Failures
* Ransomware
* Accidental Deletion

---

## Security Awareness Training

Teach users to identify:

* Phishing
* Social Engineering
* Suspicious Links

---

# Incident Response Process

## Preparation

Develop policies and procedures.

---

## Detection

Identify security incidents.

---

## Containment

Limit the impact.

---

## Eradication

Remove the threat.

---

## Recovery

Restore normal operations.

---

## Lessons Learned

Improve defenses.

---

# Network Security Architecture

Example:

```text
Internet
    ↓
Firewall
    ↓
IDS/IPS
    ↓
DMZ
    ↓
Internal Network
```

Layers:

* Perimeter Security
* Internal Security
* Endpoint Protection
* Monitoring

---

# Interview Questions

### What is Network Security?

Protecting networks, systems, and data from unauthorized access and attacks.

### What is the CIA Triad?

* Confidentiality
* Integrity
* Availability

### What is a Firewall?

A device or software that filters network traffic.

### Difference Between IDS and IPS?

IDS detects threats.

IPS detects and blocks threats.

### What is MFA?

Multi-Factor Authentication requiring multiple verification methods.

### What is a VPN?

An encrypted tunnel for secure communication.

### What is Network Segmentation?

Dividing a network into smaller secure sections.

---

# Summary

Network Security protects systems, networks, and data from cyber threats. Core concepts include the CIA Triad, Firewalls, VPNs, IDS/IPS, Authentication, Encryption, Network Segmentation, and Security Monitoring. Strong security practices help organizations maintain confidentiality, integrity, and availability while defending against modern cyber threats.
