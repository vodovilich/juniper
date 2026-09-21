## ISP Core OSPF
- Configure **all routers** to be part of a **single area OSPF** network.
- Make sure OSPF will calculate path cost using **100 Gbps as a reference bandwidth**.
  - Junos default OSPF reference-BW is 100 Mbps
- **Advertise the loopback IP** address **into OSPF on every router**.
- Make sure the **OSPF database only contains router LSAs**
  - All OSPF links are set to P2P to eliminate Type2 Network LSAs

#### All Routers
```
set protocols ospf reference-bandwidth 100g
set protocols ospf area 0 interface lo0.0 passive
```
#### PE1
```
set routing-options router-id 192.168.1.1
set protocols ospf area 0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/5.0 interface-type p2p
```

#### PE2
```
set routing-options router-id 192.168.1.2
set protocols ospf area 0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/6.0 interface-type p2p
```

#### PE3
```
set routing-options router-id 192.168.1.3
set protocols ospf area 0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/5.0 interface-type p2p
```

#### PE4
```
set routing-options router-id 192.168.1.4
set protocols ospf area 0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/6.0 interface-type p2p
```

#### P5
```
set routing-options router-id 192.168.1.5
set protocols ospf area 0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/3.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/6.0 interface-type p2p
```

#### P6
```
set routing-options router-id 192.168.1.6
set protocols ospf area 0 interface ge-0/0/2.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/4.0 interface-type p2p
set protocols ospf area 0 interface ge-0/0/5.0 interface-type p2p
```

## ISP Core LDP
- Enable LDP neighbor relationships between all routers
- Authenticate LDP sessions using the MD5 hash 'LDPSECRET'
  - To wildcard neighbor IPs - use: `set prot ldp session-group $Lo_SUBNET authentication-key LDPSECRET`
- LDP should use the same metric as the IGP
  - Junos default LDP route metric is 1
  - To set same metric as IGP: `set protocols ldp track-igp-metric`
- The IGP should prefer links with a working LDP session
  - LDP-synchronization:
    - When LDP session is down, IGP automatically increases the IGP link cost for the interfaces:
```
set protocols ospf area 0.0.0.0 interface $INTERFACE ldp-synchronization
```

#### PE1
```
set interface ge-0/0/2.0 family mpls
set interface ge-0/0/5.0 family mpls
set protocols mpls interface ge-0/0/2.0 
set protocols mpls interface ge-0/0/5.0 
set protocols ldp interface ge-0/0/2.0 
set protocols ldp interface ge-0/0/5.0 
set protocols ospf area 0.0.0.0 interface ge-0/0/2.0 ldp-synchronization
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
```

#### PE2
```
set interface ge-0/0/1.0 family mpls
set protocols mpls interface ge-0/0/1.0
set protocols ldp interface ge-0/0/1.0
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 ldp-synchronization
!
set interface ge-0/0/6.0 family mpls
set protocols mpls interface ge-0/0/6.0
set protocols ldp interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
```

#### PE3
```
set interface ge-0/0/4.0 family mpls
set protocols mpls interface ge-0/0/4.0
set protocols ldp interface ge-0/0/4.0
set protocols ospf area 0.0.0.0 interface ge-0/0/4.0 ldp-synchronization
!
set interface ge-0/0/5.0 family mpls
set protocols mpls interface ge-0/0/5.0
set protocols ldp interface ge-0/0/5.0
set protocols ospf area 0.0.0.0 interface ge-0/0/5.0 ldp-synchronization
```

#### PE4
```
set interface ge-0/0/3.0 family mpls
set protocols mpls interface ge-0/0/3.0
set protocols ldp interface ge-0/0/3.0
set protocols ospf area 0.0.0.0 interface ge-0/0/3.0 ldp-synchronization
!
set interface ge-0/0/6.0 family mpls
set protocols mpls interface ge-0/0/6.0
set protocols ldp interface ge-0/0/6.0
set protocols ospf area 0.0.0.0 interface ge-0/0/6.0 ldp-synchronization
```

#### P5
```
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
```

#### P6
```
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
```

##### All routers
```
set protocols ldp session-group 192.168.1.0/24 authentication-key LDPSECRET
set protocols ldp track-igp-metric
```

