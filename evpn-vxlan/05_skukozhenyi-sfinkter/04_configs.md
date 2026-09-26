### PE1
```
root@PE1> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE1
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces ge-0/0/6 flexible-vlan-tagging
set interfaces ge-0/0/6 encapsulation flexible-ethernet-services
set interfaces ge-0/0/6 unit 110 encapsulation vlan-bridge
set interfaces ge-0/0/6 unit 110 vlan-id 110
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 120 encapsulation vlan-bridge
set interfaces ge-0/0/7 unit 120 vlan-id 120
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 130 encapsulation vlan-bridge
set interfaces ge-0/0/8 unit 130 vlan-id 130
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 140 encapsulation vlan-bridge
set interfaces ge-0/0/9 unit 140 vlan-id 140
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AB6B6D287
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AB6B6D287
set interfaces irb unit 120 family inet address 10.120.0.254/24
set interfaces irb unit 130 family inet address 10.130.12.254/24
set interfaces irb unit 140 family inet address 10.140.123.251/24 virtual-gateway-address 10.140.123.254
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
set routing-instances BLUE-HUEPLET-LIMITED instance-type evpn
set routing-instances BLUE-HUEPLET-LIMITED protocols evpn
set routing-instances BLUE-HUEPLET-LIMITED vlan-id 120
set routing-instances BLUE-HUEPLET-LIMITED routing-interface irb.120
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.120
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:120
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN instance-type evpn
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN protocols evpn
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN vlan-id 130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN routing-interface irb.130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN interface ge-0/0/8.130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN vrf-target target:65500:130
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface irb.130
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-target target:65500:330
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-table-label
set routing-instances PURPLE-PILLS-EVPN instance-type evpn
set routing-instances PURPLE-PILLS-EVPN protocols evpn
set routing-instances PURPLE-PILLS-EVPN vlan-id 110
set routing-instances PURPLE-PILLS-EVPN interface ge-0/0/6.110
set routing-instances PURPLE-PILLS-EVPN vrf-target target:65500:110
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN instance-type evpn
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN protocols evpn default-gateway do-not-advertise
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN vlan-id 140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN routing-interface irb.140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN interface ge-0/0/9.140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN vrf-target target:65500:140
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN interface irb.140
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-target target:65500:340
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-table-label
set routing-options route-distinguisher-id 192.168.1.1
set routing-options router-id 192.168.1.1
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.1
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$eygMWXwsg4JU9ABRSyvMaJGDiq5Q3"
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$S6gyKW7NVbY4z3Au1ISysYgoJUk.f"
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
set protocols ospf area 0.0.0.0 interface irb.120 passive
set protocols ospf reference-bandwidth 100g
```
### PE2
```
root@PE2> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE2
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.12.1/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/5 flexible-vlan-tagging
set interfaces ge-0/0/5 encapsulation flexible-ethernet-services
set interfaces ge-0/0/5 unit 140 encapsulation vlan-bridge
set interfaces ge-0/0/5 unit 140 vlan-id 140
set interfaces ge-0/0/6 unit 0 family inet address 172.16.26.1/31
set interfaces ge-0/0/6 unit 0 family mpls
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 120 encapsulation vlan-bridge
set interfaces ge-0/0/7 unit 120 vlan-id 120
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 130 encapsulation vlan-bridge
set interfaces ge-0/0/8 unit 130 vlan-id 130
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 110 encapsulation vlan-bridge
set interfaces ge-0/0/9 unit 110 vlan-id 110
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AB6B6D6DB
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AB6B6D6DB
set interfaces irb unit 120 family inet address 10.120.0.254/24
set interfaces irb unit 130 family inet address 10.130.12.254/24
set interfaces irb unit 140 family inet address 10.140.123.252/24 virtual-gateway-address 10.140.123.254
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
set routing-instances BLUE-HUEPLET-LIMITED instance-type evpn
set routing-instances BLUE-HUEPLET-LIMITED protocols evpn
set routing-instances BLUE-HUEPLET-LIMITED vlan-id 120
set routing-instances BLUE-HUEPLET-LIMITED routing-interface irb.120
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.120
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:120
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN instance-type evpn
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN protocols evpn
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN vlan-id 130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN routing-interface irb.130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN interface ge-0/0/8.130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN vrf-target target:65500:130
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface irb.130
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-target target:65500:330
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-table-label
set routing-instances PURPLE-PILLS-EVPN instance-type evpn
set routing-instances PURPLE-PILLS-EVPN protocols evpn
set routing-instances PURPLE-PILLS-EVPN vlan-id 110
set routing-instances PURPLE-PILLS-EVPN interface ge-0/0/9.110
set routing-instances PURPLE-PILLS-EVPN vrf-target target:65500:110
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN instance-type evpn
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN protocols evpn default-gateway do-not-advertise
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN vlan-id 140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN routing-interface irb.140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN interface ge-0/0/5.140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN vrf-target target:65500:140
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN interface irb.140
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-target target:65500:340
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-table-label
set routing-options route-distinguisher-id 192.168.1.2
set routing-options router-id 192.168.1.2
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.2
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$N0VbYGUiH.fIElvLXdVq.P5Q3Ct0"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$1ooIcrMWXx-bmf3/tp1IN-VwY4GDH"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface irb.120 passive
set protocols ospf reference-bandwidth 100g
```
### PE3
```
root@PE3> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE3
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces ge-0/0/7 unit 120 encapsulation vlan-bridge
set interfaces ge-0/0/7 unit 120 vlan-id 120
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 130 vlan-id 130
set interfaces ge-0/0/8 unit 130 family inet address 10.130.30.254/24
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 140 encapsulation vlan-bridge
set interfaces ge-0/0/9 unit 140 vlan-id 140
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AB6B6E008
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AB6B6E008
set interfaces irb unit 120 family inet address 10.120.0.254/24
set interfaces irb unit 140 family inet address 10.140.123.253/24 virtual-gateway-address 10.140.123.254
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
set routing-instances BLUE-HUEPLET-LIMITED instance-type evpn
set routing-instances BLUE-HUEPLET-LIMITED protocols evpn
set routing-instances BLUE-HUEPLET-LIMITED vlan-id 120
set routing-instances BLUE-HUEPLET-LIMITED routing-interface irb.120
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.120
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:120
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface ge-0/0/8.130
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-target target:65500:330
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN instance-type evpn
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN protocols evpn default-gateway do-not-advertise
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN vlan-id 140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN routing-interface irb.140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN interface ge-0/0/9.140
set routing-instances RED-CUSTOMER-HUYASTOMER-EVPN vrf-target target:65500:140
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN interface irb.140
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-target target:65500:340
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-table-label
set routing-options route-distinguisher-id 192.168.1.3
set routing-options router-id 192.168.1.3
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.3
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$26oaG.m5TF6lKXNbw4ozFn/Cp1Rc"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/4.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$5T3/puB1ESs2ZDkq5TREcylvX7d"
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
set protocols ospf area 0.0.0.0 interface irb.120 passive
set protocols ospf reference-bandwidth 100g
```
### PE4
```
root@PE4> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE4
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces ge-0/0/7 unit 120 encapsulation vlan-bridge
set interfaces ge-0/0/7 unit 120 vlan-id 120
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 130 vlan-id 130
set interfaces ge-0/0/8 unit 130 family inet address 10.130.40.254/24
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 141 vlan-id 141
set interfaces ge-0/0/9 unit 141 family inet address 10.141.40.254/24
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AB6B6E05B
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AB6B6E05B
set interfaces irb unit 120 family inet address 10.120.0.254/24
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
set routing-instances BLUE-HUEPLET-LIMITED instance-type evpn
set routing-instances BLUE-HUEPLET-LIMITED protocols evpn
set routing-instances BLUE-HUEPLET-LIMITED vlan-id 120
set routing-instances BLUE-HUEPLET-LIMITED routing-interface irb.120
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.120
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:120
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface ge-0/0/8.130
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-target target:65500:330
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN interface ge-0/0/9.141
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-target target:65500:340
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-table-label
set routing-options route-distinguisher-id 192.168.1.4
set routing-options router-id 192.168.1.4
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.4
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$ojZGjf5zF6CvWNVY2JZn69ApOEcr"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$oyaUimPTQ3/evx-wsoaF369AuIES"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/3.0
set protocols mpls interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface irb.120 passive
set protocols ospf reference-bandwidth 100g
```
### P5
```
root@PE5> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE5
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AB6B6DACA
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AB6B6DACA
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
set routing-options router-id 192.168.1.5
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.5
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$hv0yrK7NVbY4z3Au1ISysYgoJUk.f"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$J0Zjkf5zF6CvWNVY2JZn69ApOEcr"
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
### P6
```
root@PE6> show configuration | display set
set version 24.2R1-S2.5
set system host-name PE6
set system root-authentication encrypted-password "$6$l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AB6B6DEC3
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AB6B6DEC3
set interfaces lo0 unit 0 family inet address 192.168.1.6/32
set routing-options router-id 192.168.1.6
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 192.168.1.6
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$xPb-dwJZDjkmBIyeW8N-Hk.P5z/Cp"
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/4.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 192.168.1.0/24 authentication-key "$9$/JPx9pOEhyrKWZUqPQz/9eKM8XNwY4"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface ge-0/0/4.0
set protocols mpls interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
set protocols ospf reference-bandwidth 100g
```
