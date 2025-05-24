Lab: DHCP Server for Multiple VLANs with Router and Multilayer Switch
Objective
Configure a network with multiple VLANs using a multilayer switch and a router that acts as the DHCP server. Enable inter-VLAN routing and DHCP services so that devices in different VLANs obtain IP addresses and communicate across VLANs.

Topology Overview
1 Router acting as DHCP server and inter-VLAN router

1 Multilayer Switch performing VLAN segmentation and routing (SVIs)

3 Normal Switches connected to the multilayer switch, each assigned to a VLAN

VLANs:

VLAN 11 (IT)

VLAN 22 (Sales)

VLAN 33 (Support)

PCs connected on normal switches, assigned to corresponding VLAN access ports

Configured Features
VLAN creation on multilayer and normal switches

Trunk ports between multilayer switch and normal switches

Layer 3 VLAN interfaces (SVIs) configured on multilayer switch for routing

Router configured as DHCP server with separate DHCP pools for each VLAN subnet

DHCP relay (ip helper-address) configured on multilayer switch VLAN interfaces pointing to router's DHCP server IP

Inter-VLAN routing enabled for communication between VLANs

DHCP IP assignment and inter-VLAN connectivity verified via ping

Technologies Used
VLAN segmentation

802.1Q trunking

Layer 3 Switch VLAN Interfaces (SVIs)

Router acting as DHCP server

DHCP relay configuration

Cisco IOS CLI
