- No VRF configured
- Spine1 and Spine2 are RRs with unique clusters
- Two VLANs:
  - VLANID: 100; VNI: 20100
  - VLANID: 200; VNI: 20200
- switch-options > RT is equal on all Leaves
 
# GlobalParams
### Interfaces, LB, BGP with multipath, Loopback-to-EBGP
#### SPINE1
```
set system host-name SPINE1

set interfaces ge-0/0/3 unit 0 family inet address 172.16.13.0/31
set interfaces ge-0/0/4 unit 0 family inet address 172.16.14.0/31
set interfaces ge-0/0/5 unit 0 family inet address 172.16.15.0/31
set interfaces lo0 unit 0 family inet address 1.1.1.1/32

set policy-options policy-statement EXPORT-LO term 1 from protocol direct
set policy-options policy-statement EXPORT-LO term 1 from interface lo0.0
set policy-options policy-statement EXPORT-LO term 1 then accept
set policy-options policy-statement LB-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LB-POLICY term 1 then accept

set routing-options router-id 1.1.1.1
set routing-options autonomous-system 65530
set routing-options forwarding-table export LB-POLICY
```
#### LEAF4
```
set system host-name LEAF4

set vlans DATA100 vlan-id 100
set vlans DATA200 vlan-id 200

set interfaces ge-0/0/1 unit 0 family inet address 172.16.14.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.24.1/31
set interfaces ge-0/0/8 unit 0 family ethernet-switching interface-mode access
set interfaces ge-0/0/8 unit 0 family ethernet-switching vlan members 200
set interfaces ge-0/0/9 unit 0 family ethernet-switching interface-mode access
set interfaces ge-0/0/9 unit 0 family ethernet-switching vlan members 100
set interfaces lo0 unit 0 family inet address 4.4.4.4/32

set policy-options policy-statement EXPORT-LO term 1 from protocol direct
set policy-options policy-statement EXPORT-LO term 1 from interface lo0.0
set policy-options policy-statement EXPORT-LO term 1 then accept
set policy-options policy-statement LB-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LB-POLICY term 1 then accept
set routing-options router-id 4.4.4.4
set routing-options autonomous-system 65530
set routing-options forwarding-table export LB-POLICY
```
# Underlay EBGP
- ASN per-device
- Built on interface IPs
- Multipath with multiple-as
- Each Spine with each Leaf, each Leaf with each Spine
#### SPINE1
```
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY export EXPORT-LO
set protocols bgp group UNDERLAY local-as 64511
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY neighbor 172.16.13.1 peer-as 64513
set protocols bgp group UNDERLAY neighbor 172.16.14.1 peer-as 64514
set protocols bgp group UNDERLAY neighbor 172.16.15.1 peer-as 64515
```
#### LEAF4
```
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY export EXPORT-LO
set protocols bgp group UNDERLAY local-as 64514
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY neighbor 172.16.14.0 peer-as 64511
set protocols bgp group UNDERLAY neighbor 172.16.24.0 peer-as 64512
```

# Overlay IBGP
- Address Family: EVPN
- RRs Spine1 and Spine2 help avoid full-mesh
- multipath within a common AS
#### SPINE1
```
 set prot bgp group OVERLAY type internal
 set prot bgp group OVERLAY local-as 65530
 set prot bgp group OVERLAY local-address 1.1.1.1
 set prot bgp group OVERLAY cluster 1.1.1.1
 set prot bgp group OVERLAY multipath
 set prot bgp group OVERLAY neighbor 2.2.2.2
 set prot bgp group OVERLAY neighbor 3.3.3.3
 set prot bgp group OVERLAY neighbor 4.4.4.4
 set prot bgp group OVERLAY neighbor 5.5.5.5
 set prot bgp group OVERLAY family evpn signaling

```
#### LEAF4
```
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 4.4.4.4
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65530
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 1.1.1.1
set protocols bgp group OVERLAY neighbor 2.2.2.2
```
##### Multipath vs Load Balance:
BGP multipath - works in RIB
- Before multipath:
```
root@LEAF4> show route 3.3.3.3
inet.0: 8 destinations, 11 routes (8 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

3.3.3.3/32         *[BGP/170] 00:09:02, localpref 100
                               AS path: 64511 64513 I, validation-state: unverified
                          >  to 172.16.14.0 via ge-0/0/1.0
                         [BGP/170] 00:08:58, localpref 100
                               AS path: 64512 64513 I, validation-state: unverified
                          >  to 172.16.24.0 via ge-0/0/2.0
```
 - After multipath:

