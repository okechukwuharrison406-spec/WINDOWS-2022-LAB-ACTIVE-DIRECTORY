# 🏢 Active Directory Domain Setup Lab  
**Platform:** Windows Server 2022  
**Lab Author:** Harrison Okechukwu Udochukwu  
**LinkedIn:** [linkedin.com/in/Harrison-Okechukwu](https://linkedin.com/in/Harrison-Okechukwu)

---

## Overview

Configured a simulated enterprise Active Directory (AD) environment on Windows Server 2022 as part of a cybersecurity internship program. The lab focused on modern domain controller deployment, group policy configuration, user/group management, LDAP setup, and SQL Server integration for practical penetration testing and Blue Team exercises.

---

## Lab Environment (Generic Overview)

| Component         | Details                                       |
|-------------------|-----------------------------------------------|
| Domain            | (New AD Forest; generic internal domain)      |
| Domain Controller | Windows Server 2022 (virtual machine)         |
| Workstations      | Windows client, Windows Server member         |
| Attack Machines   | Linux-based security distributions            |
| Functional Level  | Windows Server 2016                           |

---

## Methodology and Key Steps

### 1. Install Active Directory Domain Services (AD DS)

- Used Server Manager to add the AD DS role on Windows Server 2022.
- Included management tools for AD administration.

### 2. Promote Server to Domain Controller

- Used post-installation configuration to create a new AD forest.
- Set appropriate forest/domain functional levels and DSRM password.
- Kept DNS and Global Catalog options enabled for typical enterprise management.

### 3. Group Policy Configuration

- Modified default password policies via Group Policy Management Console.
    - Adjusted history, age, length, and complexity to fit lab requirements.
- Used GPOs to simulate typical enterprise misconfigurations and policies.

### 4. User & Group Management

- Created multiple user accounts and groups for varied privilege levels.
- Demonstrated group membership assignment, admin delegation, and privilege escalation scenarios.
- Set various account properties (password policies, Kerberos pre-authentication options).

### 5. Service Principal Name (SPN) & Kerberos

- Registered custom SPNs for lab service accounts.
- Used PowerShell for automation.
- Explored Kerberos authentication and common misconfigurations.

### 6. LDAP & ADSI Edit Configuration

- Used ADSI Edit to modify LDAP settings and attributes (e.g., dSHeuristics).
- Demonstrated secure and misconfigured LDAP scenarios for security testing.

### 7. Domain Join Operations

- Joined multiple Windows machines to the AD domain (e.g., client and server roles).
- Performed troubleshooting for DNS, credential, and policy issues during domain join.

### 8. SQL Server Integration

- Installed Microsoft SQL Server on a domain member server.
- Configured authentication, logins, and role assignments.
- Simulated typical enterprise misconfigurations for password policy/enforcement.
- Demonstrated registry modification for persistence (simulated backdoor/use case).

---

## Commands & Automation Examples

```powershell
# Register an SPN for a service account
setspn -a <SPN> <DOMAIN>\<ServiceAccount>

# List SPNs for a user/service
setspn -L <DOMAIN>\<User>
```

---

## Skills Demonstrated

- Windows Server administration & AD DS deployment
- Active Directory forest/domain architecture & design
- Group Policy management (security/policy hardening & misconfiguration)
- User/group administration & privilege management
- LDAP/ADSI Edit for directory Attribute modification and security testing
- SPN registration & Kerberos configuration
- Troubleshooting domain join and authentication issues
- SQL Server setup in a domain environment with security focus
- Registry manipulation for persistence simulation (malware/defense)

---

## Next Steps & Related Labs

- AD security assessment and penetration testing (e.g., Kerberos/LDAP/SQL attacks)
- Blue Team monitoring, SIEM integration, and detection engineering labs
- Malware simulation and defense analysis

---

**Connect:**  
[GitHub](https://github.com/HarrisonOkechukwu) | [LinkedIn](https://linkedin.com/in/Harrison-Okechukwu)
