# Active Directory Home Lab

## Overview

This project demonstrates the deployment and administration of a Windows Server Active Directory environment in a virtual lab. The purpose of this project is to develop hands-on experience with common help desk and system administration tasks typically performed in enterprise environments.

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
|---------|-----------------|----------|
| DC01 | Windows Server 2022 | Domain Controller |
| CLIENT01 | Windows 10/11 | Domain Joined Workstation |

---

## Domain Information

**Domain Name:**  
`austinlab.local`

---

## Network Configuration

### DC01
- Static IP Address: `192.168.56.10`
- Subnet Mask: `255.255.255.0`
- DNS Server: `192.168.56.10`

### CLIENT01
- DNS Server: `192.168.56.10`

---

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS
- Windows 10/11
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
- PowerShell automation
- DNS configuration and troubleshooting
- Windows Server administration
- Domain controller health validation
- Documentation and version control using Git

---

## Active Directory Structure

```text
austinlab.local
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
- Verified domain health using DCDIAG
- Documented configuration and screenshots
- Used PowerShell to automate Active Directory administration tasks

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

---

## Documentation

Detailed documentation can be found in the `Documentation` folder.

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
- [x] Collected implementation screenshots
- [x] Updated project documentation

---

# 🚧 TODO / Next Steps

## Phase 4 – Client Deployment

- [ ] Create Windows 11 client VM
- [ ] Configure networking
- [ ] Join client to `austinlab.local`
- [ ] Verify domain login
- [ ] Install RSAT tools

---

## Phase 5 – Group Policy

- [ ] Create desktop wallpaper GPO
- [ ] Configure password policy
- [ ] Configure account lockout policy
- [ ] Deploy a mapped network drive
- [ ] Disable Control Panel for a test OU

---

## Phase 6 – Advanced Administration

- [ ] Create shared folders and NTFS permissions
- [ ] Configure roaming profiles (optional)
- [ ] Create service accounts
- [ ] Delegate administrative permissions
- [ ] Implement backup procedures

---

## Phase 7 – Documentation & Portfolio

- [ ] Document client domain join process
- [ ] Document Group Policy configuration
- [ ] Add final screenshots
- [ ] Finalize GitHub portfolio documentation
- [ ] Create architecture/network diagram

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
    └── AD-Users.png
```

---

## Author

**Austin Maggs**

GitHub: https://github.com/Amaggs99