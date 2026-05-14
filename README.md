## Active Directory Home Lab
 
A beginner-friendly home lab simulating a real-world enterprise environment using Windows Server 2025 and Active Directory. Built to develop and demonstrate core Systems Administration and IT Security skills.
 
---
 
## Overview
 
This lab sets up a Windows Server 2022 Domain Controller with Active Directory Domain Services (AD DS), connects a Windows 10 client machine to the domain, and enforces security policies through Group Policy Objects (GPOs).
 
---
 
## Tools & Technologies
 
| Windows Server 2025 -> Domain Controller / AD DS |
| Windows 10 -> Domain client machine |
| VirtualBox -> Virtualization (free) |
| Active Directory Users & Computers (ADUC) -> User & group management |
| Group Policy Management (GPMC) -> Security policy enforcement |
| DNS Server -> Name resolution for the domain | 

## What Was Configured
 
- Deployed Windows Server 2025 as a Domain Controller with AD DS and DNS
- Created Organizational Units (OUs): IT, HR.
- Created and managed user accounts and security groups using ADUC
- Joined a Windows 10 client machine to the domain
- Configured Group Policy Objects (GPOs) enforcing:
  - Minimum password length of 12 characters
  - Password complexity requirements
  - Account lockout after 5 failed attempts

## How to Recreate This Lab
 
**Requirements:**
- VirtualBox
- Windows Server 2025 ISO
- Windows 10 ISO 
- 8GB+ RAM and 80GB+ free disk space
  
**Steps:**
1. Create a VM in VirtualBox (4GB RAM, 50GB disk) and install Windows Server 2025 **Desktop Experience**
2. Rename server to DClab
3. Install AD DS and DNS roles via Server Manager
4. Promote the server to a Domain Controller with domain `JSSlab.local`
5. Create OUs, users, and groups in ADUC
6. Configure GPOs in Group Policy Management
7. Create a Windows 10 VM, point DNS to the IP address of DClab, and join the domain
