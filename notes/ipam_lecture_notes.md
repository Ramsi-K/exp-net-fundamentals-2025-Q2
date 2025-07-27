# 🧠 IP Address Management (IPAM) – Lecture Notes

## 🎯 What You're Supposed to Learn

- **IP Address Management (IPAM):**

  - IPAM is the system for planning, tracking, and managing IP addresses in a network.
  - Used in large organizations to avoid conflicts and keep track of every device's IP.

- **IPv4 vs IPv6:**

  - IPv4 = 32-bit addresses (e.g., 192.168.1.1)
  - IPv6 = 128-bit addresses (e.g., 2001:0db8:85a3::8a2e:0370:7334)
  - We're running out of IPv4, so IPv6 is the future.

- **DHCP (Dynamic Host Configuration Protocol):**

  - Automatically gives IP addresses to devices
  - Saves admins from assigning IPs manually
  - Has concepts like "leases" (temporary assignments), which can expire

- **Static vs Dynamic IPs:**

  - Static = assigned manually, doesn’t change
  - Dynamic = changes over time, assigned via DHCP

- **Common Problems IPAM Solves:**

  - IP conflicts (two devices with same IP = bad)
  - Duplicate assignments
  - Expired DHCP leases not reclaimed
  - No tracking of which device had which IP at what time

- **IPAM Tools Usually Include:**

  - A centralized dashboard for subnet management
  - Audit logs of IP usage
  - DNS and DHCP integration
  - Alerts for IP conflicts or misconfigurations

## 🖼️ Simple Diagram

```mermaid
graph TD
    A[Devices] -->|DHCP Request| B[DHCP Server]
    B --> C[IP Assignment (Lease)]
    C --> D[IPAM System]
    D -->|Logs + Inventory| E[Admin View]
    D --> F[Alerts & Monitoring]
```

## 🧪 Pro Tips / Real-World Stuff

- In big companies, people plug in rogue devices → IPAM catches it
- You can reserve IPs for specific MAC addresses
- Some IPAM tools integrate with cloud networks (AWS, Azure)
- Security logs often rely on accurate IP tracking

## 📌 Key Terms

- IPAM = IP Address Management
- DHCP = Dynamic Host Configuration Protocol
- Lease = Temporary IP assignment
- MAC Address = Physical address of a device’s network card
- Subnet = A logical division of an IP network
- Conflict = Two devices trying to use the same IP

---
