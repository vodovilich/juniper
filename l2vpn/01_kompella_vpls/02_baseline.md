## BGP-signalled VPLS
- **Once a PE device receives a frame - PE creates a MAC table** (Forwarding table in junos)
- **Dst_Mac is typically unknown for PE device**
  - Processed as **UnknownUnicast**:
    - Sent out of **all RoutingInstance interfaces** except the receiving interface
  - **All PEs included into VRF receives the UnknownUnicast frame**
- **VPLS-marked interfaces on PE:**
```
root@PE1> show interfaces terse | match vpls
lc-0/0/0.32769          up    up   vpls
vt-0/0/0.1048576        up    up   vpls
ge-0/0/1.601            up    up   vpls
ge-0/0/2.601            up    up   vpls
```
- **MAC table for VRF on PE:** 
  - Virtual switch **keeps a MAC table**
  - Virtual switch **does not track IP addresses**
```
root@PE1> show vpls mac-table
MAC flags       (S -static MAC, D -dynamic MAC, L -locally learned, C -Control MAC
    O -OVSDB MAC, SE -Statistics enabled, NM -Non configured MAC, R -Remote PE MAC, P -Pinned MAC)
Routing instance : Customer1
 Bridging domain : __Customer1__, VLAN : NA
   MAC                 MAC      GBP     Logical          NH     MAC         active
   address             flags    Tag     interface        Index  property    source
   aa:bb:cc:00:60:00   D                ge-0/0/1.601
   aa:bb:cc:00:70:00   D                vt-0/0/0.1048576
   aa:bb:cc:00:80:00   D                ge-0/0/2.601
   aa:bb:cc:00:90:00   D                vt-0/0/0.1048576
```
  - **ARP bindings on CEs:**
```
CE1-R4#show arp
Protocol  Address          Age (min)  Hardware Addr   Type   Interface
Internet  192.168.10.1           71   aabb.cc00.6000  ARPA   Ethernet0/0.601
Internet  192.168.10.2           18   aabb.cc00.7000  ARPA   Ethernet0/0.601
Internet  192.168.10.3           70   aabb.cc00.8000  ARPA   Ethernet0/0.601
Internet  192.168.10.4            -   aabb.cc00.9000  ARPA   Ethernet0/0.601
```

- **BGP-VPLS: L2info > EncapsType: VPLS (19):**
<img width="952" height="698" alt="image" src="https://github.com/user-attachments/assets/8588bad7-a526-4031-ac05-b5e68af11305" />

- **BGP-VPWS: L2info > EncapsType: Ethernet(VLAN)TaggedMode (4):**
<img width="957" height="684" alt="image" src="https://github.com/user-attachments/assets/ccc1a28c-a36e-489f-bd2b-a3b005d3672f" />

- **Service Labels are signalled via BGP NLRI:**
<img width="1082" height="736" alt="image" src="https://github.com/user-attachments/assets/a42e7820-2025-42df-9825-14d4585454cf" />

- **CE_site4-CE_site3 ping request on PE1-P1 link:**	
  - **PHP takes place > only service label observable**
<img width="1090" height="287" alt="image" src="https://github.com/user-attachments/assets/a996ad61-90ef-451a-8fa8-8d2d590b18d2" />

- **800257 is assigned on PE2 based on BGP Update from P2:**
<img width="781" height="478" alt="image" src="https://github.com/user-attachments/assets/e0535a9c-d20f-4130-924d-0a8e98302a33" />

- **CE_site4-CE_site3 ping reply on PE1-P1 link:**
  - Two labels:
<img width="858" height="458" alt="image" src="https://github.com/user-attachments/assets/9f15cd88-fe65-4aa9-9183-0374c9ae76f6" />

- **800256 is  is assigned on PE1 based on BGP Update from P1:**
<img width="1010" height="614" alt="image" src="https://github.com/user-attachments/assets/a436353e-e88f-4d64-a0a1-2ba1f8336584" />

