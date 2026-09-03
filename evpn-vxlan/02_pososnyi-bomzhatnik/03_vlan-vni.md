## Single-homed - only S6,S7,S8 (LEAF3/LEAF4)
- VNI NLRIs marked with RT community: target:65500:$VNI
### CONFIGURATION
#### LEAF3
```
set interfaces ge-0/0/6 unit 0 family ethernet-switching interface-mode trunk vlan members 100
set interfaces ge-0/0/7 unit 0 family ethernet-switching interface-mode trunk vlan members 100
set interfaces ge-0/0/6 unit 0 family ethernet-switching vlan members 101
set interfaces ge-0/0/7 unit 0 family ethernet-switching vlan members 101
```
#### LEAF4
```
set interfaces ge-0/0/8 unit 0 family ethernet-switching interface-mode trunk vlan members 100
set interfaces ge-0/0/8 unit 0 family ethernet-switching vlan members 101
```
#### Both LEAF3 and LEAF4 
```
set vlans VLAN_100 vlan-id 100 vxlan vni 5100
set protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set protocols evpn extended-vni-list 5100
set policy-options community RT-VNI-5100 members target:65500:5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 from community RT-VNI-5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 then accept

set vlans VLAN_101 vlan-id 101 vxlan vni 5101
set protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set protocols evpn extended-vni-list 5101
set policy-options community RT-VNI-5101 members target:65500:5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 from community RT-VNI-5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 then accept
```

### VERIFICATION
- **LEAF4 discovers remote LEAF3 VTEP:**
```
root@LEAF4> show ethernet-switching vxlan-tunnel-end-point remote summary
Logical System Name       Id  SVTEP-IP         IFL   L3-Idx    SVTEP-Mode    ELP-SVTEP-IP
<default>                 0   192.168.1.4      lo0.0    0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 192.168.1.3      default-switch           349       vtep.32769   589     RNVE
```
- **LEAF4 learns MACs in default-switch Routing Instance:**
```
root@LEAF4> show ethernet-switching table
Ethernet switching table : 4 entries, 4 learned
Routing instance : default-switch
   Vlan                MAC                 MAC       GBP    Logical                SVLBNH/      Active
   name                address             flags     tag    interface              VENH Index   source
   VLAN_100            aa:bb:cc:00:60:00   DR               vtep.32769                          192.168.1.3
   VLAN_100            aa:bb:cc:80:60:00   DR               vtep.32769                          192.168.1.3
   VLAN_100            aa:bb:cc:80:70:00   DR               vtep.32769                          192.168.1.3
   VLAN_100            aa:bb:cc:80:80:00   D                ge-0/0/8.0
```

- **Servers can ping each other and learn ARPs:**
```
S8#show arp
Protocol  Address          Age (min)  Hardware Addr   Type   Interface
Internet  10.200.100.1           11   aabb.cc80.6000  ARPA   Vlan100
Internet  10.200.100.2           10   aabb.cc80.7000  ARPA   Vlan100
Internet  10.200.100.3            -   aabb.cc80.8000  ARPA   Vlan100
```
- **Leaves discover Type2 NLRIs:** 
  -  bgp.evpn.0 table:
```
root@LEAF4> show route match-prefix "2*"
bgp.evpn.0: 6 destinations, 6 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 00:25:35, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 00:00:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 00:00:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 00:00:04
                       Indirect
```
  - default-switch.evpn.0 table:
