## ISP CORE
### OSPF, LDP, MP-BGP
#### All Routers
```
set protocols ospf reference-bandwidth 100g
set protocols ospf area 0 interface lo0.0 passive
!
set routing-options autonomous-system 65500
set protocols bgp group IBGP-CORE type internal
!
set protocols ldp session-group 192.168.1.0/24 authentication-key LDPSECRET
set protocols ldp track-igp-metric
set protocols mpls no-propagate-ttl
set protocols mpls icmp-tunneling
set protocols mpls traffic-engineering mpls-forwarding
!
set routing-options autonomous-system 65500
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE family evpn signaling
set protocols bgp group IBGP-CORE authentication-key BGPSECRET
```
#### PE1
```
set interfaces ge-0/0/2 unit 0 family inet address 172.16.12.0/31
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.15.1/31
set interfaces ge-0/0/5 unit 0 family mpls
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
!
set routing-options router-id 192.168.1.1
set routing-options route-distinguisher-id 192.168.1.1
set protocols ospf area 0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/5.0 interface-type p2p
!
set interface ge-0/0/2.0 family mpls
set interface ge-0/0/5.0 family mpls
set protocols mpls interface ge-0/0/2.0 
set protocols mpls interface ge-0/0/5.0 
set protocols ldp interface ge-0/0/2.0 
set protocols ldp interface ge-0/0/5.0 
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
!
!
set protocols bgp group IBGP-CORE local-address 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### PE2
```
set interfaces ge-0/0/1 unit 0 family inet address 172.16.12.1/31
set interfaces ge-0/0/6 unit 0 family inet address 172.16.26.1/31
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
!
set routing-options router-id 192.168.1.2
set routing-options route-distinguisher-id 192.168.1.2
set protocols ospf area 0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/6.0 interface-type p2p
!
set interface ge-0/0/1.0 family mpls
set protocols mpls interface ge-0/0/1.0
set protocols ldp interface ge-0/0/1.0
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 ldp-synchronization
!
set interface ge-0/0/6.0 family mpls
set protocols mpls interface ge-0/0/6.0
set protocols ldp interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
!
!
set protocols bgp group IBGP-CORE local-address 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### PE3
```
set interfaces ge-0/0/4 unit 0 family inet address 172.16.34.0/31
set interfaces ge-0/0/5 unit 0 family inet address 172.16.35.1/31
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
!
set routing-options router-id 192.168.1.3
set routing-options route-distinguisher-id 192.168.1.3
set protocols ospf area 0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/5.0 interface-type p2p
!
set interface ge-0/0/4.0 family mpls
set protocols mpls interface ge-0/0/4.0
set protocols ldp interface ge-0/0/4.0
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 ldp-synchronization
!
set interface ge-0/0/5.0 family mpls
set protocols mpls interface ge-0/0/5.0
set protocols ldp interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
!
!
set protocols bgp group IBGP-CORE local-address 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### PE4
```
set interfaces ge-0/0/3 unit 0 family inet address 172.16.34.1/31
set interfaces ge-0/0/6 unit 0 family inet address 172.16.46.1/31
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
!
set routing-options router-id 192.168.1.4
set routing-options route-distinguisher-id 192.168.1.4
set protocols ospf area 0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/6.0 interface-type p2p
!
set interface ge-0/0/3.0 family mpls
set protocols mpls interface ge-0/0/3.0
set protocols ldp interface ge-0/0/3.0
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 ldp-synchronization
!
set interface ge-0/0/6.0 family mpls
set protocols mpls interface ge-0/0/6.0
set protocols ldp interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
!
!
set protocols bgp group IBGP-CORE local-address 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### P5
```
set interfaces ge-0/0/1 unit 0 family inet address 172.16.15.0/31
set interfaces ge-0/0/3 unit 0 family inet address 172.16.35.0/31
set interfaces ge-0/0/6 unit 0 family inet address 172.16.56.0/31
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
!
set routing-options router-id 192.168.1.5
set protocols ospf area 0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/6.0 interface-type p2p
!
set interface ge-0/0/1.0 family mpls
set protocols mpls interface ge-0/0/1.0
set protocols ldp interface ge-0/0/1.0
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 ldp-synchronization
!
set interface ge-0/0/3.0 family mpls
set protocols mpls interface ge-0/0/3.0
set protocols ldp interface ge-0/0/3.0
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 ldp-synchronization
!
set interface ge-0/0/6.0 family mpls
set protocols mpls interface ge-0/0/6.0
set protocols ldp interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
!
!
set protocols bgp group IBGP-CORE local-address 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```

#### P6
```
set interfaces ge-0/0/2 unit 0 family inet address 172.16.26.0/31
set interfaces ge-0/0/4 unit 0 family inet address 172.16.46.0/31
set interfaces ge-0/0/5 unit 0 family inet address 172.16.56.1/31
set interfaces lo0 unit 0 family inet address 192.168.1.6/32
!
set routing-options router-id 192.168.1.6
set protocols ospf area 0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/5.0 interface-type p2p
!
set interface ge-0/0/2.0 family mpls
set protocols mpls interface ge-0/0/2.0
set protocols ldp interface ge-0/0/2.0
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
!
set interface ge-0/0/4.0 family mpls
set protocols mpls interface ge-0/0/4.0
set protocols ldp interface ge-0/0/4.0
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 ldp-synchronization
!
set interface ge-0/0/5.0 family mpls
set protocols mpls interface ge-0/0/5.0
set protocols ldp interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
!
!
set protocols bgp group IBGP-CORE local-address 192.168.1.6
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
```

