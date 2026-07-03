# Active Directory Lab Setup Guide

## Overview
This lab demonstrates the deployment and administration of a Windows Server Active Directory environment.

## Objectives
- Install Windows Server 2022
- Configure a Domain Controller
- Install Active Directory Domain Services (AD DS)
- Create Organizational Units (OUs)
- Create Domain Users and Security Groups
- Join a Windows 11 client to the domain
- Perform common Help Desk administration tasks

---

# Lab Environment

## Virtual Machines

### Domain Controller
| Setting | Value |
|---------|--------|
| Name | DC01 |
| Operating System | Windows Server 2022 |
| RAM | 4 GB |
| CPU | 2 Cores |
| Disk | 60 GB |

### Client Computer
| Setting | Value |
|---------|--------|
| Name | CLIENT01 |
| Operating System | Windows 11 |
| RAM | 4 GB |
| CPU | 2 Cores |
| Disk | 60 GB |

---

# Network Configuration

| Device | IP Address |
|---------|------------|
| DC01 | 192.168.10.10 |
| CLIENT01 | DHCP |

## Domain Information

Domain Name:
corp.local

NetBIOS Name:
CORP

DNS Server:
192.168.10.10
