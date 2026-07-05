# Documentation

This folder contains detailed notes, commands, screenshots, and troubleshooting information related to the Active Directory Home Lab project.

---

# Purpose

The purpose of this documentation is to:

- Document the build and deployment process.
- Record server and network configuration steps.
- Track troubleshooting and resolutions.
- Provide evidence of hands-on system administration experience.
- Serve as a knowledge base for future reference.
- Support portfolio and resume projects.

---

# Documentation Structure

| File | Description |
|------|-------------|
| Project-Summary.md | High-level summary of the entire Active Directory deployment |
| Installation-Notes.md | Server installation and deployment notes |
| Lab-Setup-Guide.md | Complete build guide for the environment |
| Commands-Used.md | Git, networking, PowerShell, and Active Directory commands |
| Helpdesk.md | Common Active Directory administration tasks |
| Troubleshooting.md | Issues encountered and resolutions |

---

# Environment Overview

| Component | Value |
|-----------|--------|
| Domain Controller | DC01 |
| Client Workstation | CLIENT01 |
| Domain Name | adlab.local |
| Network | VMnet1 Host-Only |
| DC01 IP Address | 192.168.66.10 |
| CLIENT01 IP Address | 192.168.66.20 |
| Hypervisor | VMware Workstation Pro |

---

# Completed Documentation

## Domain Controller Deployment

- Installed Windows Server 2022
- Renamed server to DC01
- Configured static IP addressing
- Installed VMware Tools
- Installed AD DS and DNS roles
- Promoted server to Domain Controller
- Verified Domain Controller health

---

## Active Directory Structure

Created the following Organizational Units:

```text
Company
├── Users
├── Groups
├── Computers
├── Servers
└── Service Accounts
```

---

## Security Groups

```text
IT_Admins
HelpDesk
HR
Sales
```

---

## Test Users

| Name | Username | Department |
|------|-----------|------------|
| John Smith | jsmith | IT |
| Sarah Brown | sbrown | Help Desk |
| Emily Davis | edavis | HR |
| Mike Wilson | mwilson | Sales |

---

## Client Deployment

- Installed Windows 11
- Configured static networking
- Renamed workstation to CLIENT01
- Joined CLIENT01 to adlab.local
- Verified domain authentication
- Verified DNS functionality
- Verified communication with Domain Controller

---

# Validation Completed

The following tests were successfully performed:

```cmd
ipconfig /all
ping 192.168.66.10
nslookup adlab.local
dcdiag /v
```

Additional validation:

- DNS service operational
- Active Directory services operational
- CLIENT01 visible in Active Directory
- Successful domain login
- Domain authentication verified

---

# Screenshots

Supporting screenshots can be found in:

```text
../Screenshots/
```

Current screenshots include:

- DC01-IPConfig.png
- DC01-DomainInfo.png
- DC01-DCDiag-01.png
- DC01-DCDiag-02.png
- DC01-DCDiag-03.png
- DC01-DCDiag-04.png
- OU-Structure.png
- Security-Groups.png
- AD-Users.png
- CLIENT01-Domain-Joined.png
- Client-Domain-Login.png
- Client-System-Properties.png

---

# Lessons Learned

- Active Directory relies heavily on proper DNS configuration.
- Domain Controllers should always use static IP addresses.
- Virtual networking can significantly impact domain communication.
- PowerShell simplifies system administration and troubleshooting.
- Documentation and screenshots make future administration easier.
- Version control with Git is an excellent method for tracking project progress.

---

# Project Completion Status

✅ Active Directory deployment completed successfully.

This repository documents the deployment of a complete Active Directory environment from initial installation through domain client integration.

Future administrative tasks will be documented in separate repositories:

- IT-Helpdesk-Lab
- Group-Policy-Lab
- PowerShell-AD-Automation

---

# Repository Purpose

This documentation demonstrates:

- Windows Server Administration
- Active Directory Administration
- DNS Configuration
- Virtual Networking
- User and Group Management
- Domain Joining
- Troubleshooting
- Documentation and Version Control