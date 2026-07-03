# Troubleshooting Notes

---

## Issue
Client computer could not join the domain.

### Cause
Incorrect DNS server configuration.

### Resolution
Changed DNS server to:

192.168.10.10

### Result
Client successfully joined the domain.

---

## Issue
Unable to log in with domain credentials.

### Cause
Client was not communicating with the Domain Controller.

### Resolution
Verified:

- Network connectivity
- DNS settings
- Domain membership

### Result
Domain login successful.

---

## Issue
DNS name resolution failed.

### Resolution
Executed:

nslookup corp.local
ipconfig /flushdns

### Result
DNS functionality restored.
