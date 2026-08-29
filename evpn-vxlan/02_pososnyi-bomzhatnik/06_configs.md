#### SPINE1
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
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
set policy-options policy-statement LOAD-BALANCE term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list 5100
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list 5101
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vlan-id 100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 routing-interface irb.100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vxlan vni 5100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vlan-id 101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vxlan vni 5101
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:1
set routing-options route-distinguisher-id 192.168.1.1
set routing-options router-id 192.168.1.1
set routing-options autonomous-system 65001
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 5
set protocols bgp group UNDERLAY neighbor 172.16.13.1 peer-as 65003
set protocols bgp group UNDERLAY neighbor 172.16.14.1 peer-as 65004
set protocols bgp group UNDERLAY neighbor 172.16.15.1 peer-as 65005
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.1
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp log-updown
```
#### SPINE2
```
root@SPINE2> show configuration | display set
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
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
set policy-options policy-statement LOAD-BALANCE term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list 5100
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list 5101
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vlan-id 101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vxlan vni 5101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_100 vlan-id 100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_100 routing-interface irb.100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_100 vxlan vni 5100
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:1
set routing-options route-distinguisher-id 192.168.1.2
set routing-options router-id 192.168.1.2
set routing-options autonomous-system 65002
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 5
set protocols bgp group UNDERLAY neighbor 172.16.23.1 peer-as 65003
set protocols bgp group UNDERLAY neighbor 172.16.24.1 peer-as 65004
set protocols bgp group UNDERLAY neighbor 172.16.25.1 peer-as 65005
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.2
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp log-updown
```
#### LEAF3
```
root@LEAF3> show configuration | display set
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
set interfaces ge-0/0/6 unit 0 family ethernet-switching vlan members 100-101
set interfaces ge-0/0/7 unit 0 family ethernet-switching interface-mode trunk
set interfaces ge-0/0/7 unit 0 family ethernet-switching vlan members 100-101
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6A86B78175
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6A86B78175
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from protocol bgp
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from community FABRIC-RT
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT then accept
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 from community RT-VNI-5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 then accept
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 from community RT-VNI-5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 then accept
set policy-options policy-statement LOAD-BALANCE term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community FABRIC-RT members target:65500:1
set policy-options community RT-VNI-5100 members target:65500:5100
set policy-options community RT-VNI-5101 members target:65500:5101
set routing-options router-id 192.168.1.3
set routing-options autonomous-system 65003
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 5
set protocols bgp group UNDERLAY neighbor 172.16.13.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.23.0 peer-as 65002
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.3
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp log-updown
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set protocols evpn extended-vni-list 5100
set protocols evpn extended-vni-list 5101
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.3:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set vlans VLAN_100 vlan-id 100
set vlans VLAN_100 vxlan vni 5100
set vlans VLAN_101 vlan-id 101
set vlans VLAN_101 vxlan vni 5101
```
#### LEAF4
```
root@LEAF4> show configuration | display set
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
set interfaces ge-0/0/8 unit 0 family ethernet-switching vlan members 100-101
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 esi 00:00:00:00:00:00:00:00:00:11
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:11
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members 100-101
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6A86B78258
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6A86B78258
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from protocol bgp
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from community FABRIC-RT
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT then accept
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 from community RT-VNI-5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 then accept
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 from community RT-VNI-5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 then accept
set policy-options policy-statement LOAD-BALANCE term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community FABRIC-RT members target:65500:1
set policy-options community RT-VNI-5100 members target:65500:5100
set policy-options community RT-VNI-5101 members target:65500:5101
set routing-options router-id 192.168.1.4
set routing-options autonomous-system 65004
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 5
set protocols bgp group UNDERLAY neighbor 172.16.14.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.24.0 peer-as 65002
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.4
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp log-updown
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set protocols evpn extended-vni-list 5100
set protocols evpn extended-vni-list 5101
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.4:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set vlans VLAN_100 vlan-id 100
set vlans VLAN_100 vxlan vni 5100
set vlans VLAN_101 vlan-id 101
set vlans VLAN_101 vxlan vni 5101
```
#### LEAF5
```
root@LEAF5> show configuration | display set
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
set interfaces ae0 esi 00:00:00:00:00:00:00:00:00:11
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:11
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members 100-101
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6A86B783A5
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6A86B783A5
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
set multi-chassis mc-lag consistency-check
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from protocol bgp
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT from community FABRIC-RT
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-RT then accept
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 from community RT-VNI-5100
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5100 then accept
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 from community RT-VNI-5101
set policy-options policy-statement FABRIC-IMPORT term ACCEPT-VNI-5101 then accept
set policy-options policy-statement LOAD-BALANCE term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community FABRIC-RT members target:65500:1
set policy-options community RT-VNI-5100 members target:65500:5100
set policy-options community RT-VNI-5101 members target:65500:5101
set routing-options router-id 192.168.1.5
set routing-options autonomous-system 65005
set routing-options forwarding-table export LOAD-BALANCE
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 5
set protocols bgp group UNDERLAY neighbor 172.16.15.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.25.0 peer-as 65002
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.5
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY bfd-liveness-detection minimum-interval 2000
set protocols bgp group OVERLAY bfd-liveness-detection multiplier 3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp log-updown
set protocols evpn encapsulation vxlan
set protocols evpn multicast-mode ingress-replication
set protocols evpn vni-options vni 5100 vrf-target target:65500:5100
set protocols evpn vni-options vni 5101 vrf-target target:65500:5101
set protocols evpn extended-vni-list 5100
set protocols evpn extended-vni-list 5101
set protocols lldp interface all
set protocols lldp-med interface all
set switch-options vtep-source-interface lo0.0
set switch-options route-distinguisher 192.168.1.5:65500
set switch-options vrf-import FABRIC-IMPORT
set switch-options vrf-target target:65500:1
set vlans VLAN_100 vlan-id 100
set vlans VLAN_100 vxlan vni 5100
set vlans VLAN_101 vlan-id 101
set vlans VLAN_101 vxlan vni 5101
```
