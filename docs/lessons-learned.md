# Lessons Learned

## Technical Insights

- DNS is the foundation of Active Directory
- Without proper DNS, domain services will fail completely
- Domain controllers must always use static IP addressing

---

## System Behavior Understanding

- Active Directory relies on SRV records for domain discovery
- Client machines must point to internal DNS (not external providers)

---

## Key Takeaways

- Most AD issues originate from DNS misconfiguration
- Group-based permissions are more scalable than individual permissions
- Step-by-step troubleshooting is essential in system administration
