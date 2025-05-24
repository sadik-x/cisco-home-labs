# Lab : Router as DHCP Server for Multiple VLANs with Multilayer Switch

# Objective
Configure a router to act as a centralized DHCP server for multiple VLANs across a network with a multilayer switch and normal switches. Enable inter-VLAN routing and DHCP Relay to dynamically assign IP addresses in the correct subnet for each VLAN.

---

# Topology Overview
- **1 Router** (DHCP server + default gateway)

- **1 Multilayer Switch** (Layer 3 routing + VLAN segmentation)

- **3 Normal Switches**

**Multiple PCs** in different VLANs:

- VLAN 11 – IT

- VLAN 22 – Sales

- VLAN 33 – Support

---

# Configured Features
- VLAN creation on multilayer switch and normal switches

- Trunk ports connecting multilayer switch and normal switches

- Layer 3 VLAN interfaces (SVIs) on multilayer switch for routing

- Router configured as DHCP server with pools for each VLAN subnet:

    -`192.168.11.0/24` for VLAN 11

    -`192.168.22.0/24 `for VLAN 22

    -`192.168.33.0/24` for VLAN 33

- ip helper-address configured on multilayer switch SVIs pointing to router’s DHCP server IP

- PCs obtaining IP addresses dynamically from router DHCP pools

---  

# Technologies Used
- VLANs

- 802.1Q Trunking

- Layer 3 Switch VLAN Interfaces (SVIs)

- DHCP Server (on Router)

- DHCP Relay (ip helper-address)

- Cisco IOS CLI

---

# Results
-PCs in each VLAN successfully received IP addresses from router DHCP server.

-Inter-VLAN routing enabled seamless communication between VLANs.

-DHCP relay forwarded DHCP requests from VLANs to the router server correctly.

-Trunk links passed VLAN tagged traffic as expected.
