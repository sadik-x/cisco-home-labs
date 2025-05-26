# Lab: Configuring Voice and Data VLANs with IP Phones and PCs
# Objective
  -Set up a network with voice and data VLANs using a multilayer switch and a router. Configure the router as the default gateway, enable inter-VLAN routing, and ensure IP phones and PCs are assigned IP addresses in their respective VLANs (Voice     VLAN 55 for IP phones, Data VLAN 44 for PCs).
# Topology Overview  
  -1 Router 

  -1 Multilayer Switch

  -4 IP Phones (VLAN 55, 172.16.1.0/24)  

  -4 PCs (VLAN 44, 192.168.7.0/24)

# Configured Features  
  -VLAN creation on the multilayer switch:  
  
  -VLAN 55 (Phone VLAN)  

  -VLAN 44 (Data VLAN)

  -Trunk ports (fa0/5) 
  
  -Access ports (fa0/1-4)

Router configured as the default gateway (fa0/0)  

# IP phones and PCs assigned to their respective VLANs with dynamic IP addressing:  
  -IP Phones: 172.16.1.0/24 (VLAN 55)  

  -PCs: 192.168.7.0/24 (VLAN 44)

## Technologies Used  
-VLANs  

-802.1Q Trunking  

-Cisco IOS CLI  

-IP Telephony (Voice VLAN)

## Results  
-IP phones in VLAN 55 successfully received IP addresses in the 172.16.1.0/24 subnet.  

-PCs in VLAN 44 successfully received IP addresses in the 192.168.7.0/24 subnet.  

-Trunk links correctly passed VLAN-tagged traffic for voice and data.

