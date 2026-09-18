### CORE6
```
root@CORE6> show configuration | display set
set version 24.2R1-S2.5
set system host-name CORE6
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 1
set interfaces ge-0/0/1 unit 0 family inet address 172.16.16.0/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.26.0/31
set interfaces ge-0/0/8 gigether-options 802.3ad ae0
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 unit 0 family inet address 192.168.0.0/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AA9996FED
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AA9996FED
set interfaces irb unit 240 family inet address 10.200.240.252/24 virtual-gateway-address 10.200.240.254
set interfaces lo0 unit 0 family inet address 192.168.1.6/32
set policy-options prefix-list IRB-ANY-PL apply-path "interfaces irb unit <*> family inet address <*>"
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB from prefix-list IRB-ANY-PL
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB then accept
set policy-options policy-statement FABRIC-IMPORT term IMPORT-GLOBAL-RT from community RT-FABRIC
set policy-options policy-statement FABRIC-IMPORT term IMPORT-GLOBAL-RT then accept
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 from community RT-VNI-5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 then accept
set policy-options policy-statement LOAD-BALANCE term PER-FLOW then load-balance per-flow
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options community RT-FABRIC members target:65500:1
set policy-options community RT-VNI-5240 members target:65500:5240
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list all
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 vlan-id 240
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 routing-interface irb.240
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 vxlan vni 5240
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-import FABRIC-IMPORT
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:5240
set routing-options route-distinguisher-id 192.168.1.6
set routing-options router-id 192.168.1.6
set routing-options autonomous-system 65100
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group CORE-SPINE hold-time 9
set protocols bgp group CORE-SPINE export LOOPBACK-to-BGP
set protocols bgp group CORE-SPINE export DIRECT-to-BGP
set protocols bgp group CORE-SPINE peer-as 65200
set protocols bgp group CORE-SPINE multipath
set protocols bgp group CORE-SPINE neighbor 172.16.16.1
set protocols bgp group CORE-SPINE neighbor 172.16.26.1
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.6
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols ospf area 0.0.0.0 interface ae0.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface lo0.0 passive
```
### CORE7
```
root@CORE7> show configuration | display set
set version 24.2R1-S2.5
set system host-name CORE7
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 1
set interfaces ge-0/0/1 unit 0 family inet address 172.16.17.0/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.27.0/31
set interfaces ge-0/0/8 gigether-options 802.3ad ae0
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 unit 0 family inet address 192.168.0.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AA999BB24
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AA999BB24
set interfaces irb unit 240 family inet address 10.200.240.253/24 virtual-gateway-address 10.200.240.254
set interfaces lo0 unit 0 family inet address 192.168.1.7/32
set policy-options prefix-list IRB-ANY-PL apply-path "interfaces irb unit<*> family inet address<*>"
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB from prefix-list IRB-ANY-PL
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB then accept
set policy-options policy-statement FABRIC-IMPORT term IMPORT-GLOBAL-RT from community RT-FABRIC
set policy-options policy-statement FABRIC-IMPORT term IMPORT-GLOBAL-RT then accept
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 from community RT-VNI-5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 then accept
set policy-options policy-statement LOAD-BALANCE term PER-FLOW then load-balance per-flow
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options community RT-FABRIC members target:65500:1
set policy-options community RT-VNI-5240 members target:65500:5240
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list all
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 vlan-id 240
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 routing-interface irb.240
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 vxlan vni 5240
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-import FABRIC-IMPORT
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:5240
set routing-options route-distinguisher-id 192.168.1.7
set routing-options router-id 192.168.1.7
set routing-options autonomous-system 65100
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group CORE-SPINE hold-time 9
set protocols bgp group CORE-SPINE export LOOPBACK-to-BGP
set protocols bgp group CORE-SPINE export DIRECT-to-BGP
set protocols bgp group CORE-SPINE peer-as 65200
set protocols bgp group CORE-SPINE multipath
set protocols bgp group CORE-SPINE neighbor 172.16.17.1
set protocols bgp group CORE-SPINE neighbor 172.16.27.1
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.7
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols ospf area 0.0.0.0 interface ae0.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface lo0.0 passive
```
### SPINE1
```
root@SPINE1> show configuration | display set
set version 24.4R1.9
set groups DRAIN-GLOBAL-GROUP protocols bgp group <*> export DRAIN
set system host-name SPINE1
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system arp aging-timer 5
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
set interfaces ge-0/0/6 unit 0 family inet address 172.16.16.1/31
set interfaces ge-0/0/7 unit 0 family inet address 172.16.17.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AA999C72D
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AA999C72D
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement DRAIN term 1 then as-path-prepend "65200 65200"
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set routing-options autonomous-system 65200
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group CORE-SPINE hold-time 9
set protocols bgp group CORE-SPINE export LOOPBACK-to-BGP
set protocols bgp group CORE-SPINE peer-as 65100
set protocols bgp group CORE-SPINE neighbor 172.16.16.0
set protocols bgp group CORE-SPINE neighbor 172.16.17.0
set protocols bgp group SPINE-LEAF hold-time 9
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF peer-as 65300
set protocols bgp group SPINE-LEAF neighbor 172.16.13.1
set protocols bgp group SPINE-LEAF neighbor 172.16.14.1
set protocols bgp group SPINE-LEAF neighbor 172.16.15.1
set protocols lldp interface all
set protocols lldp-med interface all
```
### SPINE2
```
root@SPINE2> show configuration | display set
set version 24.4R1.9
set groups DRAIN-GLOBAL-GROUP protocols bgp group <*> export DRAIN
set system host-name SPINE2
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system arp aging-timer 5
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
set interfaces ge-0/0/6 unit 0 family inet address 172.16.26.1/31
set interfaces ge-0/0/7 unit 0 family inet address 172.16.27.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AA999CDC6
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AA999CDC6
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement DRAIN term 1 then as-path-prepend "65200 65200"
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set routing-options autonomous-system 65200
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group CORE-SPINE hold-time 9
set protocols bgp group CORE-SPINE export LOOPBACK-to-BGP
set protocols bgp group CORE-SPINE peer-as 65100
set protocols bgp group CORE-SPINE neighbor 172.16.26.0
set protocols bgp group CORE-SPINE neighbor 172.16.27.0
set protocols bgp group SPINE-LEAF hold-time 9
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF peer-as 65300
set protocols bgp group SPINE-LEAF neighbor 172.16.23.1
set protocols bgp group SPINE-LEAF neighbor 172.16.24.1
set protocols bgp group SPINE-LEAF neighbor 172.16.25.1
set protocols lldp interface all
set protocols lldp-med interface all
```

