## Lab: Advanced ISP Network with HSRP, QoS, NAT, and Admin Services
# Objective
Simulate a realistic Internet Service Provider (ISP) network that delivers internet to multiple homes with different service levels, while ensuring high availability, traffic shaping, and administrative monitoring. This lab integrates core enterprise features like HSRP, ACLs, Syslog, QoS, and SSH for complete ISP-grade simulation.

# Topology Overview
-2 Core Routers (ISP-R1 & ISP-R2) with HSRP

-1 Distribution Switch connecting homes and admin services

-3 Home Routers (Home1, Home2, Home3)

-Admin Zone with Syslog Server, SNMP Manager, and Admin PC

-Simulated Internet using a separate router and PC (8.8.8.8)


# Configured Features
-- Routing & Redundancy
-Static routes from ISP to customer networks

-HSRP on core routers with 192.168.100.1 as virtual gateway

-Failover tested successfully between ISP-R1 and ISP-R2

-- NAT & ACLs
-NAT enabled for home networks to access internet

-ACL blocks Guest network (Home3) from accessing Admin Zone

-- VLANs & DHCP
-Each home router has its own subnet and DHCP pool

-Admin devices use static IPs in 192.168.100.0/24

-- QoS (Traffic Shaping)
-Bandwidth shaping applied using Class-Map + Policy-Map

-Example: Home1 capped at 800 Kbps

-Simulates STANDART,PREMIUM and ULTRA internet packages

-- Monitoring & Access
-Syslog Server receives logs from ISP routers

-SNMP configuration ready for monitoring(limited because of cisco packet tracer)

-SSH enabled for secure remote management of routers


