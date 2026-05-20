# 🧱 Active Directory Home Lab (Windows Server 2022)

## 🔷 Overview

This project demonstrates the setup of a Windows Active Directory environment using Windows Server 2022 and Windows 11 virtual machines. It simulates a real enterprise network with domain services, users, groups, and shared resources.

The lab was built to practice core system administration skills including identity management, DNS configuration, domain joining, and troubleshooting network authentication issues.

---

## ⚙️ Technologies Used

- Windows Server 2022
- Windows 11
- Active Directory Domain Services (AD DS)
- DNS
- VMware / VirtualBox

---

## 🖥️ Environment

| Machine | Role |
|--------|------|
| DC01 | Domain Controller |
| CLIENT01 | Domain Joined PC |

---

## 🎯 Objectives

- Install and configure Active Directory
- Create a domain environment
- Manage users and security groups
- Configure shared network folders and permissions
- Join a client machine to the domain
- Test authentication and network connectivity

---

## 🏗️ Setup Summary

### Domain Controller (DC01)
- Installed Windows Server 2022
- Configured static IP and DNS
- Installed Active Directory Domain Services
- Promoted server to Domain Controller
- Created domain: **paullab.local**

---

### Active Directory Configuration
- Created organizational users
- Created security groups
- Assigned users to appropriate groups
- Configured basic access control

---

### File Sharing & Permissions
- Created shared network folder
- Applied group-based permissions
- Tested access control using domain users

---

### Client Machine (CLIENT01)
- Installed Windows 11
- Configured DNS to point to DC01
- Joined machine to domain: **paullab.local**
- Verified domain authentication

---

## 🚨 Issues Encountered & Fixes

### ❌ DNS Misconfiguration Prevented Domain Join

**Problem:**
CLIENT01 could not locate the domain during join process.

**Cause:**
Client was using incorrect DNS settings (public DNS instead of DC01).

**Fix:**
- Set CLIENT01 DNS server to DC01 IP address
- Removed external DNS entries
- Retried domain join successfully

---

## 📸 Screenshots

> (Add images in `/screenshots` folder and link them below)

### 

---

## 🧠 Lessons Learned

- DNS is critical for Active Directory functionality — without it, domains cannot resolve
- Domain authentication depends heavily on correct network configuration
- Group-based permissions simplify administration and improve scalability
- Most Active Directory issues are caused by misconfigured DNS or network settings
- Troubleshooting is a core IT skill and requires step-by-step validation

---

## 🚀 Key Takeaways

This lab provided hands-on experience with:
- Enterprise identity management
- Domain-based authentication systems
- Windows Server administration
- Network troubleshooting techniques
- Real-world IT infrastructure design

---

## 🔧 Future Improvements

- Implement Group Policy Objects (GPOs)
- Add additional domain users and role separation
- Configure roaming profiles or folder redirection
- Add PowerShell automation scripts for user creation
