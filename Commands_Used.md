# Commands Used

This document contains Git, Windows, networking, PowerShell, and Active Directory commands used throughout the Active Directory Home Lab.

---

# Git Commands

## Check Repository Status

```bash
git status
```

Displays modified files, untracked files, staged files, and current branch status.

---

## Stage All Changes

```bash
git add .
```

Adds all new and modified files to the staging area.

---

## Create a Commit

```bash
git commit -m "Commit message"
```

Creates a snapshot of the staged changes.

---

## Push Changes to GitHub

```bash
git push origin main
```

Uploads local commits to GitHub.

---

## Pull Changes from GitHub

```bash
git pull origin main
```

Downloads and merges changes from GitHub into the local repository.

---

## View Commit History

```bash
git log --oneline
```

Displays a concise list of previous commits.

---

## Check Remote Repository

```bash
git remote -v
```

Shows the GitHub repository associated with the local project.

---

## Clone Repository

```bash
git clone https://github.com/Amaggs99/Active-Directory-Lab.git
```

Downloads a copy of the repository from GitHub.

---

# Git Bash Commands

## Create a New File

```bash
touch filename.md
```

Example:

```bash
touch README.md
touch Documentation/Project-Summary.md
```

---

## Create a New Directory

```bash
mkdir FolderName
```

Example:

```bash
mkdir Documentation
mkdir Screenshots
```

---

## List Directory Contents

```bash
ls
```

Displays files and folders in the current directory.

---

## Rename or Move a File

```bash
mv oldname newname
```

Example:

```bash
mv Commands-Used.md.txt Commands-Used.md
```

---

## Change Directory

```bash
cd directory-name
```

Example:

```bash
cd Documentation
cd ..
cd Screenshots
```

---

## Display Current Directory

```bash
pwd
```

Displays the full path of the current working directory.

---

# Windows Networking Commands

## Display IP Configuration

```cmd
ipconfig /all
```

Displays detailed network adapter information.

---

## Flush DNS Cache

```cmd
ipconfig /flushdns
```

Clears the DNS resolver cache.

---

## Test Connectivity

```cmd
ping 192.168.66.10
```

Tests communication with the Domain Controller.

---

## Test Domain DNS Resolution

```cmd
nslookup adlab.local
```

Verifies DNS resolution for the Active Directory domain.

---

## View Routing Table

```cmd
route print
```

Displays the local routing table.

---

# Active Directory PowerShell Commands

## Import Active Directory Module

```powershell
Import-Module ActiveDirectory
```

Loads the Active Directory PowerShell module.

---

## View Domain Information

```powershell
Get-ADDomain
```

Displays Active Directory domain information.

---

## View Forest Information

```powershell
Get-ADForest
```

Displays Active Directory forest information.

---

## Create an Organizational Unit

```powershell
New-ADOrganizationalUnit -Name "Users" -Path "OU=Company,DC=adlab,DC=local"
```

Creates a new Organizational Unit.

---

## Create a Security Group

```powershell
New-ADGroup -Name "IT_Admins" -GroupScope Global -GroupCategory Security -Path "OU=Groups,OU=Company,DC=adlab,DC=local"
```

Creates a new Active Directory security group.

---

## Create a User

```powershell
New-ADUser -Name "John Smith" -SamAccountName jsmith -AccountPassword (ConvertTo-SecureString "Password123!" -AsPlainText -Force) -Enabled $true
```

Creates and enables a new Active Directory user.

---

## Add User to Group

```powershell
Add-ADGroupMember -Identity "IT_Admins" -Members jsmith
```

Adds a user to an Active Directory group.

---

## Verify Users

```powershell
Get-ADUser -Filter * -SearchBase "OU=Users,OU=Company,DC=adlab,DC=local" | Select Name,SamAccountName,Enabled
```

Displays users created inside the lab Users OU.

---

## Verify Groups

```powershell
Get-ADGroup -Filter * -SearchBase "OU=Groups,OU=Company,DC=adlab,DC=local" | Select Name
```

Displays groups created inside the lab Groups OU.

---

# Domain Controller Validation Commands

## Run Domain Controller Diagnostics

```cmd
dcdiag /v
```

Runs detailed diagnostic tests against the Domain Controller.

---

## Run DNS-Specific Diagnostic Test

```cmd
dcdiag /test:DNS
```

Checks DNS health for the Domain Controller.

---

## Check Important AD Services

```powershell
Get-Service NTDS,DNS,Netlogon,KDC
```

Verifies that core Active Directory services are running.

---

## Check VMware Tools Service

```powershell
Get-Service VMTools
```

Checks whether VMware Tools is installed and running.

---

# Client Domain Join Commands

## Rename Windows Client

```powershell
Rename-Computer -NewName "CLIENT01" -Restart
```

Renames the Windows client and restarts the machine.

---

## Join Client to Domain

```powershell
Add-Computer -DomainName adlab.local -Credential adlab\Administrator -Restart
```

Joins the Windows client to the Active Directory domain.

---

## Verify Logged-In User

```cmd
whoami
```

Shows the currently logged-in user.

Example:

```text
adlab\administrator
```

---

## Verify Computer Name

```cmd
hostname
```

Displays the local computer name.

---

# Windows Administration Consoles

## Active Directory Users and Computers

```cmd
dsa.msc
```

Opens Active Directory Users and Computers.

---

## Group Policy Management

```cmd
gpmc.msc
```

Opens Group Policy Management Console.

---

## DNS Manager

```cmd
dnsmgmt.msc
```

Opens DNS Manager.

---

## Server Manager

```cmd
servermanager
```

Opens Server Manager.

---

## System Properties

```cmd
sysdm.cpl
```

Opens System Properties.

---

## Network Connections

```cmd
ncpa.cpl
```

Opens Network Connections.

---

# Firewall Commands

## Disable Windows Firewall Temporarily

```powershell
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
```

Used temporarily during troubleshooting to test connectivity.

---

## Enable Windows Firewall

```powershell
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True
```

Re-enables Windows Firewall.

---

## Enable File and Printer Sharing Ping Rules

```powershell
Enable-NetFirewallRule -DisplayGroup "File and Printer Sharing"
```

Allows ICMP/ping responses through Windows Firewall.

---

# VMware Tasks

## Take Snapshot

```text
VM → Snapshot → Take Snapshot
```

Creates a restore point of the lab environment.

---

## Restore Snapshot

```text
VM → Snapshot → Snapshot Manager
```

Restores the VM to a previous lab state.

---

## Install VMware Tools

```text
VM → Install VMware Tools
```

Mounts VMware Tools inside the guest operating system.

---

## Open Virtual Network Editor

```text
Edit → Virtual Network Editor
```

Used to verify VMnet1 Host-Only and VMnet8 NAT configuration.

---

# Lab Notes

These commands were used throughout the Active Directory Home Lab to deploy, troubleshoot, and administer the environment. They serve as a quick reference for future projects, documentation, and interview preparation.