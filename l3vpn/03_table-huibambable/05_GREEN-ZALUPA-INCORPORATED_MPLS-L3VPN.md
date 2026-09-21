- PE-CE VLAN-ID 20 within VPN called 'GREEN-ZALUPA-INCORPORATED'.
- PE-CE routing: EBGP
- CE devices in this VPN are using ASN 65020
- RT=target:65500:20 - manually assigned
- `advertise-peer-as` to bypass loop prevention (announce prefixes among all GREEN AS 65020 peers)

#### All PEs
```
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 20 vlan-id 20
!
set routing-instances GREEN-ZALUPA-INCORPORATED instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED interface ge-0/0/8.20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-target target:65500:20
set routing-instances GREEN-ZALUPA-INCORPORATED vrf-table-label
set routing-instances GREEN-ZALUPA-INCORPORATED prot bgp group CE-EBGP peer-as 65020
!
set routing-instances GREEN-ZALUPA-INCORPORATED protocols bgp group CE-EBGP advertise-peer-as
```
PE1
```
set interfaces ge-0/0/8 unit 20 family inet address 10.0.21.1/31
!
set routing-instances GREEN-ZALUPA-INCORPORATED prot bgp group CE-EBGP neighbor 10.0.21.0
```
PE2
```
set interfaces ge-0/0/8 unit 20 family inet address 10.0.22.1/31
!
set routing-instances GREEN-ZALUPA-INCORPORATED prot bgp group CE-EBGP neighbor 10.0.22.0
```
PE3
```
set interfaces ge-0/0/8 unit 20 family inet address 10.0.23.1/31
!
set routing-instances GREEN-ZALUPA-INCORPORATED prot bgp group CE-EBGP neighbor 10.0.23.0
```
PE4
```
set interfaces ge-0/0/8 unit 20 family inet address 10.0.24.1/31
!
set routing-instances GREEN-ZALUPA-INCORPORATED prot bgp group CE-EBGP neighbor 10.0.24.0
```
#### Verification
```
GREEN_R3#show ip route
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
B        10.0.21.0/31 [20/0] via 10.0.23.1, 00:01:34
B        10.0.22.0/31 [20/0] via 10.0.23.1, 00:01:34
C        10.0.23.0/31 is directly connected, Ethernet0/0.20
L        10.0.23.0/32 is directly connected, Ethernet0/0.20
B        10.0.24.0/31 [20/0] via 10.0.23.1, 00:01:34
      192.168.20.0/32 is subnetted, 4 subnets
B        192.168.20.1 [20/0] via 10.0.23.1, 00:00:58
B        192.168.20.2 [20/0] via 10.0.23.1, 00:00:58
C        192.168.20.3 is directly connected, Loopback0
B        192.168.20.4 [20/0] via 10.0.23.1, 00:00:51
!
GREEN_R3#ping 192.168.20.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.20.1, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 2/2/3 ms
!
GREEN_R3#ping 192.168.20.2
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.20.2, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 2/3/5 ms
!
GREEN_R3#ping 192.168.20.4
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.20.4, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/2 ms
```
