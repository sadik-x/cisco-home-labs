# Lab: Configuring portfast,bpdu guard,root guard

# Objective
Configure and verify a Spanning Tree Protocol (STP) topology with a root bridge, non-root bridges, and security features like PortFast, BPDU Guard, and Root Guard, ensuring a loop-free network while shutting down Gigabit connections for FastEthernet prioritization.

---

# Topology Overview  
- **3 Switches (one root bridge, two non-root bridges)**

  - Switch_0: Root bridge  

  - Switch_1: Non-root bridge  

  - Switch_2: Non-root bridge

# Multiple PCs connected to each switch (all FastEthernet ports with BPDU and PortFast shutdown)

- **Configured Features** 
  - Spanning Tree Protocol (STP) configuration:  
  - PortFast, BPDU Guard, and Root Guard enabled

# Switch ports:  
  - Root bridge (Switch_0) with ports fa0/6 (to non-root Switch_1) and fa0/7 (to Switch_2 with root guard)  

  - Non-root bridge (Switch_1) with ports fa0/6 and fa0/7  

  - Non-root bridge (Switch_2) with fa0/1 (root guard enabled)

  -**Gigabit connections shutdown on all switches**

# Technologies Used  
  - Spanning Tree Protocol (STP)  

  - PortFast  

  - BPDU Guard  

  - Root Guard  

  - Cisco IOS CLI

## Results  
  - Switch_0 correctly operates as the root bridge  

  - Non-root bridges (Switch_1, Switch_2) properly configured with STP features  

  - Root Guard on Switch_2 (fa0/1) functioning as expected  

  - No loops detected, network stable with STP configuration