```
root@LEAF4> show route 3.3.3.3
inet.0: 8 destinations, 11 routes (8 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both
3.3.3.3/32         *[BGP/170] 00:00:05, localpref 100
                      AS path: 64511 64513 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                        to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 00:11:17, localpref 100
                      AS path: 64512 64513 I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
```
LB - works in FIB
- Before LB:
```
root@LEAF4> show route forwarding-table destination 3.3.3.3 table default
Routing table: default.inet
Internet:
Destination        Type RtRef Next hop           Type Index    NhRef Netif
3.3.3.3/32         user     0 172.16.14.0        ucst      587     5 ge-0/0/1.0
```
- After LB:
```
root@LEAF4> show route forwarding-table destination 3.3.3.3 table default
Routing table: default.inet
Internet:
Destination        Type RtRef Next hop           Type Index    NhRef Netif
3.3.3.3/32         user     0                    ulst  1048574     2
                              172.16.14.0        ucst      587     5 ge-0/0/1.0
                              172.16.24.0        ucst      588     5 ge-0/0/2.0
```

# VXLAN - anycast-gateway, VLANID-to-VNI mapping, EVPN
- Only on Leaves
- IRB has configured:
  - A unique physical IP
  - A shared IP - anycast
  - A shared MAC - anycast
- VLAN-VNI mapping - for this VLAN and this VNI:
  - When BUM traffic rx-ed - it needs to be replicated it to all VTEPs


#### LEAF4
```
set interfaces irb unit 100 family inet address 192.168.100.44/24 virtual-gateway-address 192.168.100.1
set interfaces irb unit 100 virtual-gateway-v4-mac 10:bb:cc:dd:ee:ff
set interfaces irb unit 200 family inet address 192.168.200.44/24 virtual-gateway-address 192.168.200.1
set interfaces irb unit 200 virtual-gateway-v4-mac 20:bb:cc:dd:ee:ff

set vlans DATA100 vxlan vni 20100
set vlans DATA100 vxlan ingress-node-replication
set vlans DATA100 l3-interface irb.100

set vlans DATA200 vxlan vni 20200
set vlans DATA200 vxlan ingress-node-replication
set vlans DATA200 l3-interface irb.200

set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn extended-vni-list 20100
set protocols evpn extended-vni-list 20200

set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 4.4.4.4:530
set switch-options vrf-target target:65530:530

set routing-options forwarding-table chained-composite-next-hop ingress evpn
```

# Verify
- SPINE tables:
```
root@SPINE1> show route | match routes
inet.0: 11 destinations, 17 routes (11 active, 0 holddown, 0 hidden)
inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
bgp.evpn.0: 32 destinations, 64 routes (32 active, 0 holddown, 0 hidden)
```
- LEAF tables:
```
root@LEAF3> show route | match routes
inet.0: 12 destinations, 15 routes (12 active, 0 holddown, 0 hidden)
inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
bgp.evpn.0: 32 destinations, 56 routes (32 active, 0 holddown, 0 hidden)
default-switch.evpn.0: 31 destinations, 55 routes (31 active, 0 holddown, 0 hidden)
__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
```
- Leaves have inet.0 /32 EVPN routes to VPCs connected to them: 
```
root@LEAF4> show route protocol evpn table inet.0
inet.0: 15 destinations, 19 routes (15 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

192.168.100.20/32  *[EVPN/7] 1d 11:34:08
                    >  via irb.100
192.168.200.10/32  *[EVPN/7] 12:42:15
                    >  via irb.200
```

