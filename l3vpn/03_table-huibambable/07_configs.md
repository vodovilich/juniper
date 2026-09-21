#### PE1
```
root@PE1> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE1
set system root-authentication encrypted-password "$6$PHNV8WTv$LggZwyb8eN8vZ3dhQb7Mkg77YdCxRrva2wEWbxkfuWl0dEBWoyUzTLC5rOTTc/qrUjR1.LjpbLynWupKjwzEN1"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/2 unit 0 family inet address 172.16.12.0/31
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.15.1/31
set interfaces ge-0/0/5 unit 0 family mpls
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 30 vlan-id 30
set interfaces ge-0/0/7 unit 30 family inet address 10.0.31.1/31
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 20 vlan-id 20
set interfaces ge-0/0/8 unit 20 family inet address 10.0.21.1/31
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.10.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AAE6F03BA
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AAE6F03BA
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
set policy-options policy-statement BGP-to-OSPF term 10 from protocol bgp
set policy-options policy-statement BGP-to-OSPF term 10 then accept
set policy-options policy-statement RED_R1_IMPORT term LP_150 then local-preference 150
set routing-instances BLUE-HUEPLET-LIMITED instance-type vrf
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf area 0.0.0.0 interface all
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf export BGP-to-OSPF
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.30
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:30
set routing-instances BLUE-HUEPLET-LIMITED vrf-table-label
set routing-instances GREEN-ZALUPA-INCORPORATED instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP advertise-peer-as
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP peer-as 65020
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP neighbor 10.0.21.0
set routing-instances GREEN-ZALUPA-INCORPORATED interface ge-0/0/8.20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-target target:65500:20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP import RED_R1_IMPORT
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.10.0
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label
set routing-options route-distinguisher-id 192.168.1.1
set routing-options router-id 192.168.1.1
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.1
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key "$9$qPfQCAu01EVwoZjimPB1RhSlWL7"
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols bgp log-updown
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$5T3/puB1ESs2ZDkq5TREcylvX7d"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
#### PE2
```
root@PE2> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE2
set system root-authentication encrypted-password "$6$PHNV8WTv$LggZwyb8eN8vZ3dhQb7Mkg77YdCxRrva2wEWbxkfuWl0dEBWoyUzTLC5rOTTc/qrUjR1.LjpbLynWupKjwzEN1"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.12.1/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/6 unit 0 family inet address 172.16.26.1/31
set interfaces ge-0/0/6 unit 0 family mpls
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 30 vlan-id 30
set interfaces ge-0/0/7 unit 30 family inet address 10.0.32.1/31
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 20 vlan-id 20
set interfaces ge-0/0/8 unit 20 family inet address 10.0.22.1/31
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.11.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AAE74A7AB
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AAE74A7AB
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
set policy-options policy-statement BGP-to-OSPF term 10 from protocol bgp
set policy-options policy-statement BGP-to-OSPF term 10 then accept
set policy-options policy-statement RED_R1_EXPORT term AS-PREPEND then as-path-prepend "65500 65500"
set routing-instances BLUE-HUEPLET-LIMITED instance-type vrf
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf area 0.0.0.0 interface all
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf export BGP-to-OSPF
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.30
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:30
set routing-instances BLUE-HUEPLET-LIMITED vrf-table-label
set routing-instances GREEN-ZALUPA-INCORPORATED instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP advertise-peer-as
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP peer-as 65020
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP neighbor 10.0.22.0
set routing-instances GREEN-ZALUPA-INCORPORATED interface ge-0/0/8.20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-target target:65500:20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP export RED_R1_EXPORT
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.11.0
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label
set routing-options route-distinguisher-id 192.168.1.2
set routing-options router-id 192.168.1.2
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.2
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key "$9$CO2ppuByrKv8xjHfQn6tpW8X7-bgoZ"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$CjhVA01cSleMLUjm5F3CAvM8X7dYga"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
#### PE3
```
root@PE3> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE3
set system root-authentication encrypted-password "$6$PHNV8WTv$LggZwyb8eN8vZ3dhQb7Mkg77YdCxRrva2wEWbxkfuWl0dEBWoyUzTLC5rOTTc/qrUjR1.LjpbLynWupKjwzEN1"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/4 unit 0 family inet address 172.16.34.0/31
set interfaces ge-0/0/4 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.35.1/31
set interfaces ge-0/0/5 unit 0 family mpls
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 30 vlan-id 30
set interfaces ge-0/0/7 unit 30 family inet address 10.0.33.1/31
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 20 vlan-id 20
set interfaces ge-0/0/8 unit 20 family inet address 10.0.23.1/31
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.12.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AAE7728E8
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AAE7728E8
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
set policy-options policy-statement BGP-to-OSPF term 10 from protocol bgp
set policy-options policy-statement BGP-to-OSPF term 10 then accept
set policy-options policy-statement RED-IMPORT term BLOCK-DIRECT from protocol direct
set policy-options policy-statement RED-IMPORT term BLOCK-DIRECT then reject
set policy-options policy-statement RED-IMPORT term ALLOW-BGP from protocol bgp
set policy-options policy-statement RED-IMPORT term ALLOW-BGP then community add RT-RED
set policy-options policy-statement RED-IMPORT term ALLOW-BGP then accept
set policy-options community RT-RED members target:65500:10
set routing-instances BLUE-HUEPLET-LIMITED instance-type vrf
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf area 0.0.0.0 interface all
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf export BGP-to-OSPF
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.30
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:30
set routing-instances BLUE-HUEPLET-LIMITED vrf-table-label
set routing-instances GREEN-ZALUPA-INCORPORATED instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP advertise-peer-as
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP peer-as 65020
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP neighbor 10.0.23.0
set routing-instances GREEN-ZALUPA-INCORPORATED interface ge-0/0/8.20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-target target:65500:20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.12.0
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-export RED-IMPORT
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label
set routing-options route-distinguisher-id 192.168.1.3
set routing-options router-id 192.168.1.3
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.3
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key "$9$4/JZDPfQzn9KM7dsYaJ3n/Ct0Rhy"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/4.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$zMgPF/AOBRESlgoDHmPzFcSrev8Ndw"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/4.0
set protocols mpls interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
set protocols ospf reference-bandwidth 100g
```
#### PE4
```
root@PE4> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE4
set system root-authentication encrypted-password "$6$PHNV8WTv$LggZwyb8eN8vZ3dhQb7Mkg77YdCxRrva2wEWbxkfuWl0dEBWoyUzTLC5rOTTc/qrUjR1.LjpbLynWupKjwzEN1"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/3 unit 0 family inet address 172.16.34.1/31
set interfaces ge-0/0/3 unit 0 family mpls
set interfaces ge-0/0/6 unit 0 family inet address 172.16.46.1/31
set interfaces ge-0/0/6 unit 0 family mpls
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 30 vlan-id 30
set interfaces ge-0/0/7 unit 30 family inet address 10.0.34.1/31
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 20 vlan-id 20
set interfaces ge-0/0/8 unit 20 family inet address 10.0.24.1/31
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.13.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AAE7744E0
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AAE7744E0
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
set policy-options policy-statement BGP-to-OSPF term 10 from protocol bgp
set policy-options policy-statement BGP-to-OSPF term 10 then accept
set routing-instances BLUE-HUEPLET-LIMITED instance-type vrf
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf area 0.0.0.0 interface all
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf export BGP-to-OSPF
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.30
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:30
set routing-instances BLUE-HUEPLET-LIMITED vrf-table-label
set routing-instances GREEN-ZALUPA-INCORPORATED instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP advertise-peer-as
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP peer-as 65020
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP neighbor 10.0.24.0
set routing-instances GREEN-ZALUPA-INCORPORATED interface ge-0/0/8.20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-target target:65500:20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.13.0
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label
set routing-options route-distinguisher-id 192.168.1.4
set routing-options router-id 192.168.1.4
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.4
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key "$9$c3/rlvN-bw2oFnt0IRyrY24aZDqm5"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$gm4ZDq.f5znreL7Vbg4Qz369tBIh"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/3.0
set protocols mpls interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
#### P5
```
root@P5> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name P5
set system root-authentication encrypted-password "$6$PHNV8WTv$LggZwyb8eN8vZ3dhQb7Mkg77YdCxRrva2wEWbxkfuWl0dEBWoyUzTLC5rOTTc/qrUjR1.LjpbLynWupKjwzEN1"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.15.0/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/3 unit 0 family inet address 172.16.35.0/31
set interfaces ge-0/0/3 unit 0 family mpls
set interfaces ge-0/0/6 unit 0 family inet address 172.16.56.0/31
set interfaces ge-0/0/6 unit 0 family mpls
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AAE76EF07
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AAE76EF07
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
set routing-options router-id 192.168.1.5
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.5
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key "$9$KEmW8xsY4oZDCt1EyrMWJZUjH.Tzn"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$sdYoZiH.m5zcyMLN-sYf5QFn9uOI"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/3.0
set protocols mpls interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
set protocols ospf reference-bandwidth 100g
```
#### P6
```
root@P6> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name P6
set system root-authentication encrypted-password "$6$PHNV8WTv$LggZwyb8eN8vZ3dhQb7Mkg77YdCxRrva2wEWbxkfuWl0dEBWoyUzTLC5rOTTc/qrUjR1.LjpbLynWupKjwzEN1"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/2 unit 0 family inet address 172.16.26.0/31
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/4 unit 0 family inet address 172.16.46.0/31
set interfaces ge-0/0/4 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.56.1/31
set interfaces ge-0/0/5 unit 0 family mpls
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AAE770050
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AAE770050
set interfaces lo0 unit 0 family inet address 192.168.1.6/32
set routing-options router-id 192.168.1.6
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.6
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key "$9$WqZXx-g4JZDHp0ESeKLXUDik.fFn9"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/4.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$Nn-w2JZDjkmBIyeW8N-Hk.P5z/Cp"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface ge-0/0/4.0
set protocols mpls interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
