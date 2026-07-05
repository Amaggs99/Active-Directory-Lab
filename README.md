# Active Directory Home Lab

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Windows Server](https://img.shields.io/badge/Windows%20Server-2022-blue)
![Active Directory](https://img.shields.io/badge/Active%20Directory-Lab-green)
![GitHub last commit](https://img.shields.io/github/last-commit/Amaggs99/Active-Directory-Lab)

---

## Overview

This project demonstrates the deployment and administration of a Windows Server Active Directory environment in a virtual lab. The purpose of this project is to develop hands-on experience with common help desk and system administration tasks typically performed in enterprise environments.

---

## Current Project Status

- ✅ Domain Controller deployed
- ✅ Active Directory and DNS configured
- ✅ Domain Controller health validated (DCDIAG)
- ✅ Organizational Units created
- ✅ Security Groups created
- ✅ Test Users created
- ✅ Windows 11 client joined to domain
- ✅ Domain authentication verified
- 🚧 Group Policy configuration pending

---

## Latest Milestone

### Milestone 4 – Domain Join Complete

- Configured Windows 11 client networking
- Joined CLIENT01 to `adlab.local`
- Verified DNS resolution
- Verified domain authentication
- Added screenshots and documentation

---

## Objectives

- Deploy a Windows Server Domain Controller
- Configure Active Directory Domain Services (AD DS)
- Create and manage Organizational Units (OUs)
- Create and manage users and security groups
- Join a Windows client to a domain
- Perform common help desk administration tasks
- Document the environment and troubleshooting process

---

## Lab Environment

### Virtualization Platform

- VMware Workstation Pro
- VirtualBox (optional migration platform)

### Servers and Clients

| Device | Operating System | Purpose |
|--------|------------------|----------|
| DC01 | Windows Server 2022 | Domain Controller |
| CLIENT01 | Windows 11 | Domain Joined Workstation |

---

## Domain Information

**Domain Name:** `adlab.local`

---

## Network Configuration

### DC01

- Static IP Address: `192.168.66.10`
- Subnet Mask: `255.255.255.0`
- Preferred DNS Server: `192.168.66.10`

### CLIENT01

- Static IP Address: `192.168.66.20`
- Subnet Mask: `255.255.255.0`
- Preferred DNS Server: `192.168.66.10`

---

## Architecture Diagram

![Architecture Diagram](Network-Diagram.png)

**Figure 1:** High-level network topology of the Active Directory home lab environment.

### Network Overview

- DC01 – Windows Server 2022 Domain Controller and DNS Server
- CLIENT01 – Windows 11 Domain-Joined Workstation
- VMnet1 Host-Only Network – Internal lab communication
- Domain: `adlab.local`

---

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS
- Windows 11
- PowerShell
- VMware Workstation Pro
- VirtualBox
- Git
- GitHub

---

## Skills Demonstrated

- Active Directory installation and configuration
- Domain Controller deployment
- Organizational Unit (OU) management
- User account administration
- Security group administration
- DNS configuration and troubleshooting
- Windows Server administration
- Domain controller health validation
- PowerShell administration and automation
- Documentation and version control using Git and GitHub

---

## Active Directory Structure

```text
adlab.local
└── Company
    ├── Users
    ├── Groups
    ├── Computers
    ├── Servers
    └── Service Accounts
```

### Security Groups

```text
IT_Admins
HelpDesk
HR
Sales
```

### Test Users

| Name | Username | Group |
|------|-----------|--------|
| John Smith | jsmith | IT_Admins |
| Sarah Brown | sbrown | HelpDesk |
| Emily Davis | edavis | HR |
| Mike Wilson | mwilson | Sales |

---

## Help Desk Tasks Completed

- Installed and configured Active Directory Domain Services
- Promoted server to Domain Controller
- Configured DNS
- Created Organizational Units (OUs)
- Created domain users
- Created security groups
- Added users to security groups
- Joined a Windows client to the domain
- Verified domain authentication
- Verified domain controller health using DCDIAG
- Documented configuration and screenshots
- Used PowerShell to automate administrative tasks

---

## Screenshots

The following screenshots are available in the `Screenshots` folder:

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

## Documentation

Detailed documentation can be found in the `Documentation` folder.

Current documentation includes:

- Commands-Used.md
- Domain-Controller-Setup.md
- Troubleshooting.md

Planned additions:

- Client-Domain-Join.md
- OU-Structure.md
- User-Management.md
- Group-Policy.md

---

## Lessons Learned

- DNS is critical to Active Directory functionality.
- Virtual networking configuration directly impacts domain communication.
- Domain controllers should use static IP addressing.
- Documentation and screenshots simplify troubleshooting.
- PowerShell can automate many administrative tasks.
- Proper planning of OU and group structures improves manageability.

---

## Resume Relevance

This project demonstrates practical experience relevant to:

- IT Support Technician
- Help Desk Analyst
- Service Desk Technician
- Desktop Support Technician
- Junior Systems Administrator
- Junior Network Administrator

---

# Progress

## ✅ Completed

- [x] Installed Windows Server 2022
- [x] Renamed server to DC01
- [x] Configured static IP addressing
- [x] Installed Active Directory Domain Services
- [x] Promoted server to Domain Controller
- [x] Validated DNS, SYSVOL, and DFS Replication health
- [x] Created Organizational Units (OUs)
- [x] Created security groups
- [x] Created test users
- [x] Added users to security groups
- [x] Configured Windows 11 client networking
- [x] Joined CLIENT01 to adlab.local
- [x] Verified domain login
- [x] Verified DNS resolution
- [x] Collected implementation screenshots
- [x] Updated project documentation

---

# 🚧 TODO / Next Steps

## Phase 5 – Group Policy

- [ ] Create desktop wallpaper GPO
- [ ] Configure password policy
- [ ] Configure account lockout policy
- [ ] Deploy a mapped network drive
- [ ] Disable Control Panel for a test OU

---

## Phase 6 – Help Desk Administration

- [ ] Reset user passwords
- [ ] Disable user accounts
- [ ] Unlock user accounts
- [ ] Create additional users
- [ ] Create additional security groups
- [ ] Delegate permissions

---

## Phase 7 – Advanced Administration

- [ ] Create shared folders and NTFS permissions
- [ ] Configure roaming profiles (optional)
- [ ] Create service accounts
- [ ] Implement backup procedures
- [ ] Configure PowerShell automation scripts

---

## Repository Structure

```text
Active-Directory-Lab
│
├── README.md
├── Network-Diagram.png
├── Documentation
│   ├── Commands-Used.md
│   ├── Domain-Controller-Setup.md
│   └── Troubleshooting.md
│
└── Screenshots
    ├── DC01-IPConfig.png
    ├── DC01-DomainInfo.png
    ├── DC01-DCDiag-01.png
    ├── DC01-DCDiag-02.png
    ├── DC01-DCDiag-03.png
    ├── DC01-DCDiag-04.png
    ├── OU-Structure.png
    ├── Security-Groups.png
    ├── AD-Users.png
    ├── CLIENT01-Domain-Joined.png
    ├── Client-Domain-Login.png
    └── Client-System-Properties.png
```

---

## Author

**Austin Maggs**

GitHub: https://github.com/Amaggs99