### PE1
```
root@PE1> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE1
set system root-authentication encrypted-password "6l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/2 unit 0 family inet address 172.16.12.0/31
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.15.1/31
set interfaces ge-0/0/5 unit 0 family mpls
set interfaces ge-0/0/7 gigether-options 802.3ad ae0
set interfaces ge-0/0/8 gigether-options 802.3ad ae1
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 0 family bridge interface-mode trunk
set interfaces ge-0/0/9 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:01:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:12
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 unit 100 encapsulation vlan-bridge
set interfaces ae0 unit 100 vlan-id 100
set interfaces ae1 flexible-vlan-tagging
set interfaces ae1 encapsulation flexible-ethernet-services
set interfaces ae1 esi 00:01:00:00:00:00:00:00:00:02
set interfaces ae1 esi all-active
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:12
set interfaces ae1 unit 0 family bridge interface-mode trunk
set interfaces ae1 unit 0 family bridge vlan-id-list 11-13
set interfaces ae1 unit 100 encapsulation vlan-bridge
set interfaces ae1 unit 100 vlan-id 100
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6ABE11B4F0
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6ABE11B4F0
set interfaces irb unit 11 family inet address 192.168.1.253/24 virtual-gateway-address 192.168.1.254
set interfaces irb unit 12 family inet address 192.168.1.253/24 virtual-gateway-address 192.168.1.254
set interfaces irb unit 13 family inet address 192.168.1.254/24
set interfaces irb unit 13 mac aa:aa:aa:aa:aa:aa
set interfaces irb unit 100 family inet address 192.168.100.253/24 virtual-gateway-address 192.168.100.254
set interfaces lo0 unit 0 family inet address 172.16.255.1/32
set routing-instances ASSVILLE-EVPN-VLAN-AWARE instance-type virtual-switch
set routing-instances ASSVILLE-EVPN-VLAN-AWARE protocols evpn extended-vlan-list 11-13
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-11 vlan-id 11
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-11 routing-interface irb.11
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-12 vlan-id 12
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-12 routing-interface irb.12
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-13 vlan-id 13
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-13 routing-interface irb.13
set routing-instances ASSVILLE-EVPN-VLAN-AWARE interface ge-0/0/9.0
set routing-instances ASSVILLE-EVPN-VLAN-AWARE interface ae0.0
set routing-instances ASSVILLE-EVPN-VLAN-AWARE interface ae1.0
set routing-instances ASSVILLE-EVPN-VLAN-AWARE vrf-target target:65500:65001
set routing-instances ASSVILLE-EVPN-VLAN-BASED instance-type evpn
set routing-instances ASSVILLE-EVPN-VLAN-BASED protocols evpn
set routing-instances ASSVILLE-EVPN-VLAN-BASED vlan-id 100
set routing-instances ASSVILLE-EVPN-VLAN-BASED routing-interface irb.100
set routing-instances ASSVILLE-EVPN-VLAN-BASED interface ae0.100
set routing-instances ASSVILLE-EVPN-VLAN-BASED interface ae1.100
set routing-instances ASSVILLE-EVPN-VLAN-BASED vrf-target target:65500:100200
set routing-instances L3VPN-100200 instance-type vrf
set routing-instances L3VPN-100200 interface irb.100
set routing-instances L3VPN-100200 vrf-target target:65500:100200
set routing-instances L3VPN-100200 vrf-table-label
set routing-instances L3VPN-12 instance-type vrf
set routing-instances L3VPN-12 interface irb.12
set routing-instances L3VPN-12 vrf-target target:65500:12
set routing-instances L3VPN-12 vrf-table-label
set routing-instances L3VPN-13 instance-type vrf
set routing-instances L3VPN-13 interface irb.13
set routing-instances L3VPN-13 vrf-target target:65500:13
set routing-instances L3VPN-13 vrf-table-label
set routing-options route-distinguisher-id 172.16.255.1
set routing-options router-id 172.16.255.1
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 172.16.255.1
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$ZRDjkQzn6Cp8XVs4oUD9CtuOISrK"
set protocols bgp group IBGP-CORE neighbor 172.16.255.2
set protocols bgp group IBGP-CORE neighbor 172.16.255.3
set protocols bgp group IBGP-CORE neighbor 172.16.255.4
set protocols bgp group IBGP-CORE neighbor 172.16.255.5
set protocols bgp group IBGP-CORE neighbor 172.16.255.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 172.16.255.0/24 authentication-key "$9$VQb2oUDHkm5RheMXxVb.mfTznApO"
set protocols mpls traffic-engineering mpls-forwarding
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface irb.11 passive
set protocols ospf reference-bandwidth 100g
```
### PE2
```
root@PE2> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE2
set system root-authentication encrypted-password "6l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/1 unit 0 family inet address 172.16.12.1/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/6 unit 0 family inet address 172.16.26.1/31
set interfaces ge-0/0/6 unit 0 family mpls
set interfaces ge-0/0/7 gigether-options 802.3ad ae0
set interfaces ge-0/0/8 gigether-options 802.3ad ae1
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 0 family bridge interface-mode trunk
set interfaces ge-0/0/9 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:01:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:12
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 unit 100 encapsulation vlan-bridge
set interfaces ae0 unit 100 vlan-id 100
set interfaces ae1 flexible-vlan-tagging
set interfaces ae1 encapsulation flexible-ethernet-services
set interfaces ae1 esi 00:01:00:00:00:00:00:00:00:02
set interfaces ae1 esi all-active
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:12
set interfaces ae1 unit 0 family bridge interface-mode trunk
set interfaces ae1 unit 0 family bridge vlan-id-list 11-13
set interfaces ae1 unit 100 encapsulation vlan-bridge
set interfaces ae1 unit 100 vlan-id 100
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6ABE11B73E
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6ABE11B73E
set interfaces irb unit 11 family inet address 192.168.1.252/24 virtual-gateway-address 192.168.1.254
set interfaces irb unit 12 family inet address 192.168.1.252/24 virtual-gateway-address 192.168.1.254
set interfaces irb unit 13 family inet address 192.168.1.254/24
set interfaces irb unit 13 mac aa:aa:aa:aa:aa:aa
set interfaces irb unit 100 family inet address 192.168.100.252/24 virtual-gateway-address 192.168.100.254
set interfaces lo0 unit 0 family inet address 172.16.255.2/32
set routing-instances ASSVILLE-EVPN-VLAN-AWARE instance-type virtual-switch
set routing-instances ASSVILLE-EVPN-VLAN-AWARE protocols evpn extended-vlan-list 11-13
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-11 vlan-id 11
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-11 routing-interface irb.11
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-12 vlan-id 12
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-12 routing-interface irb.12
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-13 vlan-id 13
set routing-instances ASSVILLE-EVPN-VLAN-AWARE bridge-domains BD-13 routing-interface irb.13
set routing-instances ASSVILLE-EVPN-VLAN-AWARE interface ge-0/0/9.0
set routing-instances ASSVILLE-EVPN-VLAN-AWARE interface ae0.0
set routing-instances ASSVILLE-EVPN-VLAN-AWARE interface ae1.0
set routing-instances ASSVILLE-EVPN-VLAN-AWARE vrf-target target:65500:65001
set routing-instances ASSVILLE-EVPN-VLAN-BASED instance-type evpn
set routing-instances ASSVILLE-EVPN-VLAN-BASED protocols evpn
set routing-instances ASSVILLE-EVPN-VLAN-BASED vlan-id 100
set routing-instances ASSVILLE-EVPN-VLAN-BASED routing-interface irb.100
set routing-instances ASSVILLE-EVPN-VLAN-BASED interface ae0.100
set routing-instances ASSVILLE-EVPN-VLAN-BASED interface ae1.100
set routing-instances ASSVILLE-EVPN-VLAN-BASED vrf-target target:65500:100200
set routing-instances L3VPN-100200 instance-type vrf
set routing-instances L3VPN-100200 interface irb.100
set routing-instances L3VPN-100200 vrf-target target:65500:100200
set routing-instances L3VPN-100200 vrf-table-label
set routing-instances L3VPN-12 instance-type vrf
set routing-instances L3VPN-12 interface irb.12
set routing-instances L3VPN-12 vrf-target target:65500:12
set routing-instances L3VPN-12 vrf-table-label
set routing-instances L3VPN-13 instance-type vrf
set routing-instances L3VPN-13 interface irb.13
set routing-instances L3VPN-13 vrf-target target:65500:13
set routing-instances L3VPN-13 vrf-table-label
set routing-options route-distinguisher-id 172.16.255.2
set routing-options router-id 172.16.255.2
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 172.16.255.2
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$WFkXx-g4JZDHp0ESeKLXUDik.fFn9"
set protocols bgp group IBGP-CORE neighbor 172.16.255.1
set protocols bgp group IBGP-CORE neighbor 172.16.255.3
set protocols bgp group IBGP-CORE neighbor 172.16.255.4
set protocols bgp group IBGP-CORE neighbor 172.16.255.5
set protocols bgp group IBGP-CORE neighbor 172.16.255.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 172.16.255.0/24 authentication-key "$9$E5qhrKLXN-bY5Q/A0OEhVbs24JjH."
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
set protocols ospf area 0.0.0.0 interface irb.11 passive
set protocols ospf reference-bandwidth 100g
```
### PE3
```
root@PE3> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE3
set system root-authentication encrypted-password "6l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/4 unit 0 family inet address 172.16.34.0/31
set interfaces ge-0/0/4 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.35.1/31
set interfaces ge-0/0/5 unit 0 family mpls
set interfaces ge-0/0/7 gigether-options 802.3ad ae0
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 0 family bridge interface-mode trunk
set interfaces ge-0/0/8 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:02:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:34
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 unit 200 encapsulation vlan-bridge
set interfaces ae0 unit 200 vlan-id 200
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6ABE11C01B
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6ABE11C01B
set interfaces irb unit 11 family inet address 192.168.2.253/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 11 family inet address 192.168.2.252/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 12 family inet address 192.168.2.253/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 12 family inet address 192.168.2.252/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 13 family inet address 192.168.2.254/24
set interfaces irb unit 13 mac aa:aa:aa:aa:aa:aa
set interfaces irb unit 200 family inet address 192.168.200.253/24 virtual-gateway-address 192.168.200.254
set interfaces lo0 unit 0 family inet address 172.16.255.3/32
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE instance-type virtual-switch
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE protocols evpn extended-vlan-list 11-13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-11 vlan-id 11
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-11 routing-interface irb.11
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-12 vlan-id 12
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-12 routing-interface irb.12
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-13 vlan-id 13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-13 routing-interface irb.13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE interface ge-0/0/8.0
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE interface ae0.0
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE vrf-target target:65500:65002
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED instance-type evpn
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED protocols evpn
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED vlan-id 200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED routing-interface irb.200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED interface ae0.200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED vrf-target target:65500:100200
set routing-instances L3VPN-100200 instance-type vrf
set routing-instances L3VPN-100200 interface irb.200
set routing-instances L3VPN-100200 vrf-target target:65500:100200
set routing-instances L3VPN-100200 vrf-table-label
set routing-instances L3VPN-12 instance-type vrf
set routing-instances L3VPN-12 interface irb.12
set routing-instances L3VPN-12 vrf-target target:65500:12
set routing-instances L3VPN-12 vrf-table-label
set routing-instances L3VPN-13 instance-type vrf
set routing-instances L3VPN-13 interface irb.13
set routing-instances L3VPN-13 vrf-target target:65500:13
set routing-instances L3VPN-13 vrf-table-label
set routing-options route-distinguisher-id 172.16.255.3
set routing-options router-id 172.16.255.3
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 172.16.255.3
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$/WvTAt0cSleMLUjm5F3CAvM8X7dYga"
set protocols bgp group IBGP-CORE neighbor 172.16.255.1
set protocols bgp group IBGP-CORE neighbor 172.16.255.2
set protocols bgp group IBGP-CORE neighbor 172.16.255.4
set protocols bgp group IBGP-CORE neighbor 172.16.255.5
set protocols bgp group IBGP-CORE neighbor 172.16.255.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/4.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 172.16.255.0/24 authentication-key "$9$akJDHPfQzn9KM7dsYaJ3n/Ct0Rhy"
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
set protocols ospf area 0.0.0.0 interface irb.11 passive
set protocols ospf reference-bandwidth 100g
```
### PE4
```
root@PE4> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name PE4
set system root-authentication encrypted-password "6l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/3 unit 0 family inet address 172.16.34.1/31
set interfaces ge-0/0/3 unit 0 family mpls
set interfaces ge-0/0/6 unit 0 family inet address 172.16.46.1/31
set interfaces ge-0/0/6 unit 0 family mpls
set interfaces ge-0/0/7 gigether-options 802.3ad ae0
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 0 family bridge interface-mode trunk
set interfaces ge-0/0/8 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:02:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:34
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list 11-13
set interfaces ae0 unit 200 encapsulation vlan-bridge
set interfaces ae0 unit 200 vlan-id 200
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6ABE11C3D8
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6ABE11C3D8
set interfaces irb unit 11 family inet address 192.168.2.253/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 11 family inet address 192.168.2.252/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 12 family inet address 192.168.2.253/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 12 family inet address 192.168.2.252/24 virtual-gateway-address 192.168.2.254
set interfaces irb unit 13 family inet address 192.168.2.254/24
set interfaces irb unit 13 mac aa:aa:aa:aa:aa:aa
set interfaces irb unit 200 family inet address 192.168.200.252/24 virtual-gateway-address 192.168.200.254
set interfaces lo0 unit 0 family inet address 172.16.255.4/32
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE instance-type virtual-switch
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE protocols evpn extended-vlan-list 11-13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-11 vlan-id 11
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-11 routing-interface irb.11
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-12 vlan-id 12
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-12 routing-interface irb.12
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-13 vlan-id 13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-13 routing-interface irb.13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE interface ge-0/0/8.0
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE interface ae0.0
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE vrf-target target:65500:65002
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED instance-type evpn
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED protocols evpn
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED vlan-id 200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED routing-interface irb.200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED interface ae0.200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED vrf-target target:65500:100200
set routing-instances L3VPN-100200 instance-type vrf
set routing-instances L3VPN-100200 interface irb.200
set routing-instances L3VPN-100200 vrf-target target:65500:100200
set routing-instances L3VPN-100200 vrf-table-label
set routing-instances L3VPN-12 instance-type vrf
set routing-instances L3VPN-12 interface irb.12
set routing-instances L3VPN-12 vrf-target target:65500:12
set routing-instances L3VPN-12 vrf-table-label
set routing-instances L3VPN-13 instance-type vrf
set routing-instances L3VPN-13 interface irb.13
set routing-instances L3VPN-13 vrf-target target:65500:13
set routing-instances L3VPN-13 vrf-table-label
set routing-options route-distinguisher-id 172.16.255.4
set routing-options router-id 172.16.255.4
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 172.16.255.4
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$eaqMWXwsg4JU9ABRSyvMaJGDiq5Q3"
set protocols bgp group IBGP-CORE neighbor 172.16.255.1
set protocols bgp group IBGP-CORE neighbor 172.16.255.2
set protocols bgp group IBGP-CORE neighbor 172.16.255.3
set protocols bgp group IBGP-CORE neighbor 172.16.255.5
set protocols bgp group IBGP-CORE neighbor 172.16.255.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 172.16.255.0/24 authentication-key "$9$1k4IcrMWXx-bmf3/tp1IN-VwY4GDH"
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
set protocols ospf area 0.0.0.0 interface irb.11 passive
set protocols ospf reference-bandwidth 100g
```
### P5
```
root@P5> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name P5
set system root-authentication encrypted-password "6l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6ABE11BCD5
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6ABE11BCD5
set interfaces lo0 unit 0 family inet address 172.16.255.5/32
set routing-options route-distinguisher-id 172.16.255.5
set routing-options router-id 172.16.255.5
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 172.16.255.5
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$dWwsgDjkqPTEcKWx7bwmP5QF6tuB"
set protocols bgp group IBGP-CORE neighbor 172.16.255.1
set protocols bgp group IBGP-CORE neighbor 172.16.255.2
set protocols bgp group IBGP-CORE neighbor 172.16.255.3
set protocols bgp group IBGP-CORE neighbor 172.16.255.4
set protocols bgp group IBGP-CORE neighbor 172.16.255.6
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface ge-0/0/6.0
set protocols ldp session-group 172.16.255.0/24 authentication-key "$9$/qoM9pOEhyrKWZUqPQz/9eKM8XNwY4"
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
root@P6> show configuration | display set | no-more
set version 24.2R1-S2.5
set system host-name P6
set system root-authentication encrypted-password "6l3Tl1.77$694osmMXY7aQzswWCDWBu5KK4Els9dZ7T2JBz3ttzXjVOfg2LC8QkVpWqtT8NuyEoFYzMjY5IQUufuuCYkxFo/"
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
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6ABE11C0B3
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6ABE11C0B3
set interfaces lo0 unit 0 family inet address 172.16.255.6/32
set routing-options route-distinguisher-id 172.16.255.6
set routing-options router-id 172.16.255.6
set routing-options autonomous-system 65500
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE local-address 172.16.255.6
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key "$9$PTQ3puB1ESs2ZDkq5TREcylvX7d"
set protocols bgp group IBGP-CORE neighbor 172.16.255.1
set protocols bgp group IBGP-CORE neighbor 172.16.255.2
set protocols bgp group IBGP-CORE neighbor 172.16.255.3
set protocols bgp group IBGP-CORE neighbor 172.16.255.4
set protocols bgp group IBGP-CORE neighbor 172.16.255.5
set protocols ldp track-igp-metric
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/4.0
set protocols ldp interface ge-0/0/5.0
set protocols ldp session-group 172.16.255.0/24 authentication-key "$9$pw6yu1ErlvML7ik5z6/pu8LxNdw4aG"
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
### balls-s2
```
balls-s2#show run
Building configuration...

