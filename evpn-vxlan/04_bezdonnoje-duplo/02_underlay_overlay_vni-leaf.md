## UNDERLAY 
- EBGP per-level: 
  - CORE: ASN=65100
  - SPINE: ASN=65200
  - LEAF: ASN=65300
- Configure the same export policy on every device 
  - Do not use the 'interface' statement in any of the match conditions.
  - e.g. use route-filter with prefix range to match IPs of Loopbacks
- Enable multipath and load-balance on LEAVEs and COREs
  - Not enabled on SPINEs
- BGP UNDERLAY speakers should be able to detect peer loss in 9 seconds without the use of BFD.

`set protocols bgp group $GROUPNAME hold-time 9`
- LEAF3 and LEAF5 must advertise all subnets they have gateways for:
  - LEAF3 - ge-0/0/8 - vlans 110-115
  - LEAF5 - ge-0/0/7 - vlans 130-135
- Export policy must not be changed when adding another VLAN/subnet
  - Apply-path to match all addresses into a prefix-list for a policy:

#### Both COREs
```
set routing-options autonomous-system 65100
set protocols bgp group CORE-SPINE peer-as 65200
set protocols bgp group CORE-SPINE multipath
set protocols bgp group CORE-SPINE hold-time 9
!
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 then accept
set protocols bgp group CORE-SPINE export LOOPBACK-to-BGP
!
set policy-opt policy-stat LOAD-BALANCE term PER-FLOW then load-balance per-flow
set routing-options forwarding-table export LOAD-BALANCE
```

#### CORE6
```
set protocols bgp group CORE-SPINE neighbor 172.16.16.1
set protocols bgp group CORE-SPINE neighbor 172.16.26.1
set routing-options router-id 192.168.1.6
```

#### CORE7
```
set protocols bgp group CORE-SPINE neighbor 172.16.17.1
set protocols bgp group CORE-SPINE neighbor 172.16.27.1
set routing-options router-id 192.168.1.7
```

#### Both SPINEs
```
set routing-options autonomous-system 65200
!
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 then accept
!
set protocols bgp group CORE-SPINE peer-as 65100
set protocols bgp group CORE-SPINE export LOOPBACK-to-BGP
set protocols bgp group CORE-SPINE hold-time 9
!
set protocols bgp group SPINE-LEAF peer-as 65300
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF hold-time 9
```
#### SPINE1
```
set protocols bgp group CORE-SPINE neighbor 172.16.16.0
set protocols bgp group CORE-SPINE neighbor 172.16.17.0
set protocols bgp group SPINE-LEAF neighbor 172.16.13.1
set protocols bgp group SPINE-LEAF neighbor 172.16.14.1
set protocols bgp group SPINE-LEAF neighbor 172.16.15.1
```

#### SPINE2
```
set protocols bgp group CORE-SPINE neighbor 172.16.26.0
set protocols bgp group CORE-SPINE neighbor 172.16.27.0
set protocols bgp group SPINE-LEAF neighbor 172.16.23.1
set protocols bgp group SPINE-LEAF neighbor 172.16.24.1
set protocols bgp group SPINE-LEAF neighbor 172.16.25.1
```

#### All LEAVEs
```
set routing-options autonomous-system 65300
set routing-options autonomous-system loops 2
set policy-opt policy-stat LOAD-BALANCE term PER-FLOW then load-balance per-flow
set routing-options forwarding-table export LOAD-BALANCE
!
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-opt policy-stat LOOPBACK-to-BGP term LOOPBACK_0 then accept
!
set protocols bgp group SPINE-LEAF peer-as 65200
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF multipath
set protocols bgp group SPINE-LEAF hold-time 9
```

#### LEAF3
```
set protocols bgp group SPINE-LEAF neighbor 172.16.13.0
set protocols bgp group SPINE-LEAF neighbor 172.16.23.0
!
set vlans VLAN_110 vlan-id 110
set vlans VLAN_111 vlan-id 111
set vlans VLAN_112 vlan-id 112
set vlans VLAN_113 vlan-id 113
set vlans VLAN_114 vlan-id 114
set vlans VLAN_115 vlan-id 115
!
set interfaces ge-0/0/8 vlan-tagging
set interfaces ge-0/0/8 unit 110 vlan-id 110
set interfaces ge-0/0/8 unit 110 family inet address 10.200.110.1/24
set interfaces ge-0/0/8 unit 111 vlan-id 111
set interfaces ge-0/0/8 unit 111 family inet address 10.200.111.1/24
set interfaces ge-0/0/8 unit 112 vlan-id 112
set interfaces ge-0/0/8 unit 112 family inet address 10.200.112.1/24
set interfaces ge-0/0/8 unit 113 vlan-id 113
set interfaces ge-0/0/8 unit 113 family inet address 10.200.113.1/24
set interfaces ge-0/0/8 unit 114 vlan-id 114
set interfaces ge-0/0/8 unit 114 family inet address 10.200.114.1/24
set interfaces ge-0/0/8 unit 115 vlan-id 115
set interfaces ge-0/0/8 unit 115 family inet address 10.200.115.1/24
!
set policy-options prefix-list ge-0/0/8_ALL-ADDRESSES apply-path "interfaces ge-0/0/8 unit <*> family inet address <*>"
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs from prefix-list ge-0/0/8_ALL-ADDRESSES
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs then accept
set protocols bgp group SPINE-LEAF export DIRECT-to-BGP
```

