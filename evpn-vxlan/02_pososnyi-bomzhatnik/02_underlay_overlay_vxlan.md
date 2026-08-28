- **UNDERLAY: EBGP**
- **OVERLAY: IBGP**
  - No RRs => Full Mesh
- **2 Spines, 3 Leaves**
- **1 EVI: VLAN-AWARE on Spines**
  - RoutingInstanse FABRIC on Spines = GRT on Leaves
- **2 vlans/2 VNIs:**
  - vlan100-vni5100
  - vlan101-vni5101
  - FABRIC imports both VNIs NLRIs via VNI communities   
- **4 Servers:**
  - S6,S7,S8 - single-homed
  - S9 - dual-homed 
- **L3 GW: Virtual Gateway (Redundant L3 VXLAN Gateway) on Spines**

### UNDERLAY - EBGP
#### SPINE1
```
set routing-options autonomous-system 65001
set routing-options router-id 192.168.1.1
set protocols bgp log-updown
set protocols bgp group UNDERLAY neighbor 172.16.13.1 peer-as 65003
set protocols bgp group UNDERLAY neighbor 172.16.14.1 peer-as 65004
set protocols bgp group UNDERLAY neighbor 172.16.15.1 peer-as 65005

set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
```
#### SPINE2
```
set routing-options autonomous-system 65002
set routing-options router-id 192.168.1.2
set protocols bgp log-updown
set protocols bgp group UNDERLAY neighbor 172.16.23.1 peer-as 65003
set protocols bgp group UNDERLAY neighbor 172.16.24.1 peer-as 65004
set protocols bgp group UNDERLAY neighbor 172.16.25.1 peer-as 65005

set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
```
#### LEAF3
```
set routing-options autonomous-system 65003
set routing-options router-id 192.168.1.3
set protocols bgp log-updown
set protocols bgp group UNDERLAY neighbor 172.16.13.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.23.0 peer-as 65002

set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
```
#### LEAF4
```
set routing-options autonomous-system 65004
set routing-options router-id 192.168.1.4
set protocols bgp log-updown
set protocols bgp group UNDERLAY neighbor 172.16.14.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.24.0 peer-as 65002

set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
```
#### LEAF5
```
set routing-options autonomous-system 65005
set routing-options router-id 192.168.1.5
set protocols bgp log-updown
set protocols bgp group UNDERLAY neighbor 172.16.15.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.25.0 peer-as 65002

set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
```
#### ALL DEVICES
- BFD - detect within 10 seconds:
```
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 5
```
- BGP Multipath:
```
set protocols bgp group UNDERLAY multipath multiple-as
```
- DataPlane Load Balance:
```
set policy-options policy-statement LOAD-BALANCE term 1 then load-balance per-flow
set routing-options forwarding-table export LOAD-BALANCE
```
### OVERLAY - IBGP
- 
```

```
### ENABLE VXLAN


### GlobalParams


# GlobalParams