#### Verify
- MPLS and LDP
```
root@P5> show mpls interface
Interface        State       Administrative groups (x: extended)
ge-0/0/1.0       Up         <none>
ge-0/0/3.0       Up         <none>
ge-0/0/6.0       Up         <none>
!
root@P5> show ldp interface
Interface          Address                          Label space ID   Nbr   Next
                                                                    count  hello
ge-0/0/1.0         172.16.15.0                      192.168.1.5:0     1      0
ge-0/0/3.0         172.16.35.0                      192.168.1.5:0     1      0
ge-0/0/6.0         172.16.56.0                      192.168.1.5:0     1      0
!
root@P5> show ldp session
  Address                           State       Connection  Hold time  Adv. Mode
192.168.1.1                         Operational Open          24         DU
192.168.1.3                         Operational Open          24         DU
192.168.1.6                         Operational Open          25         DU
```
- By default in Junos, LDP only advertises a label for the primary loopback interface. 
  - In addition to this, every router will also advertise a label for every received route. 
  - The end result is a full-mesh of LDP-signaled LSPs between all of the routers.
  - inet.3 table stores egress addresses for all IPv4 MPLS LSPs
```
root@PE1> show route 192.168.1.0/24 table inet.3

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.2/32     *[LDP/9] 00:02:40, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.3/32     *[LDP/9] 00:09:11, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299920
192.168.1.4/32     *[LDP/9] 00:02:40, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300000
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904
192.168.1.5/32     *[LDP/9] 00:10:22, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.6/32     *[LDP/9] 00:02:40, metric 200
                       to 172.16.12.1 via ge-0/0/2.0, Push 299984
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299888
```

- LSP PE1-PE4 walkthrough:
  - PE1 pushes 299904 and forwards via ge-0/0/5
  - P5 swaps 299904 to 299904 and forwards via ge-0/0/6
  - P6 pops 299904 and forwards via ge-0/0/4
```
root@PE1> show route 192.168.1.4 table inet.3
inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
192.168.1.4/32     *[LDP/9] 00:08:03, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300000
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904    //HERE
!
root@P5> show route label 299904
mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
299904             *[LDP/9] 00:13:22, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Swap 299856
                       to 172.16.56.1 via ge-0/0/6.0, Swap 299904    //HERE
!
root@P6> show route label 299904
mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
299904             *[LDP/9] 00:13:43, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop               //HERE
299904(S=0)        *[LDP/9] 00:13:43, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop

#299904(S=0)  - bottom-of-stack = 0, i.e. label stack detected
```
- IGP metric tracking - Before
```
root@PE1> show route protocol ldp | match metric
224.0.0.2/32       *[LDP/9] 00:37:45, metric 1
192.168.1.2/32     *[LDP/9] 00:37:40, metric 1
192.168.1.3/32     *[LDP/9] 00:32:17, metric 1
192.168.1.4/32     *[LDP/9] 00:32:06, metric 1
192.168.1.5/32     *[LDP/9] 00:32:27, metric 1
192.168.1.6/32     *[LDP/9] 00:32:16, metric 1
299776             *[LDP/9] 00:37:40, metric 1
299776(S=0)        *[LDP/9] 00:37:40, metric 1
299792             *[LDP/9] 00:32:27, metric 1
299792(S=0)        *[LDP/9] 00:32:27, metric 1
299808             *[LDP/9] 00:32:17, metric 1
299824             *[LDP/9] 00:32:06, metric 1
299840             *[LDP/9] 00:32:16, metric 1
```
- IGP metric tracking - After
```
root@PE1> show route protocol ldp | match metric
224.0.0.2/32       *[LDP/9] 00:38:09, metric 1
192.168.1.2/32     *[LDP/9] 00:00:12, metric 100
192.168.1.3/32     *[LDP/9] 00:00:12, metric 200
192.168.1.4/32     *[LDP/9] 00:00:12, metric 300
192.168.1.5/32     *[LDP/9] 00:00:12, metric 100
192.168.1.6/32     *[LDP/9] 00:00:12, metric 200
299776             *[LDP/9] 00:00:12, metric 1
299776(S=0)        *[LDP/9] 00:00:12, metric 1
299792             *[LDP/9] 00:00:12, metric 1
299792(S=0)        *[LDP/9] 00:00:12, metric 1
299808             *[LDP/9] 00:00:12, metric 1
299824             *[LDP/9] 00:00:12, metric 1
299840             *[LDP/9] 00:00:12, metric 1
```
- LDP authN - Before
```
root@P5# run show ldp session | match auth
[edit]
root@P5#
```
- LDP authN - After
```
root@P5> show ldp session detail | match auth
  Authentication type: MD5 (192.168.1.0/24)
  Authentication type: MD5 (192.168.1.0/24)
  Last down 00:03:02 ago; Reason: authentication key was changed
  Authentication type: MD5 (192.168.1.0/24)
```
- LDP Synchronization enabled:
```
root@PE1> show ospf interface extensive | match sync
  LDP sync state: in sync, for: 00:02:14, reason: LDP session up
  LDP sync state: in sync, for: 00:03:09, reason: LDP session up
```
LDP Synchronization operation:
```
# Disable LDP on PE2:
root@PE2# deactivate protocols ldp
[edit]
root@PE2# commit
!
!
#PE1 increased cost of a link with a failed LDP session:
!
root@PE1> show ospf interface ge-0/0/2.0 extensive
Interface           State   Area            DR ID           BDR ID          Nbrs
ge-0/0/2.0          PtToPt  0.0.0.0         0.0.0.0         0.0.0.0            1
  Type: P2P, Address: 172.16.12.0, Mask: 255.255.255.254, MTU: 1500, Cost: 65535
  Adj count: 1
  Hello: 10, Dead: 40, ReXmit: 5, Not Stub
  Auth type: None
  Protection type: None
  Topology default (ID 0) -> Cost: 100
  LDP sync state: in hold-down, for: 00:02:16, reason: LDP session down
           config holdtime: infinity                       //HERE
!
root@PE1> show ospf interface detail ge-0/0/2.0
Interface           State   Area            DR ID           BDR ID          Nbrs
ge-0/0/2.0          PtToPt  0.0.0.0         0.0.0.0         0.0.0.0            1
  Type: P2P, Address: 172.16.12.0, Mask: 255.255.255.254, MTU: 1500, Cost: 65535    //HERE
  Adj count: 1
  Hello: 10, Dead: 40, ReXmit: 5, Not Stub
  Auth type: None
  Protection type: None
  Topology default (ID 0) -> Cost: 100
```
## LSP options tuning
- Enable all protocols to use LDP signaled LSPs for forwarding:
`set protocols mpls traffic-engineering mpls-forwarding`

