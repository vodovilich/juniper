## PE1
```
root@PE1> show configuration | display set
set version 24.2R1-S2.5
set system host-name PE1
set system root-authentication encrypted-password "$6$HrFIAr5K$g.Ygzr0/SU4pZc5IBaNaFdW5.WMu/YC6eFn/51canj8o4uS6wJfREAsOr0LPmMFy5yweMMqhna3rqNDuKajsE1"
set interfaces ge-0/0/0 unit 0 family inet address 172.16.11.1/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 192.168.11.1/24
set interfaces lo0 unit 0 family inet address 1.1.1.1/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0001.00
set interfaces lo0 unit 0 family mpls
set routing-instances Customer1-VRF instance-type vrf
set routing-instances Customer1-VRF protocols bgp group EXT type external
set routing-instances Customer1-VRF protocols bgp group EXT advertise-peer-as
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.11.2 description CE1-R1
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.11.2 local-address 192.168.11.1
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.11.2 family inet unicast
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.11.2 peer-as 65601
set routing-instances Customer1-VRF interface ge-0/0/1.0
set routing-instances Customer1-VRF route-distinguisher 1.1.1.1:1
set routing-instances Customer1-VRF vrf-target target:65530:1
set routing-options router-id 1.1.1.1
set routing-options autonomous-system 65530
set protocols bgp group INT type internal
set protocols bgp group INT local-address 1.1.1.1
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT neighbor 11.11.11.11
set protocols isis interface ge-0/0/0.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
```
## P1
```
root@P1> show configuration | display set
set version 24.2R1-S2.5
set system host-name P1
set system root-authentication encrypted-password "$6$8nhONTQn$ACQQOuaHIPTyp3Kbq0jA1s4a3Co                           Q8Xm0HfdLXsBevlEe1pCp9PXiAPSU3gYCGLXusZnyUhD2IJrqQwYsGmQ8e/"
set interfaces ge-0/0/0 unit 0 family inet address 172.16.11.11/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 172.16.12.11/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces lo0 unit 0 family inet address 11.11.11.11/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0011.00
set interfaces lo0 unit 0 family mpls
set routing-options router-id 11.11.11.11
set routing-options autonomous-system 65530
set protocols bgp group INT type internal
set protocols bgp group INT local-address 11.11.11.11
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT cluster 11.11.11.11
set protocols bgp group INT neighbor 1.1.1.1
set protocols bgp group INT neighbor 22.22.22.22
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/1.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/1.0
```
## P2
```
root@P2> show configuration | display set
set version 24.2R1-S2.5
set system host-name P2
set system root-authentication encrypted-password "$6$55DNh8Vk$/AuZ0FYuP99fR6OGONeHhtR.A8dIZUm120ogPOvQfBN5lYz0NGPyow.BXKki9dEHD/TETLfq6CRReTg35Ufn91"
set interfaces ge-0/0/0 unit 0 family inet address 172.16.12.22/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 172.16.22.22/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces lo0 unit 0 family inet address 22.22.22.22/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0022.00
set interfaces lo0 unit 0 family mpls
set routing-options router-id 22.22.22.22
set routing-options autonomous-system 65530
set protocols bgp group INT type internal
set protocols bgp group INT local-address 22.22.22.22
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT cluster 22.22.22.22
set protocols bgp group INT neighbor 11.11.11.11
set protocols bgp group INT neighbor 2.2.2.2
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/1.0
set protocols isis interface lo0.0
set protocols ldp interface all
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/1.0
```

## PE2
```
root@PE2> show configuration | display set
set version 24.2R1-S2.5
set system host-name PE2
set system root-authentication encrypted-password "$6$GEfDmtcn$ZZB7huUt.WJWIIVXHwMPPuqDsREsVwgMHfp8qAjpkI8o1DfVauv1ar8kbNMnrKtlcVWlGBSVjS5EkIJ6Wr.lW."
set interfaces ge-0/0/0 unit 0 family inet address 172.16.22.2/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 192.168.22.1/24
set interfaces lo0 unit 0 family inet address 2.2.2.2/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0002.00
set interfaces lo0 unit 0 family mpls
set routing-instances Customer1-VRF instance-type vrf
set routing-instances Customer1-VRF protocols bgp group EXT type external
set routing-instances Customer1-VRF protocols bgp group EXT advertise-peer-as
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.22.2 description CE1-R2
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.22.2 local-address 192.168.22.1
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.22.2 family inet unicast
set routing-instances Customer1-VRF protocols bgp group EXT neighbor 192.168.22.2 peer-as 65601
set routing-instances Customer1-VRF interface ge-0/0/1.0
set routing-instances Customer1-VRF route-distinguisher 2.2.2.2:1
set routing-instances Customer1-VRF vrf-target target:65530:1
set routing-options router-id 2.2.2.2
set routing-options autonomous-system 65530
set protocols bgp group INT type internal
set protocols bgp group INT local-address 2.2.2.2
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT neighbor 22.22.22.22
set protocols isis interface ge-0/0/0.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
```