- show vlans:
```
root@LEAF4> show vlans

Routing instance        VLAN name             Tag          Interfaces
default-switch          DATA100               100
                                                           esi.636*
                                                           ge-0/0/9.0*
                                                           vtep.32769*
                                                           vtep.32770*
default-switch          DATA200               200
                                                           esi.637*
                                                           ge-0/0/8.0*
                                                           vtep.32769*
                                                           vtep.32770*
default-switch          default               1


```
- MAC table:
```
root@LEAF4> show ethernet-switching table

MAC flags (S - static MAC, D - dynamic MAC, L - locally learned, P - Persistent static, C - Control MAC
           SE - statistics enabled, NM - non configured MAC, R - remote PE MAC, O - ovsdb MAC,
           B - Blocked MAC)


Ethernet switching table : 8 entries, 8 learned
Routing instance : default-switch
   Vlan                MAC                 MAC       GBP    Logical                SVLBNH/      Active
   name                address             flags     tag    interface              VENH Index   source
   DATA100             00:50:79:66:68:0d   DR               vtep.32769                          3.3.3.3
   DATA100             00:50:79:66:68:0e   D                ge-0/0/9.0
   DATA100             10:bb:cc:dd:ee:ff   DRP              esi.636                             05:00:00:ff:fa:00:00:4e:84:00
   DATA100             2c:6b:f5:67:1b:f0   DR               vtep.32769                          3.3.3.3
   DATA200             00:50:79:66:68:0f   D                ge-0/0/8.0
   DATA200             00:50:79:66:68:10   DR               vtep.32770                          5.5.5.5
   DATA200             20:bb:cc:dd:ee:ff   DRP              esi.637                             05:00:00:ff:fa:00:00:4e:e8:00
   DATA200             2c:6b:f5:8f:aa:f0   DR               vtep.32770                          5.5.5.5

```
- EVPN database:
```

root@LEAF4> show evpn database
Instance: default-switch
VLAN  DomainId  MAC address        Active source                  Timestamp        IP address
     20100      00:50:79:66:68:0d  3.3.3.3                        Jun 02 16:51:27  192.168.100.10
     20100      00:50:79:66:68:0e  ge-0/0/9.0                     Jun 04 12:31:40  192.168.100.20
     20100      10:bb:cc:dd:ee:ff  05:00:00:ff:fa:00:00:4e:84:00  Jun 02 16:51:27  192.168.100.1
     20100      2c:6b:f5:67:1b:f0  3.3.3.3                        Jun 02 16:51:27  192.168.100.33
     20100      2c:6b:f5:93:73:f0  irb.100                        Jun 01 16:44:49  192.168.100.44
     20200      00:50:79:66:68:0f  ge-0/0/8.0                     Jun 04 12:31:48  192.168.200.10
     20200      00:50:79:66:68:10  5.5.5.5                        Jun 02 18:57:47  192.168.200.20
     20200      20:bb:cc:dd:ee:ff  05:00:00:ff:fa:00:00:4e:e8:00  Jun 02 16:51:27  192.168.200.1
     20200      2c:6b:f5:8f:aa:f0  5.5.5.5                        Jun 02 16:51:27  192.168.200.55
     20200      2c:6b:f5:93:73:f0  irb.200                        Jun 01 16:44:49  192.168.200.44

```
- vxlan commands are under ethernet-switching level:
```

root@LEAF4> show ethernet-switching vxlan-tunnel-end-point source
Logical System Name       Id  SVTEP-IP         IFL   L3-Idx    SVTEP-Mode    ELP-SVTEP-IP
<default>                 0   4.4.4.4          lo0.0    0
    L2-RTT                   Bridge Domain              VNID     Translation-VNID    MC-Group-IP    Interface
    default-switch           DATA100+100                20100                        0.0.0.0             vtep.32768
    default-switch           DATA200+200                20200                        0.0.0.0             vtep.32768
```
```
root@LEAF4> show ethernet-switching vxlan-tunnel-end-point remote
Logical System Name       Id  SVTEP-IP         IFL   L3-Idx    SVTEP-Mode    ELP-SVTEP-IP
<default>                 0   4.4.4.4          lo0.0    0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 3.3.3.3          default-switch           350       vtep.32769   634     RNVE
    VNID          MC-Group-IP
    20100         0.0.0.0
    20200         0.0.0.0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 5.5.5.5          default-switch           353       vtep.32770   635     RNVE
    VNID          MC-Group-IP
    20100         0.0.0.0
    20200         0.0.0.0

```