- **Verify:**
```
root@LEAF3> show configuration policy-options prefix-list ge-0/0/8_ALL-ADDRESSES | display inheritance
##
## apply-path was expanded to:
##     10.200.110.0/24;
##     10.200.111.0/24;
##     10.200.112.0/24;
##     10.200.113.0/24;
##     10.200.114.0/24;
##     10.200.115.0/24;
##
apply-path "interfaces ge-0/0/8 unit <*> family inet address <*>";

root@SPINE2> show route protocol bgp 10.200.0.0/16 | match BGP
Warning: License key missing; requires 'BGP' license
10.200.110.0/24    *[BGP/170] 00:03:39, localpref 100
10.200.111.0/24    *[BGP/170] 00:03:39, localpref 100
10.200.112.0/24    *[BGP/170] 00:03:39, localpref 100
10.200.113.0/24    *[BGP/170] 00:03:39, localpref 100
10.200.114.0/24    *[BGP/170] 00:03:39, localpref 100
10.200.115.0/24    *[BGP/170] 00:03:39, localpref 100
```

#### LEAF4
```
set protocols bgp group SPINE-LEAF neighbor 172.16.14.0
set protocols bgp group SPINE-LEAF neighbor 172.16.24.0
```
####LEAF5
```
set protocols bgp group SPINE-LEAF neighbor 172.16.15.0
set protocols bgp group SPINE-LEAF neighbor 172.16.25.0
!
set vlans VLAN_130 vlan-id 130
set vlans VLAN_131 vlan-id 131
set vlans VLAN_132 vlan-id 132
set vlans VLAN_133 vlan-id 133
set vlans VLAN_134 vlan-id 134
set vlans VLAN_135 vlan-id 135
!
set interfaces ge-0/0/7 vlan-tagging
set interfaces ge-0/0/7 unit 130 vlan-id 130
set interfaces ge-0/0/7 unit 130 family inet address 10.200.130.1/24
set interfaces ge-0/0/7 unit 131 vlan-id 131
set interfaces ge-0/0/7 unit 131 family inet address 10.200.131.1/24
set interfaces ge-0/0/7 unit 132 vlan-id 132
set interfaces ge-0/0/7 unit 132 family inet address 10.200.132.1/24
set interfaces ge-0/0/7 unit 133 vlan-id 133
set interfaces ge-0/0/7 unit 133 family inet address 10.200.133.1/24
set interfaces ge-0/0/7 unit 134 vlan-id 134
set interfaces ge-0/0/7 unit 134 family inet address 10.200.134.1/24
set interfaces ge-0/0/7 unit 135 vlan-id 135
set interfaces ge-0/0/7 unit 135 family inet address 10.200.135.1/24
!
set policy-options prefix-list ge-0/0/7_ALL-ADDRESSES apply-path "interfaces ge-0/0/7 unit <*> family inet address <*>"
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs from prefix-list ge-0/0/7_ALL-ADDRESSES
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs then accept
set protocols bgp group SPINE-LEAF export DIRECT-to-BGP
```


## OVERLAY 
- IBGP on LEAVEs and COREs
  - No RRs => Full Mesh

#### All LEAVEs
```
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
```

#### LEAF3
```
set routing-options router-id 192.168.1.3
set protocols bgp group OVERLAY local-address 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
```

#### LEAF4
```
set routing-options router-id 192.168.1.4
set protocols bgp group OVERLAY local-address 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
```

#### LEAF5
```
set routing-options router-id 192.168.1.5
set protocols bgp group OVERLAY local-address 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
```

#### Both COREs
```
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
```

- Not sure what is OSPF for

```
set chassis aggregated-devices ethernet device-count 1
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ge-0/0/8 gigether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set protocols ospf area 0.0.0.0 interface ae0.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface lo0.0 passive
```

#### CORE6
```
set routing-options route-distinguisher-id 192.168.1.6
set protocols bgp group OVERLAY local-address 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.7
!
set interfaces ae0 unit 0 family inet address 192.168.0.0/31
```

#### CORE7
```
set routing-options route-distinguisher-id 192.168.1.7
set protocols bgp group OVERLAY local-address 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
!
set interfaces ae0 unit 0 family inet address 192.168.0.1/31
```

## VNIs on LEAVEs
- The servers are expecting tagged frames. It should be possible to tunnel VLANs inside VLAN 230.
  - By default, tunneled frames will have their VLAN stripped.
  - Configure the VXLAN itself to encapsulate the VLAN: `set vlans vlan vxlan encapsulate-inner-vlan`
  - Configure the QFX to accept VXLAN packets that still contain the inner-VLAN.
    - This is a global setting:
`set protocols l2-learning decapsulate-accept-inner-vlan`
//SVI v 230 TAK NIHUYA NEDOSTUPNY, A ETOT TUNNELING NE NASTRAIVAETSA - NU I NAHOOYA TOGDA?
- Every VNI should have a different RT
#### LEAF3
`set switch-options route-distinguisher 192.168.1.3:65500`

#### LEAF4
`set switch-options route-distinguisher 192.168.1.4:65500`

#### LEAF5
`set switch-options route-distinguisher 192.168.1.5:65500`

### VNIs 5220,5230 - All LEAVEs
```
set vlans VLAN_220 vxlan vni 5220
set vlans VLAN_230 vxlan vni 5230
set vlans VLAN_230 vxlan encapsulate-inner-vlan
!
set protocols evpn encapsulation vxlan
set protocols evpn extended-vni-list all
set protocols evpn multicast-mode ingress-replication
!
set protocols l2-learning decapsulate-accept-inner-vlan
set switch-options vtep-source-interface lo0.0
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
```

### VNI 5240 - LEAF3, LEAF4
`set vlans VLAN_240 vxlan vni 5240`