Current configuration : 4477 bytes
!
! Last configuration change at 21:28:24 UTC Sat Oct 3 2026
!
version 15.2
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
service compress-config
!
hostname balls-s2
!
boot-start-marker
boot-end-marker
!
!
vrf definition VLAN12
 !
 address-family ipv4
 exit-address-family
!
vrf definition VLAN13
 !
 address-family ipv4
 exit-address-family
!
vrf definition VLAN200
 !
 address-family ipv4
 exit-address-family
!
!
no aaa new-model
!
!
ip cef
no ipv6 cef
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
!
interface Port-channel1
 switchport trunk allowed vlan 11-13,200
 switchport trunk encapsulation dot1q
 switchport mode trunk
 switchport nonegotiate
!
interface Ethernet0/0
 switchport trunk allowed vlan 11-13,200
 switchport trunk encapsulation dot1q
 switchport mode trunk
 switchport nonegotiate
 channel-group 1 mode active
!
interface Ethernet0/1
 switchport trunk allowed vlan 11-13,200
 switchport trunk encapsulation dot1q
 switchport mode trunk
 switchport nonegotiate
 channel-group 1 mode active
!
interface Ethernet0/2
!
interface Ethernet0/3
!
interface Vlan11
 ip address 192.168.2.2 255.255.255.0
