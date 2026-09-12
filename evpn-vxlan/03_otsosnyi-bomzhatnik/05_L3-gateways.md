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

### SPINEs automatically create ESIs for EVPN L3 IRBs:
- SPINE2 participates in 10 ESIs:
```
root@SPINE2> show evpn instance esi-info
Instance: VLAN-AWARE_FABRIC-EVI
  Number of ethernet segments: 10
    ESI: 00:00:00:00:00:00:00:00:00:09 
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 8
      ESI Num Macs: 8, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.4      5100       0               all-active
        192.168.1.5      5100       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ec:00 
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.100, Status: Up/Forwarding
      Number of remote PEs connected: 1
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5100       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ed:00
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.101, Status: Up/Forwarding
      Number of remote PEs connected: 1
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5101       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ee:00
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.102, Status: Up/Forwarding
      Number of remote PEs connected: 1
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5102       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ef:00
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.103, Status: Up/Forwarding
      Number of remote PEs connected: 1
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5103       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:f0:00
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.104, Status: Up/Forwarding
      Number of remote PEs connected: 1
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5104       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:f3:00
      State-Bitfield: 0x43
      ESI Refcount: 0
      ESI Num Macs: 0, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.107, Status: Up/Forwarding
    ESI: 05:00:00:ff:dc:00:00:13:f4:00
      State-Bitfield: 0x43
      ESI Refcount: 0
      ESI Num Macs: 0, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.108, Status: Up/Forwarding
    ESI: 05:00:00:ff:dc:00:00:13:f5:00
      State-Bitfield: 0x43
      ESI Refcount: 0
      ESI Num Macs: 0, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.109, Status: Up/Forwarding
    ESI: 05:00:00:ff:dc:00:00:13:f6:00
      State-Bitfield: 0x43
      ESI Refcount: 0
      ESI Num Macs: 0, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.110, Status: Up/Forwarding
```
- SPINE1 has Type1s from SPINE2: 
```
root@SPINE1> show route | match "1:192.168.1.2.*ES"
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
```
- LEAVEs have only ESIs from distibuted anycast GWs 5100-5104, and not for 5105-5110:
```
root@LEAF3> show evpn instance esi-info
Instance: __default_evpn__

Instance: default-switch
  Number of ethernet segments: 6
    ESI: 00:00:00:00:00:00:00:00:00:09
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 10
      ESI Num Macs: 10, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.4      5100       0               all-active
        192.168.1.5      5100       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ec:00
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5100       0               all-active
        192.168.1.2      5100       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ed:00
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5101       0               all-active
        192.168.1.2      5101       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ee:00
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5102       0               all-active
        192.168.1.2      5102       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:ef:00
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5103       0               all-active
        192.168.1.2      5103       0               all-active
    ESI: 05:00:00:ff:dc:00:00:13:f0:00
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.1      5104       0               all-active
        192.168.1.2      5104       0               all-active
```
