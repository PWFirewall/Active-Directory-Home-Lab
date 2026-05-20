# 🧱 Active Directory Home Lab (Windows Server 2022)

## 🔷 Overview

This project demonstrates how to set up a Windows Active Directory environment using Windows Server 2022 and Windows 11 virtual machines. It simulates a real enterprise network with domain services, users, groups, and shared resources.

The lab was built to practice core system administration skills, including identity management, DNS configuration, domain joining, and troubleshooting network authentication issues.

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
CLIENT01 could not locate the domain during the join process.

**Cause:**
Client was using incorrect DNS settings (public DNS instead of DC01).

**Fix:**
- Set CLIENT01 DNS server to DC01 IP address
- Removed external DNS entries
- Retried domain join successfully

---

## 📸 Screenshots

#### ISO's Downloaded
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/01-isos-downloaded.png

#### First GitHub Repo Created
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/02-github-repo-created.png

#### DC01 VM Setup
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/03-dc01-vm-setup.png

#### CLIENT01 VM Setup
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/04-client01-vm-setup.png

#### DC01 Install
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/05-dc01-fresh-install.png

#### DC01 Renamed
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/06-dc01-renamed.png

#### DC01 Static IP
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/07-dc01-static-ip.png

#### Domain Creation
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/08-domain-creation.png

#### AD Console
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/09-ad-console.png

#### Users Created
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/10-users-created.png

#### Groups Created
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/11-groups-created.png

#### File Share Permissions
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/12-share-permissions.png

#### CLIENT01 Desktop
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/13-client-desktop.png

#### CLIENT01 DNS
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/14-client-dns.png

#### CLIENT01 Ping To DC01
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/15-ping-dc01-success.png

#### Setting DNS Primary
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/16-setting-dns-primary.png

#### Confirm DNS Set
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/17-confirm-dns-set.png

#### Domain Join paullab.local
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/18-domain-join-paullab-local.png

#### Login Domain Account
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/19-login-domain-account.png

#### CLIENT01 In ADUC
https://github.com/PWFirewall/Active-Directory-Home-Lab/blob/main/screenshots/20-client01-in-aduc.png

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