```
default-switch.evpn.0: 6 destinations, 6 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 00:25:35, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 00:00:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 00:00:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 00:00:04
                       Indirect
```
- **View MACs learned from remote switches:**
```
root@LEAF4> show ethernet-switching vxlan-tunnel-end-point remote mac-table
Logical system   : <default>
Routing instance : default-switch
 Bridging domain : VLAN_100+100, VLAN : 100, VNID : 5100
   MAC                 MAC      Logical          Remote VTEP
   address             flags    interface        IP address
   aa:bb:cc:00:60:00   DR       vtep.32769       192.168.1.3
   aa:bb:cc:80:60:00   DR       vtep.32769       192.168.1.3
   aa:bb:cc:80:70:00   DR       vtep.32769       192.168.1.3
```
- **View VTEP interfaces counters**
```
root@LEAF4> show interfaces vtep
Physical interface: vtep, Enabled, Physical link is Up
  Interface index: 134, SNMP ifIndex: 512
  Type: Software-Pseudo, Link-level type: VxLAN-Tunnel-Endpoint, MTU: Unlimited, Speed: Unlimited
  Device flags   : Present Running
  Interface Specific flags: Internal: 0x200
  Link type      : Full-Duplex
  Link flags     : None
  Last flapped   : Never
    Input packets : 0
    Output packets: 0

  Logical interface vtep.32768 (Index 345) (SNMP ifIndex 542)
    Flags: Up SNMP-Traps 0x4000 Encapsulation: ENET2
    Ethernet segment value: 00:00:00:00:00:00:00:00:00:00, Mode: single-homed, Multi-homed status: Forwarding
    VXLAN Endpoint Type: Source, VXLAN Endpoint Address: 192.168.1.4, L2 Routing Instance: default-switch, L3 Routing Instance: default
    Input packets : 0
    Output packets: 0

  Logical interface vtep.32769 (Index 349) (SNMP ifIndex 543)
    Flags: Up SNMP-Traps Encapsulation: ENET2
    VXLAN Endpoint Type: Remote, VXLAN Endpoint Address: 192.168.1.3, L2 Routing Instance: default-switch, L3 Routing Instance: default
    Input packets : 1491
    Output packets: 168
    Protocol eth-switch, MTU: Unlimited
      Flags: Trunk-Mode, 0xc000000
```
- **View extensive EVPN info:**
```
root@LEAF4> show evpn instance extensive
Instance: __default_evpn__
  Route Distinguisher: 192.168.1.4:0
  Number of bridge domains: 0
  Number of neighbors: 0

Instance: default-switch
  Route Distinguisher: 192.168.1.4:65500
  Encapsulation type: VXLAN
  Duplicate MAC detection threshold: 5
  Duplicate MAC detection window: 180
  MAC database status                     Local  Remote
    MAC advertisements:                       1       3
    MAC+IP advertisements:                    0       0
    Default gateway MAC advertisements:       0       0
  Number of local interfaces: 3 (3 up)
    Interface name  ESI                            Mode             Status     AC-Role
    .local..5       00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
    ge-0/0/8.0      00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
    ge-0/0/9.0      00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
  Number of IRB interfaces: 0 (0 up)
  Number of protect interfaces: 0
  Number of bridge domains: 1
    VLAN  Domain-ID Intfs/up   IRB-intf  Mode            MAC-sync v4-SG-sync v6-SG-sync
    100   5100         2  2              Extended        Enabled  Disabled   Disabled
  Number of neighbors: 1
    Address               MAC    MAC+IP        AD        IM        ES Leaf-label DCI-Peer Flow-label DT2U-SID           DT2M-SID
    192.168.1.3             3         0         0         1         0                           NO
  Number of ethernet segments: 0
  Router-ID: 192.168.1.4
  Source VTEP interface IP: 192.168.1.4
  SMET Forwarding: Disabled
  RIB Table-ID: 184549385, Kernel Table-ID: 5, Kernel Table-Generation: 2
  EVPN instance flags: 0x300001814800
  RTT Update Timestamp: Aug 21 11:49:26.983 2026
  L2ALD state change Timestamp: Aug 21 11:49:26.996 2026
  Core-Isolation change TS: Aug 21 19:00:51.089 2026, Core-Isolated: N
  Last Core-Isolation Change Reason: bgp-peer-transition
```
- View Type2 advertisements:
  - Communities used:
    - RT configured for VNI: target:65500:5100
    - Encapsulation: VXLAN
  - ESI in single-homed: all-zeros