!
interface Vlan12
 vrf forwarding VLAN12
 ip address 192.168.2.2 255.255.255.0
!
interface Vlan13
 vrf forwarding VLAN13
 ip address 192.168.2.2 255.255.255.0
!
interface Vlan200
 vrf forwarding VLAN200
 ip address 192.168.200.2 255.255.255.0
!
ip forward-protocol nd
!
ip http server
!
ip route 0.0.0.0 0.0.0.0 192.168.2.254
ip route vrf VLAN12 0.0.0.0 0.0.0.0 192.168.2.254
ip route vrf VLAN13 0.0.0.0 0.0.0.0 192.168.2.254
ip route vrf VLAN200 0.0.0.0 0.0.0.0 192.168.200.254
ip ssh server algorithm encryption aes128-ctr aes192-ctr aes256-ctr
ip ssh client algorithm encryption aes128-ctr aes192-ctr aes256-ctr
!
!
ip sla 1101
 icmp-echo 192.168.1.1
 frequency 30
ip sla schedule 1101 life forever start-time now
ip sla 1102
 icmp-echo 192.168.1.2
 frequency 30
ip sla schedule 1102 life forever start-time now
ip sla 1103
 icmp-echo 192.168.1.3
 frequency 30
ip sla schedule 1103 life forever start-time now
ip sla 1104
 icmp-echo 192.168.1.4
 frequency 30
