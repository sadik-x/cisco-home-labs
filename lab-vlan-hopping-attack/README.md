# Lab: VLAN Hopping Attack & Preventio

# Objective
Simulate a VLAN Hopping attack using double-tagging, demonstrate its impact on a multi-VLAN network, and implement security best practices to prevent it.

---

# Topology Overview
- **3 VLANs**:
  - VLAN 11: Attacker VLAN
  - VLAN 22: Victim VLAN
  - VLAN 33: Additional User VLAN
- **Native VLAN**: VLAN 99 (used for trunk links)
- **3 Switches**:
  - Each managing a separate VLAN group
- **PCs**:
  - VLAN 11: 6 devices (includes the attacker PC)
  - VLAN 22: 6 devices
  - VLAN 33: 6 devices

---

# Key Concepts
- **Double-tagging attack**:
  - Attacker sends specially crafted frames with two VLAN tags.
  - Switch strips the outer VLAN tag (native VLAN 99) and forwards the frame with the inner tag to the victim VLAN.
- **Trunk Exploitation**:
  - Trunk links with improperly configured native VLANs can forward these packets to unintended VLANs.

---

# Security Configuration (Prevention)
- `switchport nonegotiate` — disables Dynamic Trunking Protocol (DTP)
- Change native VLAN from default 1 to unused VLAN 99
- Set access ports explicitly with `switchport mode access`
- Disable unused ports: `shutdown`
- Ensure trunk links are strictly defined and monitored

---

# Results
- The VLAN Hopping attack can successfully reach other VLANs if misconfigurations exist.
- When prevention measures are implemented, the attack fails, securing the VLANs effectively.
