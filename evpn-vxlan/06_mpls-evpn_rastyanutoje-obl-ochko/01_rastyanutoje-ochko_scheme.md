**2 DCs**  
- Assville
- Ballsackcity
**Servers - kind of DC-owned hypervisors**

**Each DC has 2 EVIs:**
- VLAN-Aware with 3 EVPN segments:
  - vlan11 | RT=target:65500:11 
  - vlan12 | RT=target:65500:12  
  - vlan13 | RT=target:65500:13 

- VLAN-Based:
- Assville
  - vlan100 on all PEs | RT=target:65500:100200 
- Ballsackcity
  - vlan200 on PE1,PE2 | RT=target:65500:100200

**DC provides three L2-domains-per-DC with repeating addressing and L3 GWs:**
- **Assville** on PE1, PE2:
  - vlan11 | 192.168.1.0/24 | Virtual GW (aka Distributed acst GW)
  - vlan12 | 192.168.1.0/24 | Virtual GW (aka Distributed acst GW) 
  - vlan13 | 192.168.1.0/24 | Anycast (IP+MAC) 
  - vlan100 | 192.168.100.0/24 | Virtual GW (aka Distributed acst GW) 
- **Ballsackcity** on PE3, PE4:
  - vlan11 | 192.168.2.0/24 | Virtual GW (aka Distributed acst GW) 
  - vlan12 | 192.168.2.0/24 | Virtual GW (aka Distributed acst GW) 
  - vlan13 | 192.168.2.0/24 |  Anycast (IP+MAC) 
  - vlan200 | 192.168.200.0/24 | Virtual GW (aka Distributed acst GW)

**L3VPNs:**
- **VLAN-AWARE EVIs in both DCs:**
  - IRB.11 | RIB = GLOBAL (No dedicated L3VPN) | | L3 scope: Global, no vrf-target
  - IRB.12 | RIB = L3VPN_12 | RT=65500:12 | L3 scope: dedicated L3VPN
  - IRB.13 | RIB = L3VPN_13 | RT=65500:13 | L3 scope: dedicated L3VPN
- **VLAN-BASED EVIs:**
  - Assville | IRB.100 | RIB = L3VPN_100 | RT=65500:100200 | L3 scope: dedicated L3VPN
  - Ballsackcity | IRB.200 | RIB = L3VPN_200 | RT=65500:100200 | L3 scope: dedicated L3VPN
 
<img width="1332" height="1082" alt="image" src="https://github.com/user-attachments/assets/308e9ede-3de9-4c02-ab59-a345b6d4f020" />

