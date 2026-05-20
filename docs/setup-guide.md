Setup Guide

## 1. Install Windows Server 2022
- Deploy VM (VirtualBox or VMware)
- Assign static IP address

---

## 2. Configure Domain Controller
- Rename server to DC01
- Install Active Directory Domain Services role
- Promote server to Domain Controller
- Create new forest:
  - Example Domain: paullab.local

---

## 3. Configure DNS
- Ensure DNS role is installed
- Verify forward lookup zone is created
- Confirm SRV records exist

---

## 4. Create Users and Groups
- Open Active Directory Users and Computers
- Create organizational units (OUs)
- Add users and assign to groups

---

## 5. Setup Shared Folder
- Create shared directory
- Assign permissions based on AD groups

---

## 6. Configure Client Machine
- Install Windows 11
- Set DNS to DC01 IP address
- Join domain: paullab.local