- **Labels on PE1:**
```
root@PE1> show vpls connections | except --
Layer-2 VPN connections:

Legend for connection status (St)

Legend for interface status

Instance: Customer1
Edge protection: Not-Primary
  Local site: Customer1-1 (1)
    connection-site           Type  St     Time last up          # Up trans
    2                         rmt   Up     Mar 22 10:21:38 2026           1
      Remote PE: 2.2.2.2, Negotiated control-word: No
      Incoming label: 800257, Outgoing label: 800256                    //OVER HERE!!!
      Local interface: vt-0/0/0.1048577, Status: Up, Encapsulation: VPLS
      Description: Intf - vpls Customer1 local site 1 remote site 2
      Flow Label Transmit: No, Flow Label Receive: No
    4                         rmt   RM
  Local site: Customer1-3 (3)
    connection-site           Type  St     Time last up          # Up trans
    2                         rmt   LM
    4                         rmt   LM
```

- **RFC 4761 - Labels are utilised per-PE, not per-Site:**
```
A label block, defined by a label base LB and a VE block size VBS, is a contiguous set of labels {LB, LB+1, ..., LB+VBS-1}
All PEs within a given VPLS are assigned unique VE IDs (VE - VPLS Edge device) as part of their configuration.
A PE X wishing to send a VPLS update sends the same label block information to all other PEs.  
Each receiving PE infers the label intended for PE X by adding its (unique) VE ID to the label base. 
In this manner, each receiving PE gets a unique demultiplexor for PE X for that VPLS.
All PEs within a given VPLS are assigned unique VE IDs as part of their configuration.  
A PE X wishing to send a VPLS update sends the same label block information to all other PEs. 
Each receiving PE infers the label intended for PE X by adding its (unique) VE ID to the label base.
In this manner, each receiving PE gets a unique demultiplexor for PE X for that VPLS.
```
- **RFC 4761 - Labels are signalled per-Site, and Path-Selection happens:**
```
When a BGP speaker receives two equivalent NLRIs (see below for the definition), it applies standard path selection criteria such as Local Preference and AS Path Length to determine which NLRI to choose; it MUST pick only one.  
If the chosen NLRI is subsequently withdrawn, the BGP speaker applies path selection to the remaining equivalent VPLS NLRIs to pick another; if none remain, the forwarding information associated with that NLRI is removed
```

- **PE1 rx-ed labels announced for site-2 and site-4, and selected site-3:**
  - Same label 800256 used for ping site1<->site2 and site1<->site4
    - Data starts with dst_mac src_mac
<img width="1082" height="262" alt="image" src="https://github.com/user-attachments/assets/1107ee51-aa31-4199-8b9c-a55d624d57e3" />

- **site1-to-site4 request on PE1_ge-0/0/0: Label 800256:**
<img width="966" height="249" alt="image" src="https://github.com/user-attachments/assets/656c58dc-3641-4bd7-ac58-71ba7b53a7aa" />

- **RM - remote site ID not minimum designated:**
```
root@PE1> show vpls connections | except --
Layer-2 VPN connections:
Legend for connection status (St)
Legend for interface status
Instance: Customer1
Edge protection: Not-Primary
  Local site: Customer1-1 (1)
    connection-site           Type  St     Time last up          # Up trans
    2                         rmt   Up     Mar 22 10:21:38 2026           1     
      Remote PE: 2.2.2.2, Negotiated control-word: No
      Incoming label: 800257, Outgoing label: 800256
      Local interface: vt-0/0/0.1048577, Status: Up, Encapsulation: VPLS
        Description: Intf - vpls Customer1 local site 1 remote site 2
      Flow Label Transmit: No, Flow Label Receive: No
    4                         rmt   RM    							        //OVER HERE!!!
  Local site: Customer1-3 (3)
    connection-site           Type  St     Time last up          # Up trans
    2                         rmt   LM
    4                         rmt   LM
```

- **Shutdown PE2 ge-0/0/1 (Site2):**
  - **Site2 now has the RD status**
  - **PE1 selected Labels signalled for Site4:**
<img width="912" height="447" alt="image" src="https://github.com/user-attachments/assets/765bc07f-33ff-4314-827a-7b4500402665" />


<img width="867" height="195" alt="image" src="https://github.com/user-attachments/assets/3da0b20d-7f2b-4c67-9ea8-2daed55b4733" />
