# Commands Used

# Git Commands

## Check Repository Status

```bash
git status
```

Displays:
- Modified files
- Untracked files
- Staged files
- Current branch status

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

## Configure Git Username

```bash
git config --global user.name "Austin Maggs"
```

Sets the global Git username.

---

## Configure Git Email

```bash
git config --global user.email "austinmaggs@gmail.com"
```

Sets the global Git email address.

---

## Clone Repository

```bash
git clone https://github.com/Amaggs99/Active-Directory-Lab.git
```

Downloads a copy of the repository from GitHub.

---

# Active Directory Commands

## Display IP Configuration

```cmd
ipconfig /all
```

Displays detailed network adapter information.

---

## Test Name Resolution

```cmd
nslookup corp.local
```

Tests DNS functionality.

---

## Test Connectivity

```cmd
ping dc01
```

Verifies network communication.

---

## Flush DNS Cache

```cmd
ipconfig /flushdns
```

Clears the DNS resolver cache.

---

## Force Group Policy Update

```cmd
gpupdate /force
```

Immediately refreshes Group Policy settings.

---

## Open Active Directory Users and Computers

```cmd
dsa.msc
```

Launches the Active Directory administration console.

---

## Open Group Policy Management

```cmd
gpmc.msc
```

Launches the Group Policy Management Console.
