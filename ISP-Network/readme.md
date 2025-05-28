## Lab – Enterprise-Grade Home Access Network ISP Infrastructure Simulation
  #  Network Architecture Overview
Simulated an end-to-end ISP-grade network infrastructure in Cisco Packet Tracer, delivering internet connectivity to multiple customer sites (home networks) using dynamic IP assignment, PAT (Port Address Translation), centralized logging, and bandwidth shaping via advanced QoS policies. The design reflects real-world ISP deployment models with modularity, scalability, and centralized control.

---

# Technologies Implemented
- Dynamic Host Configuration Protocol (DHCP)
- Network Address Translation (NAT Overload)
- Class-Based QoS (CBWFQ + Policing)
- Syslog Logging (Centralized Log Aggregation)
- Static Routing Across Segmented Topologies
- Layer 2 Ethernet Switching (Distribution Layer)
- Fully Segregated LAN/WAN Design

  ---

# Multi-Tenant Home Networks
  -Each home router simulates a customer edge (CE) device, featuring LAN-side DHCP, NAT-enabled WAN uplinks, and customized bandwidth policies reflecting different subscription tiers.

**Home**	**LAN Subnet**	**WAN IP**	  **Bandwidth	Features**
-Home1	192.168.1.0/24	  100.0.0.2	    10 Mbps	DHCP, NAT, Static Route, QoS
-Home2	192.168.2.0/24	  100.0.0.3	    5 Mbps	DHCP, NAT, Static Route, QoS
-Home3	192.168.3.0/24	  100.0.0.4	    1 Mbps	DHCP, NAT, Static Route, QoS
-Home4	192.168.4.0/24	  100.0.0.5	    512 Kbps	DHCP, NAT, Static Route, QoS
-Home5	192.168.5.0/24	  100.0.0.6	    3 Mbps	DHCP, NAT, Static Route, QoS
-Home6	192.168.6.0/24	  100.0.0.7	    6 Mbps	DHCP, NAT, Static Route, QoS
-Home7	192.168.7.0/24	  100.0.0.8	    15 Mbps	DHCP, NAT, Static Route, QoS
-Home8	192.168.8.0/24	  100.0.0.9	    100 Mbps	DHCP, NAT, Static Route, QoS

--PCs in each LAN dynamically receive IPs via DHCP. Routing and NAT allow full upstream connectivity.

---

# ISP Edge Router (Cisco 2911)
-The ISP Core router serves as a Provider Edge (PE) device and is responsible for:

-Static routing to all customer LANs

-Serving as a central NAT handoff point

-Implementing service-policy input for traffic policing per customer

-Logging events to a remote Syslog server for compliance and diagnostics

  -Interfaces:
   -Interface	IP	Purpose;
    -G0/0	100.0.0.1/24	WAN Uplinks to Customers
    -G0/1	192.168.100.1/24	Syslog LAN

# Quality of Service (QoS) Configuration
-Implemented traffic shaping policies using Class Maps and Policy Maps on the ISP router to enforce SLA-based bandwidth tiers per customer connection.Traffic was shaped at the ISP ingress interface (G0/0) to ensure fair usage and simulate real-world ISP bandwidth throttling.

---

# Technical Skills Showcased
-Advanced Cisco IOS CLI Configuration

-Layer 3 Routing + Inter-subnet Communication

-Policy-Based Traffic Shaping

-Service Differentiation per Client

-Scalable and Modular Network Design

-Log Management and Event Monitoring


