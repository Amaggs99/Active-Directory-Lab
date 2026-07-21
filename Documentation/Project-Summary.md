# Project Summary

## Project Overview

This project demonstrates the deployment of a fully functional Active Directory environment using Windows Server 2022 and Windows 11 within a virtualized lab environment.

The objective of this project was to gain practical experience with enterprise system administration tasks commonly performed by Help Desk Technicians, Desktop Support Technicians, and Junior Systems Administrators.

---

# Environment Information

| Component | Value |
|-----------|--------|
| Domain Controller | DC01 |
| Client Workstation | CLIENT01 |
| Domain Name | adlab.local |
| Network Type | VMnet1 Host-Only |
| DC01 IP Address | 192.168.66.10 |
| CLIENT01 IP Address | 192.168.66.20 |
| Hypervisor | VMware Workstation Pro |

---

# Network Architecture

The lab environment uses a VMware Host-Only network to provide isolated communication between the Windows Server 2022 Domain Controller and Windows 11 domain client.

![Active Directory Lab Network Diagram](../Network-Diagram.png)

---

# Project Objectives

- Deploy Windows Server 2022
- Install Active Directory Domain Services (AD DS)
- Configure DNS
- Create Organizational Units (OUs)
- Create Security Groups
- Create and manage domain users
- Deploy a Windows 11 client
- Join the client to the domain
- Verify domain authentication
- Document the deployment and troubleshooting process

---

# Completed Work

## Infrastructure Deployment

- Installed Windows Server 2022
- Renamed server to DC01
- Configured static networking
- Installed VMware Tools
- Configured Host-Only networking

---

## Active Directory Deployment

- Installed Active Directory Domain Services
- Promoted server to Domain Controller
- Configured DNS Server
- Verified Domain Controller health using DCDIAG
- Verified DNS functionality

---

## Active Directory Administration

Created Organizational Units:

```text
Company
├── Users
├── Groups
├── Computers
├── Servers
└── Service Accounts
```

Created Security Groups:

```text
IT_Admins
HelpDesk
HR
Sales
```

Created Test Users:

- John Smith (jsmith)
- Sarah Brown (sbrown)
- Emily Davis (edavis)
- Mike Wilson (mwilson)

Added users to appropriate security groups.

---

## Client Deployment

- Installed Windows 11
- Configured static networking
- Renamed workstation to CLIENT01
- Joined CLIENT01 to adlab.local
- Verified DNS resolution
- Verified domain authentication
- Verified communication with Domain Controller

---

# Validation Performed

The following validation tests were successfully completed:

```cmd
ipconfig /all

nslookup adlab.local

ping 192.168.66.10

dcdiag /v
```

Additional validation:

- Active Directory Users and Computers accessible
- DNS service operational
- SYSVOL replication healthy
- Domain login successful
- CLIENT01 visible within Active Directory

---

# Skills Demonstrated

## Windows Server Administration

- Server installation and configuration
- Domain Controller deployment
- DNS configuration

---

## Active Directory Administration

- Organizational Unit management
- User administration
- Security group administration
- Domain joining

---

## Networking

- Static IP configuration
- DNS troubleshooting
- Virtual networking
- Network connectivity validation

---

## Troubleshooting

- VMware networking issues
- DNS resolution problems
- Domain join troubleshooting
- Service validation

---

## Documentation and Version Control

- Technical documentation
- Screenshot collection
- Git and GitHub version control
- Project organization and repository management

---

# Lessons Learned

- DNS is critical to Active Directory functionality.
- Domain Controllers should always use static IP addressing.
- Proper virtual network configuration is essential for domain communication.
- PowerShell significantly simplifies system administration tasks.
- Thorough documentation makes troubleshooting and future administration easier.

---

# Final Status

✅ Active Directory deployment completed successfully.

This repository serves as the baseline Active Directory environment for future projects involving:

- IT Help Desk Administration
- Group Policy Management
- PowerShell Automation
- File Server Administration
- Advanced Windows Server Administration

---

# Repository Purpose

This repository demonstrates the ability to:

- Build an Active Directory environment from scratch.
- Configure and validate enterprise services.
- Document technical implementations.
- Troubleshoot and resolve infrastructure issues.
- Maintain a professional project repository suitable for portfolio and resume use.

---

# Supporting Documentation

Detailed implementation, administration, troubleshooting, and validation documentation is available throughout the repository:

- [Active Directory Lab Setup Guide](Lab-Setup-Guide.md)
- [Installation Notes](Installation-Notes.md)
- [Help Desk Administration Tasks](Helpdesk-Tasks.md)
- [Troubleshooting Notes](Troubleshooting-Notes.md)
- [Domain Controller Validation](Domain-Controller-Validation.md)