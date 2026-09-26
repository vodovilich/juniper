## PURPLE EVPN
### VLAN-Based EVI on PE1, PE2
#### Both PE1 and PE2
```
set routing-instances PURPLE-PILLS-EVPN instance-type evpn
set routing-instances PURPLE-PILLS-EVPN vlan-id 110
set routing-instances PURPLE-PILLS-EVPN vrf-target target:65500:110
set routing-instances PURPLE-PILLS-EVPN protocols evpn
```

#### PE1
```
set routing-instances PURPLE-PILLS-EVPN interface ge-0/0/6.110
!
set interfaces ge-0/0/6 flexible-vlan-tagging
set interfaces ge-0/0/6 encapsulation flexible-ethernet-services
set interfaces ge-0/0/6 unit 110 encapsulation vlan-bridge
set interfaces ge-0/0/6 unit 110 vlan-id 110
```

#### PE2
```
set routing-instances PURPLE-PILLS-EVPN interface ge-0/0/9.110
!
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 110 encapsulation vlan-bridge
set interfaces ge-0/0/9 unit 110 vlan-id 110
```

### Verification
- VNI is automatically taken from VLAN-ID of Routing-Instance or what?
```
root@PE1> show route table PURPLE-PILLS-EVPN.evpn.0

PURPLE-PILLS-EVPN.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:8::110::aa:bb:cc:01:20:00/304 MAC/IP 
                   *[EVPN/170] 22:57:14
                       Indirect
2:192.168.1.2:8::110::aa:bb:cc:01:40:00/304 MAC/IP
                   *[BGP/170] 22:57:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 603393
3:192.168.1.1:8::110::192.168.1.1/248 IM
                   *[EVPN/170] 23:03:31
                       Indirect
3:192.168.1.2:8::110::192.168.1.2/248 IM
                   *[BGP/170] 05:02:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
```
## BLUE EVPN
- **L2 services on all PEs:**
  - VLAN 120 | EVPN RT=target:65500:120
- **L3 services:**
  - Anycast gateway (Manual GW Sync, IP only) on all PEs: 10.120.0.254/24 on IRB.120
- **No L3VPN**
- Make sure **P1 and P2 can exchange traffic with hosts inside the EPVN**
  - Add BLUE IRBs into OSPF
#### All PEs
```
set interfaces ge-0/0/7 flexible-vlan-tagging
set interfaces ge-0/0/7 encapsulation flexible-ethernet-services
set interfaces ge-0/0/7 unit 120 encapsulation vlan-bridge
set interfaces ge-0/0/7 unit 120 vlan-id 120
set interfaces irb.120 family inet address 10.120.0.254/24
!
set routing-instances BLUE-HUEPLET-LIMITED instance-type evpn
set routing-instances BLUE-HUEPLET-LIMITED vlan-id 120
set routing-instances BLUE-HUEPLET-LIMITED interface ge-0/0/7.120
set routing-instances BLUE-HUEPLET-LIMITED routing-interface irb.120
set routing-instances BLUE-HUEPLET-LIMITED vrf-target target:65500:120
set routing-instances BLUE-HUEPLET-LIMITED protocols evpn
!
set protocols ospf area 0.0.0.0 interface irb.120 passive
```
#### Verify OSPF reachability for BLUE servers and P1, P2:
```
BLUE_S1#show ip route
S*    0.0.0.0/0 [1/0] via 10.120.0.254
      10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
C        10.120.0.0/24 is directly connected, Ethernet0/0.120
L        10.120.0.1/32 is directly connected, Ethernet0/0.120
!
!
BLUE_S1#ping 192.168.1.5
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.1.5, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/2 ms
!
!
BLUE_S1#ping 192.168.1.6
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 192.168.1.6, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/2 ms
```

## GREEN EVPN
- **L2 services on PE1, PE2:**
  - VLAN 130 | EVPN RT=target:65500:130
- **L3 services:**
  - Anycast gateway (Manual GW Sync, IP only) on PE1 and PE2: 10.130.12.254/24 on IRB.130
  - Unicast gateway on PE3: 10.130.30.254/24 on ge-0/0/8.130
  - Unicast gateway on PE4: 10.130.40.254/24 on ge-0/0/8.130
- **L3VPN:**
  - L3VPN RT=target:65500:330
  - PE1 and PE2 - EVPN + L3VPN:
    - Interface IRB.130
  - PE3 and PE4 - L3VPN only:
    - Interface ge-0/0/8.130

