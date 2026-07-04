\# Domain Controller Validation



\## Objective

Validate the health of the Active Directory Domain Controller after renaming the server to DC01.



\## Validation Steps Performed

\- Verified hostname and computer name.

\- Verified Service Principal Names (SPNs).

\- Verified DNS health using `dcdiag /test:dns`.

\- Verified SYSVOL and NETLOGON shares.

\- Verified DFS Replication service status.

\- Verified Active Directory replication health.



\## Commands Used



```powershell

hostname

setspn -L DC01

ipconfig /all

dcdiag /test:dns

repadmin /replsummary

net share

Get-Service DFSR

```



\## Results

\- Domain Controller renamed successfully to DC01.

\- DNS tests passed.

\- SYSVOL and NETLOGON shares available.

\- DFS Replication service running.

\- Replication health clean.

\- Historical DFSR warnings observed after rename but no active issues detected.



\## Lessons Learned

Even after renaming a Domain Controller, Active Directory can remain healthy provided DNS registration, SYSVOL, and replication services are functioning correctly.