- The MPLS network should be represented as a single hop to future VPN customers:
`set protocols mpls no-propagate-ttl`

- Tunnel ICMP messages inside MPLS:
`set protocols mpls icmp-tunneling`

### Traffic engineering options
- By default Junos installs LSP NextHops into inet.3
- BGP can use inet.3 to resolve NextHop and forward traffic through LSPs
- This behavior can be altered with traffic-engineering options:
  - **traffic-engineering bgp**
    - Default
    - Only ingress routes are installed in the inet.3 table
  - **traffic-engineering bgp-igp**
    - Move inet.3 routes to the main routing-table (inet.0)
  - **traffic-engineering bgp-igp-both-ribs**
    - Copy inet.3 routes to inet.0 (VPNs require a route in the inet.3 table)
  - **traffic-engineering mpls-forwarding**
    - When routes are moved or copied to the inet.0 table, the MPLS routes can supersede the IGP routes and cause for a router to stop redistributing prefixes
    - Allowing any traffic to be forwarded via LSPs
    - LSPs are used to forward traffic but they are excluded from route selection
    - Routes are added to the inet.0 and the inet.3 table

#### All Routers
```
set protocols mpls traffic-engineering mpls-forwarding
```
#### Verification
- **Before - PE1 has routes to PE4**:
  - in inet.0 via OSPF
  - in inet.3 via LDP
```
root@PE1> show route 192.168.1.4

inet.0: 23 destinations, 23 routes (23 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
192.168.1.4/32     *[OSPF/10] 04:22:28, metric 300
                       to 172.16.12.1 via ge-0/0/2.0
                    >  to 172.16.15.0 via ge-0/0/5.0
!
inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
192.168.1.4/32     *[LDP/9] 04:22:28, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300000
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904

```
- **After - inet.3 routes added into inet.0**:
```
root@PE1> show route 192.168.1.4
inet.0: 23 destinations, 28 routes (23 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both
192.168.1.4/32     @[OSPF/10] 00:00:02, metric 300
                       to 172.16.12.1 via ge-0/0/2.0
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 00:00:02, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300000
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904
!
inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both
192.168.1.4/32     *[LDP/9] 00:00:02, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300000
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904
```

