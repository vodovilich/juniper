- PE-CE VLAN-ID 10 within VPN called 'RED-CUSTOMER-HUYASTOMER'.
- PE-CE routing: EBGP. 
- CE devices in this VPN are using **ASN 65010**
- RT=target:65500:10 - manually assigned
- RED_R1 is multihomed
  - Make sure traffic to and from that site traverses PE1
- `as-override` to bypass loop prevention (announce prefixes among all RED AS 65010 peers)
- **The PE interface routes should be reachable for remote sites**
  - **By default - Per-NextHop label allocation**
    - Label per unique NextHop (i.e. per-CE-facing-interface)
    - Incoming packet sent to next-hop right away once arrived
    - May be no ARP record to complete forwarding => drop
    - No lookup for IP header is performed
  - **vrf-tabel-label - enables Per-VRF allocation**
    - Label per VRF
    - Lookup for IP header is performed
    - ARP request is sent when needed
    - No need to configure export policy for direct routes exporting
  - **Example:**
    - CE1 ------ PE1 ------ P ------- PE2 ------ CE2 
      - PE2 learns routes from CE2 via BGP
      - No vrf-tabel-label needed
      - CE2’s ARP always known
    - CE1 ------ PE1 ------ P ------- PE2 --- SWITCH --- servers 
      - PE2 does not learn routes from CE2 via BGP (no packets rx-ed at all)
      - PE2 does not have MAC record for servers
      - Additional lookup is required - so as vrf-tabel-label
      - Also allows to e.g. apply firewall to VRF interfaces

/*  
But they are already exported into MP-BGP and announced because **vrf-target automatically takes all active routes in a VRF (direct, local, IGP, etc) and exports them into MP-BGP with RT community.**  
Effect of `vrf-tabel-label` is not reproducible in this lab, except label value change, YOBANIJ VASH ROT  
*/    



- Block export of the P2P subnet on the RED-R2 <-> PE3 link

#### PE1
```
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.10.1/31
!
set routing-options route-distinguisher-id 192.168.1.1
!
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label
set routing-instances RED-CUSTOMER-HUYASTOMER prot bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER prot bgp group CE-EBGP neighbor 10.0.10.0
!
set policy-options policy-statement RED_R1_IMPORT term LP_150 then local-preference 150
set routing-instances RED-CUSTOMER-HUYASTOMER prot bgp group CE-EBGP import RED_R1_IMPORT
!
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
```

**Verify as-override:**
- PE1 sees 192.168.10.3 with original AS-PATH: `65010 I`
```
root@PE1> show route table RED-CUSTOMER-HUYASTOMER.inet.0 192.168.10.3

RED-CUSTOMER-HUYASTOMER.inet.0: 7 destinations, 7 routes (7 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.10.3/32    *[BGP/170] 00:11:14, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300048, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 300048, Push 299904(top)
```
- PE1 advertises 192.168.10.3 to RED_R1 with overridden AS-PATH: `65500 I`
```
root@PE1> show route advertising-protocol bgp 10.0.10.0

RED-CUSTOMER-HUYASTOMER.inet.0: 7 destinations, 7 routes (7 active, 0 holddown, 0 hidden)
  Prefix                  Nexthop              MED     Lclpref    AS path
* 10.0.12.0/31            Self                                    I
* 10.0.13.0/31            Self                                    I
* 192.168.10.2/32         Self                                    65500 I  - 
* 192.168.10.3/32         Self                                    65500 I
```

#### PE2
```
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.11.1/31
!
set routing-options route-distinguisher-id 192.168.1.2
!
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label 
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.11.0
!
set policy-options policy-stat RED_R1_EXPORT term AS-PREPEND then as-path-prepend "65500 65500"
set routing-instances RED-CUSTOMER-HUYASTOMER prot bgp group CE-EBGP export RED_R1_EXPORT
!
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
```