```
root@LEAF4> show route advertising-protocol bgp 192.168.1.3 detail match-prefix "2*"
bgp.evpn.0: 6 destinations, 6 routes (6 active, 0 holddown, 0 hidden)
* 2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP (1 entry, 1 announced)
 BGP group OVERLAY type Internal
     Route Distinguisher: 192.168.1.4:65500
     Route Label: 5100
     ESI: 00:00:00:00:00:00:00:00:00:00                                      //ESI
     Nexthop: Self
     Flags: Nexthop Change
     Localpref: 100
     AS path: [65500] I
     Communities: target:65500:5100 encapsulation:vxlan(0x8)                 //COMMUNITIES

default-switch.evpn.0: 6 destinations, 6 routes (6 active, 0 holddown, 0 hidden)
* 2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP (1 entry, 1 announced)
 BGP group OVERLAY type Internal
     Route Distinguisher: 192.168.1.4:65500
     Route Label: 5100
     ESI: 00:00:00:00:00:00:00:00:00:00
     Nexthop: Self
     Flags: Nexthop Change
     Localpref: 100
     AS path: [65500] I
     Communities: target:65500:5100 encapsulation:vxlan(0x8)
```
- **View routes marked with a community:**
```
root@LEAF4> show route community target:65500:5100 brief | match ^2
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
```



## Dual-homed - only LEAF5

### CONFIGURATION
#### LEAF5
- **Enable VXLAN:**
```
set vlans VLAN_100 vlan-id 100 vxlan vni 5100
set protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set protocols evpn extended-vni-list 5100
set policy-options community RT-VNI-5100 members target:65500:5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 from community RT-VNI-5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 then accept

set vlans VLAN_101 vlan-id 101 vxlan vni 5101
set protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set protocols evpn extended-vni-list 5101
set policy-options community RT-VNI-5101 members target:65500:5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 from community RT-VNI-5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 then accept
```

#### Both LEAF4 and LEAF5
- **Create AE:**
```
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:11
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 esi 00:00:00:00:00:00:00:00:00:11
set interfaces ae0 esi all-active
set interfaces ae0 unit 0 family ethernet-switching vlan members 100
set interfaces ae0 unit 0 family ethernet-switching vlan members 101
```
### VERIFICATION
- **View ESI via show int ae0:**
```
root@LEAF4> show interfaces ae0 | match "ethernet segment"
  Ethernet segment value: 00:00:00:00:00:00:00:00:00:11, Mode: all-active
root@LEAF5> show interfaces ae0 | match "ethernet segment"
  Ethernet segment value: 00:00:00:00:00:00:00:00:00:11, Mode: all-active
```
- **show evpn instance extensive:**
```
root@LEAF4> show evpn instance extensive
Instance: __default_evpn__
  Route Distinguisher: 192.168.1.4:0
  Number of bridge domains: 0
  Number of neighbors: 1
    Address               MAC    MAC+IP        AD        IM        ES Leaf-label DCI-Peer Flow-label DT2U-SID           DT2M-SID
    192.168.1.5             0         0         0         0         1                           NO

Instance: default-switch
  Route Distinguisher: 192.168.1.4:65500
  Encapsulation type: VXLAN
  Duplicate MAC detection threshold: 5
  Duplicate MAC detection window: 180
  MAC database status                     Local  Remote
    MAC advertisements:                       1       4
    MAC+IP advertisements:                    0       0
    Default gateway MAC advertisements:       0       0
  Number of local interfaces: 3 (3 up)
    Interface name  ESI                            Mode             Status     AC-Role
    .local..5       00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
    ae0.0           00:00:00:00:00:00:00:00:00:11  all-active       Up         Root
    ge-0/0/8.0      00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
  Number of IRB interfaces: 0 (0 up)
  Number of protect interfaces: 0
  Number of bridge domains: 1
    VLAN  Domain-ID Intfs/up   IRB-intf  Mode            MAC-sync v4-SG-sync v6-SG-sync
    100   5100         2  2              Extended        Enabled  Disabled   Disabled
  Number of neighbors: 2
    Address               MAC    MAC+IP        AD        IM        ES Leaf-label DCI-Peer Flow-label DT2U-SID           DT2M-SID
    192.168.1.3             3         0         0         1         0                           NO
    192.168.1.5             1         0         2         1         0                           NO
  Number of ethernet segments: 1
    ESI: 00:00:00:00:00:00:00:00:00:11
      Status: Resolved by IFL ae0.0
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: ae0.0, Status: Up/Forwarding
      Number of remote PEs connected: 1
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.5      5100       0               all-active
      DF Election Algorithm: MOD based
      Designated forwarder: 192.168.1.4
      Backup forwarder: 192.168.1.5
      Last designated forwarder update: Aug 22 13:23:41
  Router-ID: 192.168.1.4
  Source VTEP interface IP: 192.168.1.4
  SMET Forwarding: Disabled
  RIB Table-ID: 184549385, Kernel Table-ID: 5, Kernel Table-Generation: 2
  EVPN instance flags: 0x300001814800
  RTT Update Timestamp: Aug 21 11:49:26.984 2026
  L2ALD state change Timestamp: Aug 21 11:49:26.996 2026
  Core-Isolation change TS: Aug 22 13:23:16.390 2026, Core-Isolated: N
  Last Core-Isolation Change Reason: evpn-peer-transition
```


