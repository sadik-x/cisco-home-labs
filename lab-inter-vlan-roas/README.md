# Lab : Inter-VLAN Routing with ROAS (Router-on-a-Stick)

# Objective
Configure Inter-VLAN communication using a single router and trunk link (ROAS method). Enable devices in different VLANs to communicate via subinterfaces on the router.

---

# Topology Overview
- **1 Router** (with subinterfaces)
- **1 Switch** (trunk connection to router, access ports to PCs)
- **3 PCs** in different VLANs:
  - VLAN 10 
  - VLAN 20 
  - VLAN 30 

---

# Configured Features
- VLAN creation and access port assignment
- Trunk port setup between switch and router
- Router subinterface configuration:
  - `Gig0/0.10` for VLAN 10
  - `Gig0/0.20` for VLAN 20
  - `Gig0/0.30` for VLAN 30
- IP addressing and gateway setup
- Inter-VLAN ping tests to verify connectivity

---

# Technologies Used
- VLANs
- Trunking (802.1Q)
- Router-on-a-Stick
- Cisco IOS CLI

---

# Results
- Successful communication between VLANs through the router
- Trunk port and subinterfaces working as expected