- **EVPN + L3VPN config:**
  - IP address on IRB
  - GE subinterface encapsulation =  vlan-bridge
  - EVPN Routing-Instance:
    - routing-interface = IRB
    - interface = GE.SUBINT
  - L3VPN Routing-Instance:
    - interface = IRB
- **L3VPN only config:**
  - No IRB
  - IP address on GE.SUBINT
  - No GE subinterface encapsulation
  - L3VPN Routing-Instance:
    - interface = GE.SUBINT

### L2 EVPN

#### PE1 and PE2 
```
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 130 encapsulation vlan-bridge
set interfaces ge-0/0/8 unit 130 vlan-id 130
set interfaces irb.130 family inet address 10.130.12.254/24
!
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN instance-type evpn
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN vlan-id 130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN routing-interface irb.130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN interface ge-0/0/8.130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN vrf-target target:65500:130
set routing-instances GREEN-ZALUPA-INCORPORATED-EVPN protocols evpn
```
### L3 VPN
#### All PEs
```
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8 unit 130 vlan-id 130
!
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN instance-type vrf
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-target target:65500:330
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN vrf-table-label
```
#### PE1 and PE2

```
set interfaces ge-0/0/8 unit 130 encapsulation vlan-bridge
set interfaces irb unit 130 family inet address 10.130.12.254/24
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface irb.130
```

#### PE3
```
set interfaces ge-0/0/8 unit 130 family inet address 10.130.30.254/24
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface ge-0/0/8.130
```
#### PE4
```
set interfaces ge-0/0/8 unit 130 family inet address 10.130.40.254/24
set routing-instances GREEN-ZALUPA-INCORPORATED-L3VPN interface ge-0/0/8.130
```
### Verification
- **All GREEN-sites servers are mutually reachable**
```
GREEN_S1#show ip route
S*    0.0.0.0/0 [1/0] via 10.130.12.254
      10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
C        10.130.12.0/24 is directly connected, Ethernet0/0.130
L        10.130.12.1/32 is directly connected, Ethernet0/0.130
```

```
GREEN_S1#ping 10.130.12.2
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 10.130.12.2, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/2 ms
```

```
GREEN_S1#ping 10.130.30.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 10.130.30.1, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/2/3 ms
```

```
GREEN_S1#ping 10.130.40.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 10.130.40.1, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 2/2/3 ms
```

```
GREEN_S1#show ip arp
Protocol  Address          Age (min)  Hardware Addr   Type   Interface
Internet  10.130.12.1             -   aabb.cc00.e000  ARPA   Ethernet0/0.130
Internet  10.130.12.2            91   aabb.cc00.f000  ARPA   Ethernet0/0.130
Internet  10.130.12.254           1   2c6b.f580.67f0  ARPA   Ethernet0/0.130
```
- **L3VPN table on only EVPN-enabled PE1 and PE2** - no remote routes
```
root@PE1> show route table GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0
GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 2 destinations, 3 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.130.12.0/24     *[Direct/0] 00:08:40
                    >  via irb.130
                    [BGP/170] 00:08:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.130.12.254/32   *[Local/0] 00:08:40
                       Local via irb.130
```
- **L3VPN table after L3VPN enabled on all PEs** - remote /24s and /32s appeared

