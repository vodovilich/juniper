- PE-CE VLAN-ID 30 within VPN called 'BLUE-HUEPLET-LIMITED'.
- PE-CE routing: OSPF
- RT=target:65500:30 - manually assigned
#### All PEs
```
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 30 vlan-id 30
!
set routing-instances BLUE-HUEPLET-LIMITED instance-type vrf
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.30
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:30
set routing-instances BLUE-HUEPLET-LIMITED vrf-table-label
set routing-instances BLUE-HUEPLET-LIMITED prot ospf area 0 int all
!
set policy-options policy-statement BGP-to-OSPF term 10 from protocol bgp
set policy-options policy-statement BGP-to-OSPF term 10 then accept
set routing-instances BLUE-HUEPLET-LIMITED protocols ospf export BGP-to-OSPF
```
#### PE1
```
set interfaces ge-0/0/7 unit 30 family inet address 10.0.31.1/31
```
#### PE2
```
set interfaces ge-0/0/7 unit 30 family inet address 10.0.32.1/31
```
#### PE3
```
set interfaces ge-0/0/7 unit 30 family inet address 10.0.33.1/31
```

#### PE4
```
set interfaces ge-0/0/7 unit 30 family inet address 10.0.34.1/31
```
#### Verification
```
BLUE_R4#show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2
       i - IS-IS, su - IS-IS summary, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area, * - candidate default, U - per-user static route
       o - ODR, P - periodic downloaded static route, H - NHRP, l - LISP
       a - application route
       + - replicated route, % - next hop override, p - overrides from PfR
Gateway of last resort is not set
      10.0.0.0/8 is variably subnetted, 5 subnets, 2 masks
O E2     10.0.31.0/31 [110/0] via 10.0.34.1, 00:00:09, Ethernet0/0.30
O E2     10.0.32.0/31 [110/0] via 10.0.34.1, 00:00:09, Ethernet0/0.30
O E2     10.0.33.0/31 [110/0] via 10.0.34.1, 00:00:09, Ethernet0/0.30
C        10.0.34.0/31 is directly connected, Ethernet0/0.30
L        10.0.34.0/32 is directly connected, Ethernet0/0.30
      192.168.30.0/32 is subnetted, 4 subnets
O IA     192.168.30.1 [110/12] via 10.0.34.1, 00:00:09, Ethernet0/0.30
O IA     192.168.30.2 [110/12] via 10.0.34.1, 00:00:09, Ethernet0/0.30
O IA     192.168.30.3 [110/12] via 10.0.34.1, 00:00:09, Ethernet0/0.30
C        192.168.30.4 is directly connected, Loopback0
BLUE_R4#ping 192.168.30.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.30.1, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 2/2/3 ms
BLUE_R4#ping 192.168.30.2
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.30.2, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/2 ms
BLUE_R4#ping 192.168.30.3
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.30.3, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/2 ms
```