### LEAF3
```
root@LEAF3> show configuration | display set
set version 24.4R1.9
set system host-name LEAF3
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 1
set interfaces ge-0/0/1 unit 0 family inet address 172.16.13.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.23.1/31
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
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 esi 00:00:00:00:00:00:00:00:09:0a
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:34
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members 220
set interfaces ae0 unit 0 family ethernet-switching vlan members 230
set interfaces ae0 unit 0 family ethernet-switching vlan members 240
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AA999E022
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AA999E022
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
set multi-chassis mc-lag consistency-check
set policy-options prefix-list ge-0/0/8_ALL-ADDRESSES apply-path "interfaces ge-0/0/8 unit <*> family inet address <*>"
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs from prefix-list ge-0/0/8_ALL-ADDRESSES
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs then community add LEAF3
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/8_ALL-GWs then accept
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 from community RT-VNI-5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 then accept
set policy-options policy-statement LOAD-BALANCE term PER-FLOW then load-balance per-flow
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then community add LEAF3
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options community RT-VNI-5240 members target:65500:5240
set routing-options router-id 192.168.1.3
set routing-options autonomous-system 65300
set routing-options autonomous-system loops 2
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group SPINE-LEAF hold-time 9
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF export DIRECT-to-BGP
set protocols bgp group SPINE-LEAF peer-as 65200
set protocols bgp group SPINE-LEAF multipath
set protocols bgp group SPINE-LEAF neighbor 172.16.13.0
set protocols bgp group SPINE-LEAF neighbor 172.16.23.0
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.3
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5240 vrf-target export target:65500:5240
set protocols evpn extended-vni-list all
set protocols l2-learning decapsulate-accept-inner-vlan
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.3:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
set vlans VLAN_110 vlan-id 110
set vlans VLAN_111 vlan-id 111
set vlans VLAN_112 vlan-id 112
set vlans VLAN_113 vlan-id 113
set vlans VLAN_114 vlan-id 114
set vlans VLAN_115 vlan-id 115
set vlans VLAN_220 vlan-id 220
set vlans VLAN_220 vxlan vni 5220
set vlans VLAN_230 vlan-id 230
set vlans VLAN_230 vxlan vni 5230
set vlans VLAN_230 vxlan encapsulate-inner-vlan
set vlans VLAN_240 vlan-id 240
set vlans VLAN_240 vxlan vni 5240
```
### LEAF4
```
root@LEAF4> show configuration | display set
set version 24.4R1.9
set system host-name LEAF4
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 esi 00:00:00:00:00:00:00:00:09:0a
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:34
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members 220
set interfaces ae0 unit 0 family ethernet-switching vlan members 230
set interfaces ae0 unit 0 family ethernet-switching vlan members 240
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AA999E867
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AA999E867
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 from community RT-VNI-5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 then accept
set policy-options policy-statement LOAD-BALANCE term PER-FLOW then load-balance per-flow
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then community add LEAF4
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options community RT-VNI-5240 members target:65500:5240
set routing-options router-id 192.168.1.4
set routing-options autonomous-system 65300
set routing-options autonomous-system loops 2
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group SPINE-LEAF hold-time 9
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF peer-as 65200
set protocols bgp group SPINE-LEAF multipath
set protocols bgp group SPINE-LEAF neighbor 172.16.14.0
set protocols bgp group SPINE-LEAF neighbor 172.16.24.0
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.4
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5240 vrf-target export target:65500:5240
set protocols evpn extended-vni-list all
set protocols l2-learning decapsulate-accept-inner-vlan
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.4:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
set vlans VLAN_220 vlan-id 220
set vlans VLAN_220 vxlan vni 5220
set vlans VLAN_230 vlan-id 230
set vlans VLAN_230 vxlan vni 5230
set vlans VLAN_230 vxlan encapsulate-inner-vlan
set vlans VLAN_240 vlan-id 240
set vlans VLAN_240 vxlan vni 5240
```
### LEAF5
```
root@LEAF5> show configuration | display set
set version 24.4R1.9
set system host-name LEAF5
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.15.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.25.1/31
set interfaces ge-0/0/6 unit 0 family ethernet-switching interface-mode trunk
set interfaces ge-0/0/6 unit 0 family ethernet-switching vlan members 220
set interfaces ge-0/0/6 unit 0 family ethernet-switching vlan members 230
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
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AA999E71A
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AA999E71A
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
set multi-chassis mc-lag consistency-check
set policy-options prefix-list ge-0/0/7_ALL-ADDRESSES apply-path "interfaces ge-0/0/7 unit <*> family inet address <*>"
set policy-options policy-statement CORE7-via-SPINE1 term 1 from next-hop 172.16.15.0
set policy-options policy-statement CORE7-via-SPINE1 term 1 from route-filter 192.168.1.7/32 exact
set policy-options policy-statement CORE7-via-SPINE1 term 1 then local-preference 110
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs from prefix-list ge-0/0/7_ALL-ADDRESSES
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs then community add LEAF5
set policy-options policy-statement DIRECT-to-BGP term ge-0/0/7_ALL-GWs then accept
set policy-options policy-statement LOAD-BALANCE term PER-FLOW then load-balance per-flow
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from protocol direct
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 from route-filter 192.168.1.0/24 prefix-length-range /32-/32
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then community add LEAF5
set policy-options policy-statement LOOPBACK-to-BGP term LOOPBACK_0 then accept
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set routing-options router-id 192.168.1.5
set routing-options autonomous-system 65300
set routing-options autonomous-system loops 2
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group SPINE-LEAF hold-time 9
set protocols bgp group SPINE-LEAF advertise-peer-as
set protocols bgp group SPINE-LEAF import CORE7-via-SPINE1
set protocols bgp group SPINE-LEAF export LOOPBACK-to-BGP
set protocols bgp group SPINE-LEAF export DIRECT-to-BGP
set protocols bgp group SPINE-LEAF peer-as 65200
set protocols bgp group SPINE-LEAF multipath
set protocols bgp group SPINE-LEAF neighbor 172.16.15.0
set protocols bgp group SPINE-LEAF neighbor 172.16.25.0
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.5
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn extended-vni-list all
set protocols l2-learning decapsulate-accept-inner-vlan
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.5:65500
set switch-options vrf-target target:65500:1
set switch-options vrf-target auto
set vlans VLAN_130 vlan-id 130
set vlans VLAN_131 vlan-id 131
set vlans VLAN_132 vlan-id 132
set vlans VLAN_133 vlan-id 133
set vlans VLAN_134 vlan-id 134
set vlans VLAN_135 vlan-id 135
set vlans VLAN_220 vlan-id 220
set vlans VLAN_220 vxlan vni 5220
set vlans VLAN_230 vlan-id 230
set vlans VLAN_230 vxlan vni 5230
set vlans VLAN_230 vxlan encapsulate-inner-vlan
```
