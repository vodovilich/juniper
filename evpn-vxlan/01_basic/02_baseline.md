- No VRF configured
- Spine1 adn Spine2 are RRs with unique clusters
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
