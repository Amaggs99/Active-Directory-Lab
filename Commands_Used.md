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

# Git Bash Commands

## Create a New File

```bash
touch filename.md
```

Creates a new empty file in the current directory.

Example:

```bash
touch README.md
touch Documentation/Lab-Setup-Guide.md
```

---

## Create a New Directory

```bash
mkdir FolderName
```

Creates a new folder in the current directory.

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

Displays all files and folders in the current directory.

Example:

```bash
ls
ls Documentation
```

---

## Rename or Move a File

```bash
mv oldname newname
```

Renames a file or moves it to a new location.

Example:

```bash
mv Commands-Used.md.txt Commands-Used.md
mv Documentation/Helpdesk-Task.md Documentation/Helpdesk-Tasks.md
```

---

## Change Directory

```bash
cd directory-name
```

Changes the current working directory.

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

Example:

```bash
pwd
```

Output:

```text
C:/Users/Austin/Documents/Master-Career/Repositories/Home-Labs/Active-Directory-Lab
```

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