ip sla schedule 1104 life forever start-time now
ip sla 1201
 icmp-echo 192.168.2.1
 frequency 30
ip sla schedule 1201 life forever start-time now
ip sla 1203
 icmp-echo 192.168.2.3
 frequency 30
ip sla schedule 1203 life forever start-time now
ip sla 121101
 icmp-echo 192.168.1.1 source-interface Vlan12
 vrf VLAN12
 frequency 30
ip sla schedule 121101 life forever start-time now
ip sla 121102
 icmp-echo 192.168.1.2 source-interface Vlan12
 vrf VLAN12
 frequency 30
ip sla schedule 121102 life forever start-time now
ip sla 121103
 icmp-echo 192.168.1.3 source-interface Vlan12
 vrf VLAN12
 frequency 30
ip sla schedule 121103 life forever start-time now
ip sla 121104
 icmp-echo 192.168.1.4 source-interface Vlan12
 vrf VLAN12
 frequency 30
ip sla schedule 121104 life forever start-time now
ip sla 121201
 icmp-echo 192.168.2.1 source-interface Vlan12
 vrf VLAN12
 frequency 30
ip sla schedule 121201 life forever start-time now
ip sla 121203
 icmp-echo 192.168.2.3 source-interface Vlan12
 vrf VLAN12
 frequency 30
