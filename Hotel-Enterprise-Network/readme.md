## Lab:Hotel Enterprise Network Management
  # Network Overview
Central Cisco 2960-24TT Switch used to connect all devices.

Three main VLANs:

Admin VLAN 10: 192.168.10.0/24 (🟧 orange)

Guests VLAN 20: 192.168.20.0/24 (🟥 red)

Servers VLAN 30: 192.168.30.0/24 (🟦 blue)

  # Admin VLAN 10
-Hosts: PC0–PC4 (IP range: 192.168.10.10 to 192.168.10.14)

-Connected to switch ports Fa0/1 to Fa0/5

-All ports marked as secured (Port Security  enabled)

  # Guests VLAN 20
-Hosts: PC5–PC17 (IP range: 192.168.20.11 to 192.168.20.21)

-Connected to switch ports Fa0/6 to Fa0/16

  # Servers VLAN 30
-DHCP Server: 192.168.30.100

-SNMP Server: 192.168.30.200

--Connected to switch ports Fa0/17 and Fa0/18

  # Router Configuration
-Device: ISR4331 Router

-Router-on-a-Stick (ROAS) used for Inter-VLAN Routing

Interfaces:

g0/0/0: Connected to Cloud0 (internet simulation)

g0/0/1: Trunk port to switch

  # Network Services
-DHCP enabled via Server in VLAN30

-SNMP monitoring enabled via separate server

-SSH  enabled (router shows hostname hoteladmin, password hotel123)

-Syslog/SNMP management tools assumed active