#### PE3
```
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.12.1/31
!
set routing-options route-distinguisher-id 192.168.1.3
!
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label 
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.12.0
!
set policy-options community RT-RED members target:65500:10
set policy-options policy-statement RED-IMPORT term BLOCK-DIRECT from protocol direct
set policy-options policy-statement RED-IMPORT term BLOCK-DIRECT then reject
set policy-options policy-statement RED-IMPORT term ALLOW-BGP from protocol bgp
set policy-options policy-statement RED-IMPORT term ALLOW-BGP then community add RT-RED
set policy-options policy-statement RED-IMPORT term ALLOW-BGP then accept
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-export RED-IMPORT
```

#### Verification:
- Before -  10.0.12.0/31 is propagated
```
root@PE1> show route table RED-CUSTOMER-HUYASTOMER.inet.0

RED-CUSTOMER-HUYASTOMER.inet.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.10.0/31       *[Direct/0] 13:20:21
                    >  via ge-0/0/9.10
10.0.10.1/32       *[Local/0] 13:20:21
                       Local via ge-0/0/9.10
10.0.11.0/31       *[BGP/170] 01:03:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.0.12.0/31       *[BGP/170] 01:02:52, localpref 100, from 192.168.1.3               //HERE
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299920(top)
10.0.13.0/31       *[BGP/170] 01:02:47, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
192.168.10.1/32    *[BGP/170] 13:12:31, MED 0, localpref 150
                      AS path: 65010 I, validation-state: unverified
                    >  to 10.0.10.0 via ge-0/0/9.10
192.168.10.2/32    *[BGP/170] 00:01:23, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299920(top)
192.168.10.3/32    *[BGP/170] 01:02:47, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
```

- After - 10.0.12.0/31 is not advertised
```
root@PE1> show route table RED-CUSTOMER-HUYASTOMER.inet.0

RED-CUSTOMER-HUYASTOMER.inet.0: 7 destinations, 7 routes (7 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.10.0/31       *[Direct/0] 13:27:29
                    >  via ge-0/0/9.10
10.0.10.1/32       *[Local/0] 13:27:29
                       Local via ge-0/0/9.10
10.0.11.0/31       *[BGP/170] 01:10:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.0.13.0/31       *[BGP/170] 01:09:55, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
192.168.10.1/32    *[BGP/170] 13:19:39, MED 0, localpref 150
                      AS path: 65010 I, validation-state: unverified
                    >  to 10.0.10.0 via ge-0/0/9.10
192.168.10.2/32    *[BGP/170] 00:00:02, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299920(top)
192.168.10.3/32    *[BGP/170] 01:09:55, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
```


#### PE4
```
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 10 vlan-id 10
set interfaces ge-0/0/9 unit 10 family inet address 10.0.13.1/31
!
set routing-options route-distinguisher-id 192.168.1.4
!
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-table-label 
set routing-instances RED-CUSTOMER-HUYASTOMER instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER interface ge-0/0/9.10
set routing-instances RED-CUSTOMER-HUYASTOMER vrf-target target:65500:10
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP peer-as 65010
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP as-override
set routing-instances RED-CUSTOMER-HUYASTOMER protocols bgp group CE-EBGP neighbor 10.0.13.0
```

#### Verify
```
RED_R2#ping 192.168.10.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.10.1, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/2/3 ms
RED_R2#ping 192.168.10.3
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.10.3, timeout is 2 seconds:
!!!!!

RED_R2#show ip route
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
B        10.0.10.0/31 [20/0] via 10.0.12.1, 11:43:23
B        10.0.11.0/31 [20/0] via 10.0.12.1, 00:05:34
C        10.0.12.0/31 is directly connected, Ethernet0/0.10
L        10.0.12.0/32 is directly connected, Ethernet0/0.10
B        10.0.13.0/31 [20/0] via 10.0.12.1, 10:33:26
      192.168.10.0/32 is subnetted, 3 subnets
B        192.168.10.1 [20/0] via 10.0.12.1, 11:43:23
C        192.168.10.2 is directly connected, Loopback0
B        192.168.10.3 [20/0] via 10.0.12.1, 10:33:24
```
