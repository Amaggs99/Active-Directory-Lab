\# Documentation



This folder contains detailed notes, commands, screenshots, and troubleshooting information related to the Active Directory Home Lab project.



\---



\# Purpose



The goal of this documentation is to:



\- Document the build process

\- Record configuration steps

\- Track troubleshooting and resolutions

\- Provide evidence of hands-on system administration experience

\- Serve as a knowledge base for future reference



\---



\# Documentation Structure



| File | Description |

|------|-------------|

| Domain-Controller-Setup.md | Installation and promotion of the Domain Controller |

| Commands-Used.md | PowerShell, networking, and Git commands used throughout the project |

| Troubleshooting.md | Issues encountered and how they were resolved |

| OU-Structure.md | Documentation of Organizational Units |

| User-Management.md | User and security group administration |

| Client-Domain-Join.md | Domain joining process for CLIENT01 |

| Group-Policy.md | Group Policy configuration and testing |



\---



\# Completed Documentation



\## Domain Controller Deployment

\- Installed Windows Server 2022

\- Renamed server to DC01

\- Configured static IP addressing

\- Installed AD DS and DNS roles

\- Promoted server to Domain Controller

\- Verified replication and DNS health



\## Active Directory Structure

Created the following Organizational Units:



```text

Company

├── Users

├── Groups

├── Computers

├── Servers

└── Service Accounts

```



\## Security Groups



```text

IT\_Admins

HelpDesk

HR

Sales

```



\## Test Users



| Name | Username | Department |

|------|-----------|-------------|

| John Smith | jsmith | IT |

| Sarah Brown | sbrown | Help Desk |

| Emily Davis | edavis | HR |

| Mike Wilson | mwilson | Sales |



\---



\# Screenshots



Screenshots supporting this documentation can be found in:



```text

../Screenshots/

```



Current screenshots include:



\- DC01-IPConfig.png

\- DC01-DomainInfo.png

\- DC01-DCDiag-01.png

\- DC01-DCDiag-02.png

\- DC01-DCDiag-03.png

\- DC01-DCDiag-04.png

\- OU-Structure.png

\- Security-Groups.png

\- AD-Users.png



\---



\# Lessons Learned



\- Active Directory relies heavily on proper DNS configuration.

\- Documentation and screenshots make troubleshooting easier.

\- PowerShell significantly speeds up Active Directory administration.

\- Version control with Git provides an excellent way to track lab progress.

\- Troubleshooting virtualization and networking issues is a valuable skill in itself.



\---



\# Upcoming Tasks



\- Deploy CLIENT01

\- Join CLIENT01 to the domain

\- Configure Group Policy Objects (GPOs)

\- Create shared folders and NTFS permissions

\- Configure password policies

\- Test domain authentication

\- Finalize documentation and portfolio presentation

