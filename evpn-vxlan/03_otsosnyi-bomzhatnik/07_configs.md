### SPINE1
```
root@SPINE1> show configuration | display set
set version 24.2R1-S2.5
set system host-name SPINE1
set system root-authentication encrypted-password "$6$RWI4wGzg$oBkDpx9bQ2IZw/0o.j3Hlk7tAVl99A65dhjuM6vJ7kXqMrjOO3gIFjNAO1JaRxgwTMrKd5YeoZcjIqKCB/Yv41"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/3 unit 0 family inet address 172.16.13.0/31
set interfaces ge-0/0/4 unit 0 family inet address 172.16.14.0/31
set interfaces ge-0/0/5 unit 0 family inet address 172.16.15.0/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6A86B776ED
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6A86B776ED
set interfaces irb unit 100 family inet address 10.200.100.252/24 virtual-gateway-address 10.200.100.254
set interfaces irb unit 101 family inet address 10.200.101.252/24 virtual-gateway-address 10.200.101.254
set interfaces irb unit 102 family inet address 10.200.102.252/24 virtual-gateway-address 10.200.102.254
set interfaces irb unit 103 family inet address 10.200.103.252/24 virtual-gateway-address 10.200.103.254
set interfaces irb unit 104 family inet address 10.200.104.252/24 virtual-gateway-address 10.200.104.254
set interfaces irb unit 105 family inet address 10.200.105.254/24
set interfaces irb unit 106 family inet address 10.200.106.254/24
set interfaces irb unit 109 family inet address 10.200.109.254/24
set interfaces irb unit 109 mac aa:aa:aa:aa:aa:09
set interfaces irb unit 110 family inet address 10.200.110.254/24
set interfaces irb unit 110 mac aa:aa:aa:aa:aa:10
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
set policy-options policy-statement LOAD-BALANCE-POLICY term LOAD-BALANCE then load-balance per-flow
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list all
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5105 vrf-target export target:65500:5105
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5106 vrf-target export target:65500:5106
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5109 vrf-target target:65500:5109
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5110 vrf-target target:65500:5110
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vlan-id 100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 routing-interface irb.100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vxlan vni 5100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vlan-id 101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vxlan vni 5101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 vlan-id 102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 routing-interface irb.102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 vxlan vni 5102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 vlan-id 103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 routing-interface irb.103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 vxlan vni 5103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 vlan-id 104
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 routing-interface irb.104
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 vxlan vni 5104
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-105 vlan-id 105
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-105 routing-interface irb.105
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-105 vxlan vni 5105
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-106 vlan-id 106
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-106 routing-interface irb.106
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-106 vxlan vni 5106
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-109 vlan-id 109
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-109 routing-interface irb.109
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-109 vxlan vni 5109
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-110 vlan-id 110
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-110 routing-interface irb.110
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-110 vxlan vni 5110
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:1
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target auto
set routing-options route-distinguisher-id 192.168.1.1
set routing-options router-id 192.168.1.1
set routing-options autonomous-system 65500
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.1
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY cluster 192.168.1.1
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 authentication md5 1 key "$9$fz6CuOIRcr8XDHqmQz6/Cp1EleMx-b"
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 authentication md5 1 key "$9$O2nlRSlM8x7dwaZ6CtuIRSylvXNsY4Gjk"
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 authentication md5 1 key "$9$OqWfRSlM8x7dwaZ6CtuIRSylvXNsY4Gjk"
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface irb.105 passive
set protocols ospf area 0.0.0.0 interface irb.106 passive
```
### SPINE2
```
root@SPINE2> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name SPINE2
set system root-authentication encrypted-password "$6$RWI4wGzg$oBkDpx9bQ2IZw/0o.j3Hlk7tAVl99A65dhjuM6vJ7kXqMrjOO3gIFjNAO1JaRxgwTMrKd5YeoZcjIqKCB/Yv41"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/3 unit 0 family inet address 172.16.23.0/31
set interfaces ge-0/0/4 unit 0 family inet address 172.16.24.0/31
set interfaces ge-0/0/5 unit 0 family inet address 172.16.25.0/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6A86B778D9
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6A86B778D9
set interfaces irb unit 100 family inet address 10.200.100.253/24 virtual-gateway-address 10.200.100.254
set interfaces irb unit 101 family inet address 10.200.101.253/24 virtual-gateway-address 10.200.101.254
set interfaces irb unit 102 family inet address 10.200.102.253/24 virtual-gateway-address 10.200.102.254
set interfaces irb unit 103 family inet address 10.200.103.253/24 virtual-gateway-address 10.200.103.254
set interfaces irb unit 104 family inet address 10.200.104.253/24 virtual-gateway-address 10.200.104.254
set interfaces irb unit 107 family inet address 10.200.107.254/24
set interfaces irb unit 108 family inet address 10.200.108.254/24
set interfaces irb unit 109 family inet address 10.200.109.254/24
set interfaces irb unit 109 mac aa:aa:aa:aa:aa:09
set interfaces irb unit 110 family inet address 10.200.110.254/24
set interfaces irb unit 110 mac aa:aa:aa:aa:aa:10
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
set policy-options policy-statement LOAD-BALANCE-POLICY term LOAD-BALANCE then load-balance per-flow
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list all
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5107 vrf-target export target:65500:5107
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5108 vrf-target export target:65500:5108
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5109 vrf-target target:65500:5109
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5110 vrf-target target:65500:5110
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vlan-id 100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 routing-interface irb.100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vxlan vni 5100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vlan-id 101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vxlan vni 5101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 vlan-id 102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 routing-interface irb.102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-102 vxlan vni 5102
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 vlan-id 103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 routing-interface irb.103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-103 vxlan vni 5103
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 vlan-id 104
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 routing-interface irb.104
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-104 vxlan vni 5104
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-107 vlan-id 107
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-107 routing-interface irb.107
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-107 vxlan vni 5107
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-108 vlan-id 108
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-108 routing-interface irb.108
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-108 vxlan vni 5108
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-109 vlan-id 109
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-109 routing-interface irb.109
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-109 vxlan vni 5109
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-110 vlan-id 110
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-110 routing-interface irb.110
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-110 vxlan vni 5110
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:1
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target auto
set routing-options route-distinguisher-id 192.168.1.2
set routing-options router-id 192.168.1.2
set routing-options autonomous-system 65500
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.2
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY cluster 192.168.1.2
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 authentication md5 1 key "$9$gPJDHmfQzn9O1NVwYaJDjH.TFCAuIhy"
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 authentication md5 1 key "$9$QXC9nCpBIhcrKxNH.P53nCApOESvML-bY"
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 authentication md5 1 key "$9$l3kMXNbsg4JU.P1EcyvMXxNV2oDjkfQ3"
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface irb.107 passive
set protocols ospf area 0.0.0.0 interface irb.108 passive 
```
### LEAF3
```
root@LEAF3> show configuration | display set | no-more
set version 24.4R1.9
set system host-name LEAF3
set system root-authentication encrypted-password "$6$RWI4wGzg$oBkDpx9bQ2IZw/0o.j3Hlk7tAVl99A65dhjuM6vJ7kXqMrjOO3gIFjNAO1JaRxgwTMrKd5YeoZcjIqKCB/Yv41"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.13.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.23.1/31
set interfaces ge-0/0/6 unit 0 family ethernet-switching interface-mode trunk
set interfaces ge-0/0/6 unit 0 family ethernet-switching vlan members 100-110
set interfaces ge-0/0/7 unit 0 family ethernet-switching interface-mode trunk
set interfaces ge-0/0/7 unit 0 family ethernet-switching vlan members 100-110
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6A86B78175
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6A86B78175
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from community FABRIC-RT
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT then accept
set policy-options policy-statement IMPORT-5105-to-5110-RTs term IMPORT-5105 from community 5105-RT
set policy-options policy-statement IMPORT-5105-to-5110-RTs term IMPORT-5105 then accept
set policy-options policy-statement IMPORT-5105-to-5110-RTs term IMPORT-5106 from community 5106-RT
set policy-options policy-statement IMPORT-5105-to-5110-RTs term IMPORT-5106 then accept
set policy-options policy-statement IMPORT-5105-to-5110-RTs term IMPORT-5107 from community 5107-RT
set policy-options policy-statement IMPORT-5105-to-5110-RTs term IMPORT-5107 then accept
set policy-options policy-statement LOAD-BALANCE-POLICY term LOAD-BALANCE then load-balance per-flow
set policy-options community 5105-RT members target:65500:5105
set policy-options community 5106-RT members target:65500:5106
set policy-options community 5107-RT members target:65500:5107
set policy-options community FABRIC-RT members target:65500:1
set routing-options router-id 192.168.1.3
set routing-options autonomous-system 65500
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.3
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5105 vrf-target export target:65500:5105
set protocols evpn vni-options vni 5106 vrf-target export target:65500:5106
set protocols evpn vni-options vni 5107 vrf-target export target:65500:5107
set protocols evpn vni-options vni 5108 vrf-target export target:65500:5108
set protocols evpn vni-options vni 5109 vrf-target export target:65500:5109
set protocols evpn vni-options vni 5110 vrf-target export target:65500:5110
set protocols evpn extended-vni-list all
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 authentication md5 1 key "$9$tMhVORclKW8x-24zn/C0OREcrMLdVsoZD"
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 authentication md5 1 key "$9$kPQ39Au01EevaGDimPQz3/pOhcrML7"
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.3:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-import IMPORT-5105-to-5110-RTs
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
set vlans VLAN_100 vlan-id 100
set vlans VLAN_100 vxlan vni 5100
set vlans VLAN_101 vlan-id 101
set vlans VLAN_101 vxlan vni 5101
set vlans VLAN_102 vlan-id 102
set vlans VLAN_102 vxlan vni 5102
set vlans VLAN_103 vlan-id 103
set vlans VLAN_103 vxlan vni 5103
set vlans VLAN_104 vlan-id 104
set vlans VLAN_104 vxlan vni 5104
set vlans VLAN_105 vlan-id 105
set vlans VLAN_105 vxlan vni 5105
set vlans VLAN_106 vlan-id 106
set vlans VLAN_106 vxlan vni 5106
set vlans VLAN_107 vlan-id 107
set vlans VLAN_107 vxlan vni 5107
set vlans VLAN_108 vlan-id 108
set vlans VLAN_108 vxlan vni 5108
set vlans VLAN_109 vlan-id 109
set vlans VLAN_109 vxlan vni 5109
set vlans VLAN_110 vlan-id 110
set vlans VLAN_110 vxlan vni 5110
```
### LEAF4
```
root@LEAF4> show configuration | display set | no-more
set version 24.4R1.9
set system host-name LEAF4
set system root-authentication encrypted-password "$6$RWI4wGzg$oBkDpx9bQ2IZw/0o.j3Hlk7tAVl99A65dhjuM6vJ7kXqMrjOO3gIFjNAO1JaRxgwTMrKd5YeoZcjIqKCB/Yv41"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 1
set interfaces ge-0/0/1 unit 0 family inet address 172.16.14.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.24.1/31
set interfaces ge-0/0/8 unit 0 family ethernet-switching interface-mode trunk
set interfaces ge-0/0/8 unit 0 family ethernet-switching vlan members 100-110
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 esi 00:00:00:00:00:00:00:00:00:09
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:45
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members 100-110
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6A86B78258
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6A86B78258
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from community FABRIC-RT
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT then accept
set policy-options policy-statement LOAD-BALANCE-POLICY term LOAD-BALANCE then load-balance per-flow
set policy-options community FABRIC-RT members target:65500:1
set routing-options router-id 192.168.1.4
set routing-options autonomous-system 65500
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.4
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5105 vrf-target export target:65500:5105
set protocols evpn vni-options vni 5106 vrf-target export target:65500:5106
set protocols evpn vni-options vni 5107 vrf-target export target:65500:5107
set protocols evpn vni-options vni 5108 vrf-target export target:65500:5108
set protocols evpn vni-options vni 5109 vrf-target export target:65500:5109
set protocols evpn vni-options vni 5110 vrf-target export target:65500:5110
set protocols evpn extended-vni-list all
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 authentication md5 1 key "$9$niX2CuBEcrlv8dbm5QF9Cu0BRyeLXNw2o"
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 authentication md5 1 key "$9$AFcx0IhreMWXNYgQ369u0IRhyv8-dw4JU"
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.4:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
set vlans VLAN_100 vlan-id 100
set vlans VLAN_100 vxlan vni 5100
set vlans VLAN_101 vlan-id 101
set vlans VLAN_101 vxlan vni 5101
set vlans VLAN_102 vlan-id 102
set vlans VLAN_102 vxlan vni 5102
set vlans VLAN_103 vlan-id 103
set vlans VLAN_103 vxlan vni 5103
set vlans VLAN_104 vlan-id 104
set vlans VLAN_104 vxlan vni 5104
set vlans VLAN_105 vlan-id 105
set vlans VLAN_105 vxlan vni 5105
set vlans VLAN_106 vlan-id 106
set vlans VLAN_106 vxlan vni 5106
set vlans VLAN_107 vlan-id 107
set vlans VLAN_107 vxlan vni 5107
set vlans VLAN_108 vlan-id 108
set vlans VLAN_108 vxlan vni 5108
set vlans VLAN_109 vlan-id 109
set vlans VLAN_109 vxlan vni 5109
set vlans VLAN_110 vlan-id 110
set vlans VLAN_110 vxlan vni 5110
```
### LEAF5
```
root@LEAF5> show configuration | display set | no-more
set version 24.4R1.9
set system host-name LEAF5
set system root-authentication encrypted-password "$6$RWI4wGzg$oBkDpx9bQ2IZw/0o.j3Hlk7tAVl99A65dhjuM6vJ7kXqMrjOO3gIFjNAO1JaRxgwTMrKd5YeoZcjIqKCB/Yv41"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 1
set interfaces ge-0/0/1 unit 0 family inet address 172.16.15.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.25.1/31
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 esi 00:00:00:00:00:00:00:00:00:09
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:45
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members 100-110
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6A86B783A5
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6A86B783A5
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from community FABRIC-RT
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT then accept
set policy-options policy-statement LOAD-BALANCE-POLICY term LOAD-BALANCE then load-balance per-flow
set policy-options community FABRIC-RT members target:65500:1
set routing-options router-id 192.168.1.5
set routing-options autonomous-system 65500
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.5
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5105 vrf-target export target:65500:5105
set protocols evpn vni-options vni 5106 vrf-target export target:65500:5106
set protocols evpn vni-options vni 5107 vrf-target export target:65500:5107
set protocols evpn vni-options vni 5108 vrf-target export target:65500:5108
set protocols evpn vni-options vni 5109 vrf-target export target:65500:5109
set protocols evpn vni-options vni 5110 vrf-target export target:65500:5110
set protocols evpn extended-vni-list all
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 authentication md5 1 key "$9$o-GiqfTF3/A1RdwYgZGiHqPzntpOESl"
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 authentication md5 1 key "$9$HmTF/CpuBRlKoZUj.mTQF6t0Ehyv8x"
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 bfd-liveness-detection minimum-interval 2000
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 bfd-liveness-detection multiplier 5
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.5:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
set vlans VLAN_100 vlan-id 100
set vlans VLAN_100 vxlan vni 5100
set vlans VLAN_101 vlan-id 101
set vlans VLAN_101 vxlan vni 5101
set vlans VLAN_102 vlan-id 102
set vlans VLAN_102 vxlan vni 5102
set vlans VLAN_103 vlan-id 103
set vlans VLAN_103 vxlan vni 5103
set vlans VLAN_104 vlan-id 104
set vlans VLAN_104 vxlan vni 5104
set vlans VLAN_105 vlan-id 105
set vlans VLAN_105 vxlan vni 5105
set vlans VLAN_106 vlan-id 106
set vlans VLAN_106 vxlan vni 5106
set vlans VLAN_107 vlan-id 107
set vlans VLAN_107 vxlan vni 5107
set vlans VLAN_108 vlan-id 108
set vlans VLAN_108 vxlan vni 5108
set vlans VLAN_109 vlan-id 109
set vlans VLAN_109 vxlan vni 5109
set vlans VLAN_110 vlan-id 110
set vlans VLAN_110 vxlan vni 5110
```
