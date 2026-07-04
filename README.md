# Active Directory Home Lab

## Overview

This project demonstrates the deployment and administration of a Windows Server Active Directory environment in a virtual lab. The purpose of this project is to develop hands-on experience with common help desk and system administration tasks typically performed in enterprise environments.

---

## Objectives

- Deploy a Windows Server Domain Controller
- Configure Active Directory Domain Services
- Create and manage users and groups
- Join a Windows client to a domain
- Perform common help desk administration tasks
- Document the environment and troubleshooting process

---

## Lab Environment

### Virtualization Platform
- VMware Workstation / VirtualBox

### Servers and Clients
| Device | Operating System | Purpose |
|---------|-----------------|----------|
| DC01 | Windows Server 2022 | Domain Controller |
| CLIENT01 | Windows 10/11 | Domain Joined Workstation |

### Domain Information

Domain Name:
austinlab.local

### Network Configuration

DC01:
IP Address: 192.168.10.10
Subnet Mask: 255.255.255.0

CLIENT01:
DNS Server: 192.168.10.10

---

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services
- DNS
- Windows 10/11
- VMware
- VirtualBox

---

## Skills Demonstrated

- Active Directory installation
- Domain controller configuration
- User account creation
- Password resets
- Account unlocks
- Group administration
- Organizational Unit management
- Windows administration
- DNS configuration
- Domain joining
- Troubleshooting

---

## Help Desk Tasks Completed

- Created domain users
- Reset user passwords
- Disabled user accounts
- Added users to security groups
- Joined computers to the domain
- Logged in using domain credentials
- Unlocked user accounts

---

## Screenshots

See the Screenshots folder for implementation evidence.

---

## Documentation

Detailed documentation can be found in the Documentation folder.

---

## Resume Relevance

This project demonstrates practical experience relevant to:

- IT Support Technician
- Help Desk Analyst
- Service Desk Technician
- Junior Systems Administrator
- Desktop Support Technician

## Progress

### Completed
- [x] Installed Windows Server 2022
- [x] Configured static IP addressing
- [x] Installed Active Directory Domain Services
- [x] Promoted server to Domain Controller
- [x] Renamed Domain Controller to DC01
- [x] Validated DNS, SYSVOL, and DFS Replication health

## 🚧 TODO / Next Steps

### Phase 2 – Active Directory Structure
- [ ] Create Organizational Units (OUs)
- [ ] Admin
- [ ] Groups
- [ ] Servers
- [ ] Service Accounts
- [ ] Users
- [ ] HR
- [ ] IT
- [ ] Sales
- [ ] Workstations
- [ ] Desktops
- [ ] Laptops

### Phase 3 – User and Group Management
- [ ] Create test users:
- [ ] John Doe
- [ ] Jane Smith
- [ ] Helpdesk Admin
- [ ] Create security groups:
- [ ] IT_Admins
- [ ] HR_Users
- [ ] Sales_Users
- [ ] Assign users to groups.

### Phase 4 – Client Deployment
- [ ] Create Windows 10/11 client VM.
- [ ] Configure static networking.
- [ ] Join client to `adlab.local`.
- [ ] Verify domain login.
- [ ] Install RSAT tools.

### Phase 5 – Group Policy
- [ ] Create desktop wallpaper GPO.
- [ ] Configure password policy.
- [ ] Configure account lockout policy.
- [ ] Deploy a mapped network drive.
- [ ] Disable Control Panel for a test OU.

### Phase 6 – Documentation
- [ ] Document OU structure.
- [ ] Document users and groups.
- [ ] Document client domain join process.
- [ ] Document Group Policy configuration.
- [ ] Update README with screenshots.
- [ ] Finalize GitHub portfolio documentation.

