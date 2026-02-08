# Active Directory Home Lab

## Overview
Built a Windows Server 2025 Domain Controller in VirtualBox to create a functional Active Directory environment for hands-on learning and skill development.

## Environment
- **Hypervisor:** Oracle VirtualBox 7.2.6
- **Operating System:** Windows Server 2025 Standard Evaluation
- **Domain Name:** cookin.local
- **Server Name:** GCDC-01
- **Resources:** 2GB RAM, 2 CPU cores, 60GB storage

## What I Built

### 1. Domain Controller Setup
- Installed and configured Windows Server 2025
- Promoted server to Domain Controller
- Created domain: `cookin.local`
- Configured DNS services

### 2. Organizational Structure
Created logical OU (Organizational Unit) structure:
```
cookin.local/
├── Employees/
│   ├── Accounting/
│   ├── IT/
│   ├── Human Resources/
│   └── Help Desk/
├── Computers/
└── Domain Controllers/
```

### 3. User & Group Management
- Created 10+ domain user accounts across different departments
- Established security groups for role-based access control
- Implemented manager/employee relationships using AD Organization tab
- Configured nested security groups (Help_Desk_L1, Help_Desk_L2 → Help_Desk_All)

### 4. File Sharing & Permissions
- Created shared network folder: `\\GCDC-01\SharedData`
- Configured NTFS permissions:
  - FinanceManager: Full Control
  - Accounting Group: Modify
  - Domain Users: Read Only
- Set up Share permissions with least-privilege principle
- Mapped network drives for easy user access

### 5. Network Drive Mapping
- Mapped `\\GCDC-01\SharedData` to Z: drive
- Demonstrated understanding of UNC paths vs drive letters
