# Troubleshooting

## Issue: Domain not found during join

**Cause:**
Incorrect DNS configuration on client machine

**Fix:**
- Set DNS server to DC01 IP
- Remove external DNS entries
- Retry domain join

---

## Issue: Domain join fails intermittently

**Cause:**
Cached DNS records or propagation delay

**Fix:**
- ipconfig /flushdns
- Restart DNS service on DC01
- Retry join process