## Type4 NLRI - ES Route
- **ES-sharing Leaf sends Type4 to all Leaves**
- **All Leaves receive, only same-ES nodes accept**
- **DF election:**
  - ES-sharing Leaves form a list of all Leaf Loopbacks
  - VLANID mod N_nodes = i,
    - i - order in the list of ES-sharing Leaves
  - Leaf number i is elected as a DF
- **DF - forwards BUM traffic from fabric to Client**
- **For VLAN_100: i = 100 mod 2=0 => lowest Loopback is a DF:**
```
root@LEAF5> show evpn instance designated-forwarder
Instance: default-switch
  Number of ethernet segments: 1
    ESI: 00:00:00:00:00:00:00:00:00:11
      Designated forwarder: 192.168.1.4

root@LEAF4> show evpn instance designated-forwarder
Instance: default-switch
  Number of ethernet segments: 1
    ESI: 00:00:00:00:00:00:00:00:00:11
      Designated forwarder: 192.168.1.4
```
- **Non-ES-sharing Leaf is aware of the ES, but is not aware about DF:**
```
root@LEAF3> show evpn instance designated-forwarder
Instance: default-switch
  Number of ethernet segments: 1
    ESI: 00:00:00:00:00:00:00:00:00:11
```
- **Autogenerated RD 192.168.1.5:0 and RT es-import-target:0-0-0-0-0-0 for ES scope exchange**
- **ExtCommunities:**
  - Encapsulation
  - ES-Import RT (autogenerated) 
- **NLRI:**
  - Autogenerated RT
  - ESI
```
root@LEAF5> show route advertising-protocol bgp 192.168.1.4 match-prefix "4*" detail
bgp.evpn.0: 17 destinations, 17 routes (17 active, 0 holddown, 0 hidden)
* 4:192.168.1.5:0::11:192.168.1.5/296 ES (1 entry, 1 announced)
 BGP group OVERLAY type Internal
     Route Distinguisher: 192.168.1.5:0                         #RD
     Nexthop: Self
     Flags: Nexthop Change
     Localpref: 100
     AS path: [65500] I
     Communities: encapsulation:vxlan(0x8) es-import-target:0-0-0-0-0-0    #ES-IMPORT RT

default-switch.evpn.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
__default_evpn__.evpn.0: 3 destinations, 3 routes (3 active, 0 holddown, 0 hidden)
* 4:192.168.1.5:0::11:192.168.1.5/296 ES (1 entry, 1 announced)
 BGP group OVERLAY type Internal
     Route Distinguisher: 192.168.1.5:0
     Nexthop: Self
     Flags: Nexthop Change
     Localpref: 100
     AS path: [65500] I
     Communities: encapsulation:vxlan(0x8) es-import-target:0-0-0-0-0-0
```
<img width="520" height="501" alt="image" src="https://github.com/user-attachments/assets/02eb218b-9c03-4cfa-a002-e9f1f4d5430b" />

- **Routers have a hidden policy __vrf-import-__default_evpn__-internal__:**
  - **Non ES-sharing LEAF3 has empty list of communities:**
