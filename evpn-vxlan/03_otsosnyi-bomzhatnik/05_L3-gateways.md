### VNI 5100-5104 - Virtual GW (Redundant Layer 3 VXLAN Gateway) on SPINEs
#### SPINE1
```
set int irb.100 fam inet addr 10.200.100.252/24 virtual-gateway-address 10.200.100.254
set int irb.101 fam inet addr 10.200.101.252/24 virtual-gateway-address 10.200.101.254
set int irb.102 fam inet addr 10.200.102.252/24 virtual-gateway-address 10.200.102.254
set int irb.103 fam inet addr 10.200.103.252/24 virtual-gateway-address 10.200.103.254
set int irb.104 fam inet addr 10.200.104.252/24 virtual-gateway-address 10.200.104.254
```

#### SPINE2
```
set int irb.100 fam inet addr 10.200.100.253/24 virtual-gateway-address 10.200.100.254
set int irb.101 fam inet addr 10.200.101.253/24 virtual-gateway-address 10.200.101.254
set int irb.102 fam inet addr 10.200.102.253/24 virtual-gateway-address 10.200.102.254
set int irb.103 fam inet addr 10.200.103.253/24 virtual-gateway-address 10.200.103.254
set int irb.104 fam inet addr 10.200.104.253/24 virtual-gateway-address 10.200.104.254
```

#### ALL SPINEs
```
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 routing-interface irb.100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 routing-interface irb.102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 routing-interface irb.103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 routing-interface irb.104
```

### VNI 5105-5108 - Unicast GW on SPINEs
- Make sure there is IP connectivity between the different subnets
  - e.i. advertise the subnet we configure on the IRB interface into OSPF
#### SPINE1
```
set protocols ospf area 0.0.0.0 interface irb.105 passive
set protocols ospf area 0.0.0.0 interface irb.106 passive
!
set interfaces irb unit 105 family inet address 10.200.105.254/24
set interfaces irb unit 106 family inet address 10.200.106.254/24
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-105 routing-interface irb.105
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-106 routing-interface irb.106
```
#### SPINE2
```
set protocols ospf area 0.0.0.0 interface irb.107 passive
set protocols ospf area 0.0.0.0 interface irb.108 passive
!
set interfaces irb unit 107 family inet address 10.200.107.254/24
set interfaces irb unit 108 family inet address 10.200.108.254/24
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-107 routing-interface irb.107
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-108 routing-interface irb.108
```

### VNI 5109-5110 - Anycast GW on SPINEs (Manual GW Sync)
#### SPINE1
```
set int irb.109 fam inet address 10.200.109.254/24
set int irb.109 mac aa:aa:aa:aa:aa:09
set int irb.110 fam inet address 10.200.110.254/24
set int irb.110 mac aa:aa:aa:aa:aa:10
```

#### SPINE2
```
set int irb.109 fam inet address 10.200.109.254/24
set int irb.109 mac aa:aa:aa:aa:aa:09
set int irb.110 fam inet address 10.200.110.254/24
set int irb.110 mac aa:aa:aa:aa:aa:10
```