### Hiding topology via TTL manipulation
- Two options in MPLS config:
  - no-decrement-ttl
    - Proprietary
    - Works only in RSVP
    - Existing LSPs need to be cleared
    - Per-LSP or for all LSPs
    - Configured on ingress router
  - no-propagate-ttl
    - Works in both LDP and RSVP
    - Disables normal TTL decrementing on LSR
    - Effective immediately, existing LSPs do not need to be cleared
    - Needs to be configured on all routers

- Default MPLS TTL handling on Junos
  - Ingress LSR: sets MPLS_TTL = IP_TTL - 1 (minus one)
  - IP_TTL is left intact during transfer across an LSP
  - Every LSR decrements MPLS_TTL
  - Penultimate LSR during POP:
    - IP_TTL = MPLS_TTL
    - Decrements IP_TTL before sending the packet to EgressLSR
  - In summary, TTL decremented as many times as many LSRs a packet passed
- TTL handling with no-propagate-ttl option:
  - Ingress LSR: 
    - Decrements IP_TTL
    - Sets MPLS_TTL to 255
  - Every LSR along the path decrements MPLS_TTL and leaves IP_TTL intact
  - Penultimate LSR during POP:
    - MPLS_TTL is not copied into IP_TTL
    - IP_TTL is left intact and the packet is sent to EgressLSR
  - Egress LSR:
    - Decrements IP_TTL before sending the packet
  - In summary, all ISP network represented as two hops (Ingress and Egress LSRs)
#### All Routers
```
set protocols mpls no-propagate-ttl
```

#### Verification
- Before - trace from PE1 to PE4:
```
root@PE1> traceroute 192.168.1.4 source 192.168.1.1
traceroute to 192.168.1.4 (192.168.1.4) from 192.168.1.1, 30 hops max, 52 byte packets
 1  172.16.15.0 (172.16.15.0)  1.873 ms  1.608 ms  1.425 ms
     MPLS Label=299904 CoS=0 TTL=1 S=1
 2  172.16.35.1 (172.16.35.1)  2.429 ms  1.966 ms  9.935 ms
     MPLS Label=299984 CoS=0 TTL=1 S=1
 3  192.168.1.4 (192.168.1.4)  3.594 ms  2.999 ms  3.027 ms
```
- After:
```
root@PE1> traceroute 192.168.1.4 source 192.168.1.1
traceroute to 192.168.1.4 (192.168.1.4) from 192.168.1.1, 30 hops max, 52 byte packets
 1  192.168.1.4 (192.168.1.4)  3.578 ms  2.979 ms  3.052 ms
```


### Tunnel ICMP messages inside MPLS
- By default, transit LSRs that run out of TTL cannot route an ICMP "TTL Expired" message back to the trace initiator if these TransitLSRs lack an IP route for the encapsulated payload
  - TransitLSR may not have Full-View or CustomerVRF table.
- With ICMP-tunneling enabled TransitLSR **tunnels ICMP-reply along the LSP towards EgressLSR**, where the proper VRF or global routing table lookup can successfully route the message back to the source 
#### All Routers
```
set protocols mpls icmp-tunneling
```
#### Verification
- `no-propagate-ttl` needs to be disabled
- BEFORE - intermediate nodes cannot reach the traceroute initiator
```
RED-R1#traceroute 192.168.10.2
Type escape sequence to abort.
Tracing the route to 192.168.10.2
VRF info: (vrf in name/id, vrf out name/id)
  1 10.0.10.1 [AS 65500] 1 msec 0 msec 1 msec
  2  *  *  *                         //HERE
  3 172.16.35.1 [MPLS: Label 300048 Exp 0] 2 msec 2 msec 3 msec
  4 10.0.12.0 [AS 65500] 2 msec 2 msec *

```
- AFTER
```
RED-R1#traceroute 192.168.10.2
Type escape sequence to abort.
Tracing the route to 192.168.10.2
VRF info: (vrf in name/id, vrf out name/id)
  1 10.0.10.1 [AS 65500] 1 msec 0 msec 1 msec
  2 172.16.15.0 [MPLS: Labels 299920/300048 Exp 0] 3 msec 3 msec 2 msec               //HERE
  3 172.16.35.1 [MPLS: Label 300048 Exp 0] 3 msec 2 msec 2 msec
  4 10.0.12.0 [AS 65500] 3 msec 3 msec *
```