```
root@LEAF3> show policy
Configured policies:
FABRIC-IMPORT
LOAD-BALANCE
LOOPBACK-TO-BGP
__evpn-export-default-switch-bd-override-5100-internal__
__evpn-import-autoderive-default-switch-internal__
__vrf-export-default-switch-internal__
__vrf-import-__default_evpn__-internal__     //POLICY HERE
__vrf-import-default-switch-internal__

root@LEAF3> show policy __vrf-import-__default_evpn__-internal__
Policy __vrf-import-__default_evpn__-internal__: [EVPN_ESI]
    Term unnamed:
        from
             community __vrf-community-__default_evpn__-import-internal__ []    //COMMUNITY LIST HERE
        then
               accept
    Term unnamed:
        then
               reject
``` 
- 
  - **ES-sharing LEAF4 has list of communities containing ES-import RT:**
```
root@LEAF4# run show policy
Configured policies:
FABRIC-IMPORT
LOAD-BALANCE
LOOPBACK-TO-BGP
__evpn-export-default-switch-bd-override-5100-internal__
__evpn-import-autoderive-default-switch-internal__
__vrf-export-default-switch-internal__
__vrf-import-__default_evpn__-internal__      //POLICY HERE
__vrf-import-default-switch-internal__

root@LEAF4# run show policy __vrf-import-__default_evpn__-internal__
Policy __vrf-import-__default_evpn__-internal__: [EVPN_ESI]
    Term unnamed:
        from
             community __vrf-community-__default_evpn__-import-internal__ [es-import-target:0-0-0-0-0-0]  //COMMUNITY LIST HERE
        then
               accept
    Term unnamed:
        then
               reject
```



## Type1 NLRI - AD (Auto Discovery) route
- LEAF3 receives Type1 ESI/EVIs from Multihoming LEAF4 and LEAF5:
```
root@LEAF3> show route match-prefix "1:*"
bgp.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI                                 //ESI HERE 
                   *[BGP/170] 23:18:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI                                 //EVI HERE 
                   *[BGP/170] 23:18:28, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI                                 //ESI HERE 
                   *[BGP/170] 23:18:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI                                 //EVI HERE 
                   *[BGP/170] 23:18:28, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0

default-switch.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI                                 //ESI HERE 
                   *[BGP/170] 23:18:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI                                 //EVI HERE 
                   *[BGP/170] 23:18:28, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI                                 //ESI HERE 
                   *[BGP/170] 23:18:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI                                 //EVI HERE 
                   *[BGP/170] 23:18:28, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
```
### Type1 per-ES 
- **Autogenerated RDs: 192.168.1.4:0, 192.168.1.5:0**
- **Communities:**
  - Encapsulation
  - **RT - All configured EVIs (including Global)**
  - **ESI-Label ExtCommunity = 0**
- **NLRI contains:**
  - ESI
  - **Ethernet_Tag_ID = max_value**
  - VNI (0 for global)
```
root@LEAF3> show route match-prefix "1:192.168.1.4:0*" detail
bgp.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI (1 entry, 0 announced)
        *BGP    Preference: 170/-101
                Route Distinguisher: 192.168.1.4:0                //RD - autogenerated
                Next hop type: Indirect, Next hop index: 0
                Address: 0x809cc14
                Next-hop reference count: 6
                Kernel Table Id: 0
                Source: 192.168.1.4
                Protocol next hop: 192.168.1.4
                Indirect next hop: 0x2 no-forward INH Session ID: 0
                Indirect next hop: INH non-key opaque: 0x0 INH key opaque: 0x0
                State: <Active Int Ext>
                Local AS: 65003 Peer AS: 65500
                Age: 23:21:00   Metric2: 0
                Validation State: unverified
                Task: BGP_65500_65500.192.168.1.4
                AS path: I
                Communities: target:65500:1 encapsulation:vxlan(0x8) esi-label:0x0:all-active (label 0)    //COMMUNITIES
                Import Accepted
                Localpref: 100
                Router ID: 192.168.1.4
                Secondary Tables: default-switch.evpn.0
                Thread: junos-main

default-switch.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI (1 entry, 1 announced)
        *BGP    Preference: 170/-101
                Route Distinguisher: 192.168.1.4:0                //RD - autogenerated
                Next hop type: Indirect, Next hop index: 0
                Address: 0x809cc14
                Next-hop reference count: 6
                Kernel Table Id: 0
                Source: 192.168.1.4
                Protocol next hop: 192.168.1.4
                Indirect next hop: 0x2 no-forward INH Session ID: 0
                Indirect next hop: INH non-key opaque: 0x0 INH key opaque: 0x0
                State: <Secondary Active Int Ext>
                Local AS: 65003 Peer AS: 65500
                Age: 23:21:00   Metric2: 0
                Validation State: unverified
                Task: BGP_65500_65500.192.168.1.4
                Announcement bits (2): 0-default-switch-evpn 1-default-switch-evpn
                AS path: I
                Communities: target:65500:1 encapsulation:vxlan(0x8) esi-label:0x0:all-active (label 0)    //COMMUNITIES
                Import Accepted
                Localpref: 100
                Router ID: 192.168.1.4
                Primary Routing Table: bgp.evpn.0
                Thread: junos-main
```
<img width="520" height="663" alt="image" src="https://github.com/user-attachments/assets/90887c51-074f-4730-bb37-7f077cadabee" />

 -  Juniper depicts MPLS Label = 0 within NLRI for Type1-per-ES, but perhaps it is for EVPN-MPLS only:
<img width="1078" height="275" alt="image" src="https://github.com/user-attachments/assets/0cb73729-a53a-43d6-ba63-0bb9fdf01c57" />


### Type1 per-EVI (including global)
- **RDs configured for all VNIs: 192.168.1.4:65500, 192.168.1.5:65500**
- **Communities:**
  - Encapsulation
  - **RT for this EVI**
- **NLRI contains:**
  - ESI
  - **Ethernet_Tag_ID = 0**
  - VNI (0 for global)
```
root@LEAF3> show route match-prefix "1:192.168.1.4:65500*" detail
bgp.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
1:192.168.1.4:65500::11::0/192 AD/EVI (1 entry, 0 announced)
        *BGP    Preference: 170/-101
                Route Distinguisher: 192.168.1.4:65500          //RD configured for VNI
                Next hop type: Indirect, Next hop index: 0
                Address: 0x809cc14
                Next-hop reference count: 6
                Kernel Table Id: 0
                Source: 192.168.1.4
                Protocol next hop: 192.168.1.4
                Indirect next hop: 0x2 no-forward INH Session ID: 0
                Indirect next hop: INH non-key opaque: 0x0 INH key opaque: 0x0
                State: <Active Int Ext>
                Local AS: 65003 Peer AS: 65500
                Age: 23:21:29   Metric2: 0
                Validation State: unverified
                Task: BGP_65500_65500.192.168.1.4
                AS path: I
                Communities: target:65500:1 encapsulation:vxlan(0x8)          //COMMUNITIES
                Import Accepted
                Localpref: 100
                Router ID: 192.168.1.4
                Secondary Tables: default-switch.evpn.0
                Thread: junos-main

default-switch.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
1:192.168.1.4:65500::11::0/192 AD/EVI (1 entry, 1 announced)
        *BGP    Preference: 170/-101
                Route Distinguisher: 192.168.1.4:65500
                Next hop type: Indirect, Next hop index: 0
                Address: 0x809cc14
                Next-hop reference count: 6
                Kernel Table Id: 0
                Source: 192.168.1.4
                Protocol next hop: 192.168.1.4
                Indirect next hop: 0x2 no-forward INH Session ID: 0
                Indirect next hop: INH non-key opaque: 0x0 INH key opaque: 0x0
                State: <Secondary Active Int Ext>
                Local AS: 65003 Peer AS: 65500
                Age: 23:21:29   Metric2: 0
                Validation State: unverified
                Task: BGP_65500_65500.192.168.1.4
                Announcement bits (1): 0-default-switch-evpn
                AS path: I
                Communities: target:65500:1 encapsulation:vxlan(0x8)
                Import Accepted
                Localpref: 100
                Router ID: 192.168.1.4
                Primary Routing Table: bgp.evpn.0
                Thread: junos-main
``` 
<img width="528" height="627" alt="image" src="https://github.com/user-attachments/assets/5ad92ed0-b3b3-4931-b75e-f18f13fac411" />