ip sla schedule 121203 life forever start-time now
ip sla 131101
 icmp-echo 192.168.1.1 source-interface Vlan13
 vrf VLAN13
 frequency 30
ip sla schedule 131101 life forever start-time now
ip sla 131102
 icmp-echo 192.168.1.2 source-interface Vlan13
 vrf VLAN13
 frequency 30
ip sla schedule 131102 life forever start-time now
ip sla 131103
 icmp-echo 192.168.1.3 source-interface Vlan13
 vrf VLAN13
 frequency 30
ip sla schedule 131103 life forever start-time now
ip sla 131104
 icmp-echo 192.168.1.4 source-interface Vlan13
 vrf VLAN13
 frequency 30
ip sla schedule 131104 life forever start-time now
ip sla 131201
 icmp-echo 192.168.2.1 source-interface Vlan13
 vrf VLAN13
 frequency 30
ip sla schedule 131201 life forever start-time now
ip sla 131203
 icmp-echo 192.168.2.3 source-interface Vlan13
 vrf VLAN13
 frequency 30
ip sla schedule 131203 life forever start-time now
ip sla 2001102
 icmp-echo 192.168.100.2 source-interface Vlan200
 vrf VLAN200
 frequency 30
ip sla schedule 2001102 life forever start-time now
ip sla 2001103
 icmp-echo 192.168.100.3 source-interface Vlan200
 vrf VLAN200
 frequency 30
ip sla schedule 2001103 life forever start-time now
!
!
!
control-plane
!
!
line con 0
 logging synchronous
line aux 0
line vty 0 4
!
!
!
end
```
