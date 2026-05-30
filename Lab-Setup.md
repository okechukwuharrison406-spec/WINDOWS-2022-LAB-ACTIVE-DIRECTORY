# Lab Environment Setup: Active Directory Domain Configuration

## Lab Title

**Active Directory Domain Setup & Configuration**

---

### Platform

- Windows Server 2022 (Virtual Machine)

---

### Lab Overview

This lab simulates a modern enterprise environment for Active Directory (AD) deployment and security testing, including domain controller setup, group policy configuration, user/group management, Kerberos/LDAP experiments, SQL Server integration, and CTF scenarios.

---

## 1. Active Directory Domain Services (AD DS) Installation

**Host:** Server2022 (Windows Server 2022 VM)

#### Steps Performed

1. **Login** to Windows Server 2022 (Server2022).
2. **Server Manager** → Add Roles and Features.
3. **Role-based or feature-based installation** selected.
4. **Selected destination server:** Server2022.
5. **Checked** `Active Directory Domain Services` under Server Roles. Clicked **Add Features** when prompted.
6. **Confirmed selection,** enabled "Restart automatically if required."
7. Clicked **Install** and waited for completion, then closed the wizard.

#### Installed Components

- **Active Directory Domain Services (AD DS)**
- **Remote Server Administration Tools**
  - Role Administration Tools  
    - AD DS and AD LDS Tools
      - Active Directory Administrative Center
      - AD DS Snap-Ins and Command-Line Tools
      - Active Directory module for Windows PowerShell

---

## 2. Lab Property Details

| Property              | Details                                                |
|-----------------------|-------------------------------------------------------|
| **Lab Title**         | Active Directory Domain Setup & Configuration         |
| **Platform**          | Windows Server 2022 (Virtual Machine)                 |
| **Domain Name**       | (Specify as configured)                               |
| **Domain Controller** | Server2022                                            |
| **Operating Systems** | Windows Server 2022, Windows 11, Windows Server 2019  |
| **Tools Used**        | Server Manager, AD DS, Group Policy, ADSI Edit, SQL Server 2019|

---

## 3. Virtual Machine Inventory

| Host Name   | OS/Dist             | Role/Use Case                  |
|-------------|---------------------|--------------------------------|
| Server2022  | Windows Server 2022 | Primary Domain Controller      |
| Windows11   | Windows 11          | Domain Workstation             |
| SQL_srv     | Windows Server 2019 | SQL Server + Domain Member     |
| Parrot OS   | Parrot Security     | Attack Machine (Pentesting)    |
| Kali Linux  | Kali Linux          | Attack Machine (Pentesting)    |

---

## 4. Network Topology

Create or sketch a diagram showing:

- **Server2022** as AD Domain Controller
- **Windows11** and **SQL_srv** joined to domain
- **Parrot OS** and **Kali Linux** able to access internal network for attack/defense exercises

*(For visuals, use diagramming tools, or insert a table format or ASCII art if preferred)*

---

## 5. Skills Demonstrated

- Windows Server 2022 administration, role-based installation & troubleshooting
- Active Directory Domain Services (AD DS) installation and domain controller promotion
- New forest/domain creation (functional level: Windows Server 2016)
- Group Policy Management — password policies, GPOs
- Active Directory user/group administration
- Kerberos pre-authentication configuration (for As-Rep Roasting simulation)
- LDAP attribute/service edits with ADSI Edit
- SQL Server 2019 installation and login setup (on domain-joined host)
- CTF/Blue Team scenario: BO2K backdoor service simulation
- Multi-OS domain join: Windows 11, Server 2019

---

## References

- [Lab Author LinkedIn](https://linkedin.com/in/Harrison-Okechukwu)
- [Lab Author GitHub](https://github.com/HarrisonOkechukwu)