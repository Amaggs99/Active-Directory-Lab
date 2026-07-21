# Troubleshooting Notes

This document outlines issues encountered during the deployment of the Active Directory Home Lab and the steps taken to resolve them.

---

# Issue 1 – CLIENT01 Could Not Communicate with DC01

## Symptoms

- `ping` requests timed out.
- Domain join failed.
- DNS queries failed.

---

## Cause

DC01 and CLIENT01 were configured on different virtual networks and different IP subnets.

Example:

```text
DC01      192.168.66.x
CLIENT01  192.168.56.x
```

The machines were unable to communicate.

---

## Resolution

Configured both virtual machines to use:

```text
VMnet1 - Host-Only Network
```

Configured static IP addresses:

| Device | IP Address |
|---------|------------|
| DC01 | 192.168.66.10 |
| CLIENT01 | 192.168.66.20 |

### Verify DC01 Network Configuration

After correcting the virtual network configuration, DC01 was verified with the static IP address `192.168.66.10` and the appropriate DNS configuration.

![DC01 IP Configuration](../Screenshots/DC01-IPConfig.png)

---

## Verification

```cmd
ping 192.168.66.10
ping 192.168.66.20
```

---

## Result

✅ Network communication restored.

---

# Issue 2 – Client Could Not Join the Domain

## Symptoms

- Domain join wizard failed.
- Domain could not be located.
- DNS resolution failed.

---

## Cause

CLIENT01 was configured with an incorrect DNS server.

---

## Resolution

Configured CLIENT01 to use:

```text
Preferred DNS Server:
192.168.66.10
```

Verified:

```cmd
nslookup adlab.local
```

### Verify Successful Domain Join

After correcting the DNS configuration, CLIENT01 was successfully joined to the `adlab.local` Active Directory domain.

![CLIENT01 Domain Joined](../Screenshots/CLIENT01-Domain-Joined.png)

---

## Result

✅ Client successfully joined the domain.

---

# Issue 3 – Unable to Log In with Domain Credentials

## Symptoms

- Domain credentials were rejected.
- Domain logon option was unavailable.

---

## Cause

CLIENT01 was not properly communicating with the Domain Controller.

---

## Resolution

Verified:

```cmd
ping 192.168.66.10
nslookup adlab.local
```

Verified:

- Network configuration
- DNS configuration
- Domain membership
- Domain Controller health

### Verify Domain Authentication

After network connectivity, DNS configuration, domain membership, and Domain Controller health were verified, domain authentication was successfully tested from CLIENT01.

![Client Domain Login](../Screenshots/Client-Domain-Login.png)

---

## Result

✅ Domain authentication successful.

---

# Issue 4 – DNS Name Resolution Failed

## Symptoms

```cmd
nslookup adlab.local
```

returned errors.

---

## Cause

Incorrect DNS configuration and stale DNS cache.

---

## Resolution

Executed:

```cmd
ipconfig /flushdns
nslookup adlab.local
```

Verified DNS server:

```text
192.168.66.10
```

---

## Result

✅ DNS functionality restored.

---

# Issue 5 – VMware Network Adapter "Connected" Option Greyed Out

## Symptoms

- Unable to manually connect the virtual network adapter.
- "Connected" checkbox was greyed out.

---

## Troubleshooting Performed

- Verified VMware network services.
- Recreated NAT adapter.
- Reinstalled VMware networking components.
- Verified Virtual Network Editor configuration.
- Disabled Windows Memory Integrity.

---

## Resolution

Continued lab deployment using Host-Only networking after verifying adapter functionality.

---

## Result

✅ Lab functionality unaffected.

---

# Issue 6 – Active Directory Users and Computers (ADUC) Opened Very Slowly

## Symptoms

- ADUC required an extended period to open.
- Management consoles appeared unresponsive.

---

## Possible Causes

- Limited virtual machine resources.
- VMware Tools not installed.
- Windows Server background initialization.

---

## Resolution

- Installed VMware Tools.
- Increased VM resources where possible.
- Allowed server initialization to complete before opening management consoles.

---

## Result

✅ Functionality restored. Performance remained acceptable for lab purposes.

---

# Validation Commands Used

## Network Configuration

```cmd
ipconfig /all
```

---

## Connectivity

```cmd
ping 192.168.66.10
ping 192.168.66.20
```

---

## DNS Validation

```cmd
nslookup adlab.local
ipconfig /flushdns
```

---

## Domain Controller Health

```cmd
dcdiag /v
```

---

## Service Validation

```powershell
Get-Service NTDS,DNS,Netlogon,KDC
```

---

# Lessons Learned

- DNS is critical to Active Directory functionality.
- Virtual networking issues can prevent domain communication.
- Static IP addressing should be configured before promoting a Domain Controller.
- Documentation and screenshots simplify troubleshooting.
- PowerShell is a powerful troubleshooting and administration tool.
- Troubleshooting skills are just as important as deployment skills.

---

# Final Status

All issues encountered during the deployment of the Active Directory Home Lab were successfully resolved, resulting in a fully functional Active Directory environment consisting of:

- DC01 – Windows Server 2022 Domain Controller
- CLIENT01 – Windows 11 Domain-Joined Workstation
- DNS Services
- Organizational Units
- Security Groups
- Test Users
- Verified Domain Authentication