## PE1
```
set version 24.2R1-S2.5
set system host-name PE1
set system root-authentication encrypted-password "$6$CuDeQY0V$ny9JCYCCoQutI0YPkBJNPqTqnftP1.M2HgAevPo3b0MaYVH5MT.bvLIRwP1OZGzPfdDzJ55DXBcSDoyJdmSPb0"
set chassis fpc 0 pic 0 tunnel-services
set interfaces ge-0/0/0 unit 0 family inet address 172.16.11.1/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 vlan-tagging
set interfaces ge-0/0/1 encapsulation vlan-vpls
set interfaces ge-0/0/1 unit 601 description Cust1_Site1
set interfaces ge-0/0/1 unit 601 encapsulation vlan-vpls
set interfaces ge-0/0/1 unit 601 vlan-id 601
set interfaces ge-0/0/2 vlan-tagging
set interfaces ge-0/0/2 encapsulation vlan-vpls
set interfaces ge-0/0/2 unit 601 description Cust1_Site3
set interfaces ge-0/0/2 unit 601 encapsulation vlan-vpls
set interfaces ge-0/0/2 unit 601 vlan-id 601
set interfaces lo0 unit 0 family inet address 1.1.1.1/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0001.00
set interfaces lo0 unit 0 family mpls
set routing-instances Customer1 instance-type vpls
set routing-instances Customer1 protocols vpls neighbor 2.2.2.2
set routing-instances Customer1 protocols vpls vpls-id 100
set routing-instances Customer1 interface ge-0/0/1.601
set routing-instances Customer1 interface ge-0/0/2.601
set routing-instances Customer1 route-distinguisher 1.1.1.1:1
set routing-instances Customer1 vrf-target target:65530:1
set routing-options router-id 1.1.1.1
set routing-options autonomous-system 65530
set protocols isis interface ge-0/0/0.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface lo0.0
set protocols mpls interface lo0.0
set protocols mpls interface ge-0/0/0.0

```
## P1
```
set version 24.2R1-S2.5
set system host-name P1
set system root-authentication encrypted-password "$6$sx5A5b5O$hfT3OsI1zhmbdIwOZKzBbcj6GMPzOTimZnaY1cmQxHl2acK4qcE0iXxaa1PSZbGXHT64.WWHMvTwbc0PDvsrd0"
set interfaces ge-0/0/0 unit 0 family inet address 172.16.11.11/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 172.16.13.11/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces lo0 unit 0 family inet address 11.11.11.11/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0011.00
set interfaces lo0 unit 0 family mpls
set routing-options router-id 11.11.11.11
set routing-options autonomous-system 65530
set protocols bgp group INTERNAL type internal
set protocols bgp group INTERNAL local-address 11.11.11.11
set protocols bgp group INTERNAL family inet unicast
set protocols bgp group INTERNAL family l2vpn signaling
set protocols bgp group INTERNAL cluster 11.11.11.11
set protocols bgp group INTERNAL neighbor 1.1.1.1
set protocols bgp group INTERNAL neighbor 33.33.33.33
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/1.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface lo0.0
```
## Core
```
set version 24.2R1-S2.5
set system host-name Core
set system root-authentication encrypted-password "$6$p.tenhQP$CO2Yp31K4DlkbUK7QYVNHsAdDpZHhDQwbLBxMxcrVQ6Ta7gbnrNjc6iDSROTHqwF7qH1cWF7Cg0HT.klsGR/J1"
set interfaces ge-0/0/0 unit 0 family inet address 172.16.13.33/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 172.16.23.33/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces lo0 unit 0 family inet address 33.33.33.33/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0033.00
set interfaces lo0 unit 0 family mpls
set routing-options router-id 33.33.33.33
set routing-options autonomous-system 65530
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INTERNAL type internal
set protocols bgp group INTERNAL local-address 33.33.33.33
set protocols bgp group INTERNAL family inet unicast
set protocols bgp group INTERNAL family l2vpn signaling
set protocols bgp group INTERNAL cluster 33.33.33.33
set protocols bgp group INTERNAL neighbor 11.11.11.11
set protocols bgp group INTERNAL neighbor 22.22.22.22
set protocols isis interface all
set protocols ldp interface all
set protocols mpls interface all
```
## P2
```
set version 24.2R1-S2.5
set system host-name P2
set system root-authentication encrypted-password "$6$2s2uOrQ/$F3uQYV.hZbtN3emH8qXzx48.4ktjWrhqKu9AZtTOznz2LdmpF7Wk1Hn3AaP5pTRNaM9Qj57k7Dy4XjInDwhaG1"
set interfaces ge-0/0/0 unit 0 family inet address 172.16.22.22/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 172.16.23.22/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces lo0 unit 0 family inet address 22.22.22.22/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0022.00
set interfaces lo0 unit 0 family mpls
set routing-options router-id 22.22.22.22
set routing-options autonomous-system 65530
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INTERNAL type internal
set protocols bgp group INTERNAL local-address 22.22.22.22
set protocols bgp group INTERNAL family inet unicast
set protocols bgp group INTERNAL family l2vpn signaling
set protocols bgp group INTERNAL cluster 22.22.22.22
set protocols bgp group INTERNAL neighbor 33.33.33.33
set protocols bgp group INTERNAL neighbor 2.2.2.2
set protocols isis interface all
set protocols ldp interface all
set protocols mpls interface all
```
## PE2
```
set version 24.2R1-S2.5
set system host-name PE2
set system root-authentication encrypted-password "$6$q0PGXBnV$AWIUtAngE2PFpIkYW6wCRgQkH8QWWJXmj23sglpCA8ayP2BGwh5W5fYizciTBMgkQ2T02IonHGDCnNWFYF009/"
set chassis fpc 0 pic 0 tunnel-services
set interfaces ge-0/0/0 unit 0 family inet address 172.16.22.2/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 vlan-tagging
set interfaces ge-0/0/1 encapsulation vlan-vpls
set interfaces ge-0/0/1 unit 601 description Customer1_Site2
set interfaces ge-0/0/1 unit 601 encapsulation vlan-vpls
set interfaces ge-0/0/1 unit 601 vlan-id 601
set interfaces ge-0/0/2 vlan-tagging
set interfaces ge-0/0/2 encapsulation vlan-vpls
set interfaces ge-0/0/2 unit 601 description Cust1_Site4
set interfaces ge-0/0/2 unit 601 encapsulation vlan-vpls
set interfaces ge-0/0/2 unit 601 vlan-id 601
set interfaces lo0 unit 0 family inet address 2.2.2.2/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0002.00
set interfaces lo0 unit 0 family mpls
set routing-instances Customer1 instance-type vpls
set routing-instances Customer1 protocols vpls neighbor 1.1.1.1
set routing-instances Customer1 protocols vpls vpls-id 100
set routing-instances Customer1 interface ge-0/0/1.601
set routing-instances Customer1 interface ge-0/0/2.601
set routing-instances Customer1 route-distinguisher 2.2.2.2:1
set routing-instances Customer1 vrf-target target:65530:1
set routing-options router-id 2.2.2.2
set routing-options autonomous-system 65530
set protocols isis interface ge-0/0/0.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface lo0.0
```