```
# PE1 (EVPN+L3VPN)
!
!
root@PE1> show route table GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0
GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 6 destinations, 7 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.130.12.0/24     *[Direct/0] 13:47:43
                    >  via irb.130
                    [BGP/170] 13:47:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.130.12.1/32     *[EVPN/7] 13:02:13
                    >  via irb.130
10.130.12.2/32     *[BGP/170] 13:01:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.130.12.254/32   *[Local/0] 13:47:43
                       Local via irb.130
10.130.30.0/24     *[BGP/170] 13:10:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299776(top)
10.130.40.0/24     *[BGP/170] 13:11:02, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 299824(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299792(top)
```
- **No changes in EVPN table**
```
root@PE1> show route table GREEN-ZALUPA-INCORPORATED-EVPN.evpn.0

GREEN-ZALUPA-INCORPORATED-EVPN.evpn.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:10::130::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[EVPN/170] 13:50:06
                       Indirect
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00/304 MAC/IP
                   *[EVPN/170] 13:08:49
                       Indirect
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 13:50:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00/304 MAC/IP
                   *[BGP/170] 13:08:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0::10.130.12.254/304 MAC/IP
                   *[EVPN/170] 13:50:06
                       Indirect
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00::10.130.12.1/304 MAC/IP
                   *[EVPN/170] 13:04:36
                       Indirect
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0::10.130.12.254/304 MAC/IP
                   *[BGP/170] 13:50:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00::10.130.12.2/304 MAC/IP
                   *[BGP/170] 13:04:18, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
3:192.168.1.1:10::130::192.168.1.1/248 IM
                   *[EVPN/170] 14:07:48
                       Indirect
3:192.168.1.2:10::130::192.168.1.2/248 IM
                   *[BGP/170] 13:50:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 607488
```
- **PE4 (only L3VPN)**
```
root@PE4> show route table GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0
GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 6 destinations, 7 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
10.130.12.0/24     *[BGP/170] 13:28:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299776(top)
                    [BGP/170] 13:28:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299792(top)
10.130.12.1/32     *[BGP/170] 13:02:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299792(top)
10.130.12.2/32     *[BGP/170] 13:02:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299776(top)
10.130.30.0/24     *[BGP/170] 13:11:05, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
10.130.40.0/24     *[Direct/0] 13:11:09
                    >  via ge-0/0/8.130
10.130.40.254/32   *[Local/0] 13:11:09
                       Local via ge-0/0/8.130
```
## RED EVPN
- **L2 services on PE1, PE2, PE3:**
  - VLAN 140 | EVPN RT=target:65500:140
- **L3 services:**
  - Virtual GW on PE1, PE2, PE3 IRBs:
    - PE1: PHY_IP=10.140.123.251/24 | VIP=10.140.123.254
    - PE2: PHY_IP=10.140.123.252/24 | VIP=10.140.123.254
    - PE3: PHY_IP=10.140.123.253/24 | VIP=10.140.123.254
  - Unicast gateway on PE4: 10.141.40.254/24 on ge-0/0/9.141 
    - VLANID 141
  - Do not advertise the EVPN gateway addresses:    
`set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN prot evpn default-gateway do-not-advertise`  

//RED_S2 connected to PE2 via ge-0/0/5, not ge-0/0/9!

- **L3VPN:**
  - L3VPN RT=target:65500:340
  - PE1, PE2, PE3 - EVPN + L3VPN:
    - Interface IRB.140
  - PE4 - L3VPN only:
    - Interface ge-0/0/9.140

### L2 EVPN
#### PE1, PE3
```
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 140 encapsulation vlan-bridge
set interfaces ge-0/0/9 unit 140 vlan-id 140
!
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN instance-type evpn
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN vlan-id 140
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN routing-interface irb.140
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN interface ge-0/0/9.140
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN vrf-target target:65500:140
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN prot evpn
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN prot evpn default-gateway do-not-advertise
```

#### PE1
```
set interfaces irb.140 family inet address 10.140.123.251/24 virtual-gateway-address 10.140.123.254
```
#### PE2
```
set interfaces ge-0/0/5 flexible-vlan-tagging
set interfaces ge-0/0/5 encapsulation flexible-ethernet-services
set interfaces ge-0/0/5 unit 140 encapsulation vlan-bridge
set interfaces ge-0/0/5 unit 140 vlan-id 140
set interfaces irb.140 family inet address 10.140.123.252/24 virtual-gateway-address 10.140.123.254
set routing-inst RED-CUSTOMER-HUYASTOMER-EVPN interface ge-0/0/5.140
```
#### PE3
```
set interfaces irb.140 family inet address 10.140.123.253/24 virtual-gateway-address 10.140.123.254
```
### L3 VPN
#### All PEs
```
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN instance-type vrf
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-target target:65500:340
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN vrf-table-label
```
#### PE1,PE2,PE3
```
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN interface irb.140
```
#### PE4
```
set interfaces ge-0/0/9 flexible-vlan-tagging
set interfaces ge-0/0/9 encapsulation flexible-ethernet-services
set interfaces ge-0/0/9 unit 141 vlan-id 141
set interfaces ge-0/0/9 unit 141 family inet address 10.141.40.254/24
!
set routing-instances RED-CUSTOMER-HUYASTOMER-L3VPN interface ge-0/0/9.141
```

