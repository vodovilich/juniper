### PE1
```
root@PE1> show route | no-more

inet.0: 23 destinations, 28 routes (23 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[Direct/0] 2d 14:15:53
                    >  via ge-0/0/2.0
172.16.12.0/32     *[Local/0] 2d 14:15:53
                       Local via ge-0/0/2.0
172.16.15.0/31     *[Direct/0] 2d 14:15:53
                    >  via ge-0/0/5.0
172.16.15.1/32     *[Local/0] 2d 14:15:53
                       Local via ge-0/0/5.0
172.16.26.0/31     *[OSPF/10] 1d 07:46:14, metric 200
                    >  to 172.16.12.1 via ge-0/0/2.0
172.16.34.0/31     *[OSPF/10] 00:34:01, metric 300
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.35.0/31     *[OSPF/10] 1d 07:46:14, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.46.0/31     *[OSPF/10] 1d 07:46:14, metric 300
                    >  to 172.16.12.1 via ge-0/0/2.0
                       to 172.16.15.0 via ge-0/0/5.0
172.16.56.0/31     *[OSPF/10] 1d 07:46:14, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.255.1/32    *[Direct/0] 2d 11:47:20
                    >  via lo0.0
172.16.255.2/32    @[OSPF/10] 1d 07:46:14, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
                   #[LDP/9] 1d 07:46:14, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
172.16.255.3/32    @[OSPF/10] 00:34:01, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 00:34:01, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
172.16.255.4/32    @[OSPF/10] 1d 07:46:14, metric 300
                    >  to 172.16.12.1 via ge-0/0/2.0
                       to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 07:46:14, metric 300
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300416
                       to 172.16.15.0 via ge-0/0/5.0, Push 299952
172.16.255.5/32    @[OSPF/10] 1d 07:46:14, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 07:46:14, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.255.6/32    @[OSPF/10] 1d 07:46:14, metric 200
                    >  to 172.16.12.1 via ge-0/0/2.0
                       to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 07:46:14, metric 200
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300448
                       to 172.16.15.0 via ge-0/0/5.0, Push 300000
192.168.1.0/24     *[Direct/0] 05:45:56
                    >  via irb.11
192.168.1.1/32     *[EVPN/7] 05:28:37
                    >  via irb.11
192.168.1.2/32     *[EVPN/7] 05:01:31
                    >  via irb.11
192.168.1.3/32     *[EVPN/7] 01:12:10
                    >  via irb.11
192.168.1.253/32   *[Local/0] 05:45:56
                       Local via irb.11
192.168.2.0/24     *[OSPF/10] 00:34:01, metric 300
                    >  to 172.16.15.0 via ge-0/0/5.0
224.0.0.2/32       *[LDP/9] 2d 14:15:53, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 2d 14:15:53, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.2/32    *[LDP/9] 1d 07:46:14, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
172.16.255.3/32    *[LDP/9] 00:34:01, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
172.16.255.4/32    *[LDP/9] 1d 07:46:14, metric 300
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300416
                       to 172.16.15.0 via ge-0/0/5.0, Push 299952
172.16.255.5/32    *[LDP/9] 1d 07:46:14, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.255.6/32    *[LDP/9] 1d 07:46:14, metric 200
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300448
                       to 172.16.15.0 via ge-0/0/5.0, Push 300000

L3VPN-12.inet.0: 10 destinations, 15 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[Direct/0] 05:45:56
                    >  via irb.12
                    [BGP/170] 05:45:57, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.1/32     *[EVPN/7] 05:27:40
                    >  via irb.12
192.168.1.2/32     *[EVPN/7] 05:00:39
                    >  via irb.12
                    [BGP/170] 05:00:39, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.3/32     *[EVPN/7] 01:00:53
                    >  via irb.12
                    [BGP/170] 01:00:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.4/32     *[BGP/170] 05:21:34, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.253/32   *[Local/0] 05:45:56
                       Local via irb.12
192.168.2.0/24     *[BGP/170] 00:34:01, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 300016(top)
                    [BGP/170] 01:37:00, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299952(top)
192.168.2.1/32     *[BGP/170] 00:34:01, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 300016(top)
192.168.2.2/32     *[BGP/170] 00:34:01, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 300016(top)
                    [BGP/170] 00:35:23, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299952(top)
192.168.2.3/32     *[BGP/170] 01:23:44, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299952(top)

L3VPN-13.inet.0: 10 destinations, 15 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[Direct/0] 05:45:56
                    >  via irb.13
                    [BGP/170] 05:45:57, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.1/32     *[EVPN/7] 05:27:08
                    >  via irb.13
192.168.1.2/32     *[EVPN/7] 05:00:39
                    >  via irb.13
                    [BGP/170] 05:00:39, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.3/32     *[EVPN/7] 00:58:24
                    >  via irb.13
                    [BGP/170] 00:58:24, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.4/32     *[BGP/170] 05:21:34, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.254/32   *[Local/0] 05:45:56
                       Local via irb.13
192.168.2.0/24     *[BGP/170] 00:34:01, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 300016(top)
                    [BGP/170] 01:37:00, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299952(top)
192.168.2.1/32     *[BGP/170] 00:34:01, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 300016(top)
192.168.2.2/32     *[BGP/170] 00:34:01, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 300016(top)
                    [BGP/170] 00:35:24, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299952(top)
192.168.2.3/32     *[BGP/170] 01:23:44, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299952(top)

L3VPN-100200.inet.0: 6 destinations, 11 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.100.0/24   *[Direct/0] 03:59:41
                    >  via irb.100
                    [BGP/170] 03:47:34, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
192.168.100.2/32   *[EVPN/7] 03:47:33
                    >  via irb.100
                    [BGP/170] 03:47:34, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
192.168.100.3/32   *[EVPN/7] 01:13:01
                    >  via irb.100
                    [BGP/170] 02:53:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
192.168.100.253/32 *[Local/0] 03:59:41
                       Local via irb.100
192.168.200.0/24   *[BGP/170] 00:34:02, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 300016(top)
                    [BGP/170] 01:28:07, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299952(top)
192.168.200.2/32   *[BGP/170] 00:34:02, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 300016(top)
                    [BGP/170] 00:35:05, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299952(top)

mpls.0: 67 destinations, 77 routes (67 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2d 14:15:54, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2d 14:15:54, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2d 14:15:54, metric 1
                       Receive
2                  *[MPLS/0] 2d 14:15:54, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2d 14:15:54, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2d 14:15:54, metric 1
                       Receive
16                 *[VPN/0] 05:46:53
                    >  via lsi.256 (L3VPN-12), Pop
17                 *[VPN/0] 05:46:53
                    >  via lsi.257 (L3VPN-13), Pop
18                 *[VPN/0] 03:59:41
                    >  via lsi.258 (L3VPN-100200), Pop
300480             *[LDP/9] 2d 11:46:29, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Pop
300480(S=0)        *[LDP/9] 2d 11:46:29, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Pop
300512             *[LDP/9] 2d 11:44:48, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 300416
                       to 172.16.15.0 via ge-0/0/5.0, Swap 299952
300528             *[LDP/9] 2d 11:45:15, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Pop
300528(S=0)        *[LDP/9] 2d 11:45:15, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Pop
300544             *[LDP/9] 2d 11:44:58, metric 1
                       to 172.16.12.1 via ge-0/0/2.0, Swap 300448
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 300000
301264             *[EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301280             *[EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00                        :ff:dc:00:00:00:0b:00
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301344
301296             *[EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00                        :ff:dc:00:00:00:0c:00
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301376
301328             *[EVPN/7] 05:46:52, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301344             *[EVPN/7] 05:46:52, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301360             *[EVPN/7] 05:46:52, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301376             *[EVPN/7] 05:45:58, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301232
301392             *[EVPN/7] 05:45:57, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301344
301408             *[EVPN/7] 05:45:57, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301376
301424             *[EVPN/7] 05:45:57, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-IM, vlan-id 11
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301408
301440             *[EVPN/7] 05:45:57, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-IM, vlan-id 12
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301424
301456             *[EVPN/7] 05:45:57, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-IM, vlan-id 13
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301440
301472             *[EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301504             *[EVPN/7] 05:45:57, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301536             *[EVPN/7] 05:01:58, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 00:01:00                        :00:00:00:00:00:00:01
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301520
301552             *[EVPN/7] 05:02:10, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:02:08, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:02:08, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:02:08, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301584             *[EVPN/7] 02:54:48, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 00:01:00                        :00:00:00:00:00:00:02
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 302192
301696             *[EVPN/7] 05:01:58, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301520
301712             *[EVPN/7] 05:01:58, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-SH, vlan-id 11
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301536, Push 301408(top)
301728             *[EVPN/7] 05:01:58, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-SH, vlan-id 12
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301536, Push 301424(top)
301744             *[EVPN/7] 05:01:58, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-SH, vlan-id 13
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301536, Push 301440(top)
301824             *[EVPN/7] 03:59:41, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301840             *[EVPN/7] 03:47:33, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00                        :ff:dc:00:00:00:64:00
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301952
301856             *[EVPN/7] 03:58:55, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00                        :00:00:00:00:00:00:01
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301840
301872             *[EVPN/7] 03:59:37, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
                    [EVPN/7] 03:55:12, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301888             *[EVPN/7] 03:59:41, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301920             *[EVPN/7] 03:59:39, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-IM, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301936             *[EVPN/7] 03:59:09, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-IM, vlan-id 100
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301936
301952             *[EVPN/7] 03:58:55, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301840
301968             *[EVPN/7] 03:58:55, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-SH, vlan-id 100
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301536, Push 301936(top)
301984             *[EVPN/7] 03:47:34, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301792
302000             *[EVPN/7] 03:47:33, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301952
302144             *[EVPN/7] 01:13:01, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00                        :00:00:00:00:00:00:02
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 302208
302160             *[EVPN/7] 02:53:36, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:22:29, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:00:55, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 00:58:26, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
302192             *[EVPN/7] 02:53:36, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
                    [EVPN/7] 02:53:35, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
302208             *[EVPN/7] 02:54:49, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 302192
302224             *[EVPN/7] 02:54:49, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 302208
302240             *[EVPN/7] 02:54:49, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-SH, vlan-id 11
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301584, Push 301408(top)
302256             *[EVPN/7] 02:54:49, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-SH, vlan-id 12
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301584, Push 301424(top)
302272             *[EVPN/7] 02:54:49, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type                         Egress-SH, vlan-id 13
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301584, Push 301440(top)
302288             *[EVPN/7] 02:54:49, remote-pe 172.16.255.2, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-SH, vlan-id 100
                    >  to 172.16.12.1 via ge-0/0/2.0, Swap 301584, Push 301936(top)
302320             *[EVPN/7] 00:35:37, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00                        :ff:dc:00:00:00:c8:00
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 303744, Push 300016(top)
                       to 172.16.12.1 via ge-0/0/2.0, Push 301360, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 301360, Push 299952(top)
302368             *[EVPN/7] 01:28:08, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                       to 172.16.12.1 via ge-0/0/2.0, Push 301040, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301040, Push 299952(top)
302384             *[EVPN/7] 01:28:07, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                       to 172.16.12.1 via ge-0/0/2.0, Push 301360, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301360, Push 299952(top)
302400             *[EVPN/7] 01:28:07, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-IM, vlan-id 200
                       to 172.16.12.1 via ge-0/0/2.0, Push 301392, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301392, Push 299952(top)
302480             *[EVPN/7] 00:35:17, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:02:00                        :00:00:00:00:00:00:01
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301648, Push 300016(top)
                       to 172.16.12.1 via ge-0/0/2.0, Push 301680, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 301680, Push 299952(top)
302496             *[EVPN/7] 01:12:43, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 301680, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 301680, Push 299952(top)
302528             *[LDP/9] 00:34:03, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 300016
302656             *[EVPN/7] 00:34:03, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-IM, vlan-id 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301344, Push 300016(top)
302672             *[EVPN/7] 00:34:03, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301040, Push 300016(top)
302688             *[EVPN/7] 00:34:03, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 303744, Push 300016(top)
302704             *[EVPN/7] 00:34:03, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type                         Egress-MAC
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 301648, Push 300016(top)

bgp.l3vpn.0: 27 destinations, 27 routes (27 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.2:8:192.168.1.0/24
                   *[BGP/170] 05:45:59, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
172.16.255.2:8:192.168.1.2/32
                   *[BGP/170] 05:00:41, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
172.16.255.2:8:192.168.1.3/32
                   *[BGP/170] 01:00:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
172.16.255.2:8:192.168.1.4/32
                   *[BGP/170] 05:21:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
172.16.255.2:9:192.168.1.0/24
                   *[BGP/170] 05:45:59, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
172.16.255.2:9:192.168.1.2/32
                   *[BGP/170] 05:00:41, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
172.16.255.2:9:192.168.1.3/32
                   *[BGP/170] 00:58:26, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
172.16.255.2:9:192.168.1.4/32
                   *[BGP/170] 05:21:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
172.16.255.2:11:192.168.100.0/24
                   *[BGP/170] 03:47:35, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
172.16.255.2:11:192.168.100.2/32
                   *[BGP/170] 03:47:35, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
172.16.255.2:11:192.168.100.3/32
                   *[BGP/170] 02:53:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
172.16.255.3:8:192.168.2.0/24
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 300016(top)
172.16.255.3:8:192.168.2.1/32
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 300016(top)
172.16.255.3:8:192.168.2.2/32
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 300016(top)
172.16.255.3:9:192.168.2.0/24
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 300016(top)
172.16.255.3:9:192.168.2.1/32
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 300016(top)
172.16.255.3:9:192.168.2.2/32
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 300016(top)
172.16.255.3:11:192.168.200.0/24
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 300016(top)
172.16.255.3:11:192.168.200.2/32
                   *[BGP/170] 00:34:03, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 300016(top)
172.16.255.4:8:192.168.2.0/24
                   *[BGP/170] 01:37:02, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299952(top)
172.16.255.4:8:192.168.2.2/32
                   *[BGP/170] 00:35:25, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299952(top)
172.16.255.4:8:192.168.2.3/32
                   *[BGP/170] 01:23:46, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299952(top)
172.16.255.4:9:192.168.2.0/24
                   *[BGP/170] 01:37:02, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299952(top)
172.16.255.4:9:192.168.2.2/32
                   *[BGP/170] 00:35:26, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299952(top)
172.16.255.4:9:192.168.2.3/32
                   *[BGP/170] 01:23:46, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299952(top)
172.16.255.4:11:192.168.200.0/24
                   *[BGP/170] 01:28:08, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299952(top)
172.16.255.4:11:192.168.200.2/32
                   *[BGP/170] 00:35:06, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299952(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 2d 14:28:54
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 14:29:05
                       MultiRecv

bgp.evpn.0: 127 destinations, 127 routes (127 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 03:59:28
                       Indirect
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 02:53:26
                       Indirect
1:172.16.255.1:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:45:58
                       Indirect
1:172.16.255.1:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:45:58
                       Indirect
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 03:59:42
                       Indirect
1:172.16.255.1:10::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 05:02:12
                       Indirect
1:172.16.255.1:10::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:53:38
                       Indirect
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 03:59:39
                       Indirect
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:53:37
                       Indirect
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 03:58:57, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 02:54:50, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:45:59, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:45:59, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 03:47:35, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:10::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 05:02:11, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
1:172.16.255.2:10::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:55:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 03:59:08, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 635137
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:55:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 641025
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:44, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 300416
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299952
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:28:08, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300416
                       to 172.16.15.0 via ge-0/0/5.0, Push 299952
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:12:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 632577, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 632577, Push 299952(top)
2:172.16.255.1:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:10
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 05:28:40
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:01:35
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:12:14
                       Indirect
2:172.16.255.1:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:10
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 05:27:43
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:00:43
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:00:57
                       Indirect
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:10
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 05:27:11
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:00:43
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 00:58:28
                       Indirect
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 03:59:43
                       Indirect
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[EVPN/170] 03:59:43
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 03:55:14
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 03:53:30
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 02:53:38
                       Indirect
2:172.16.255.2:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627201
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 05:21:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:01:34, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:12:13, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627713
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 05:21:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:00:42, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:00:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 05:21:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:00:42, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:58:27, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 03:47:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 636929
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 03:47:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 634369
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 03:47:35, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 635137
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:13:03, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 641025
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:34:04, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:28:09, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 627457, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 627457, Push 299952(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 01:28:09, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 622337, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 299952(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:56:07, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 632577, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632577, Push 299952(top)
2:172.16.255.1:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[EVPN/170] 05:28:40
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:01:35
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:12:14
                       Indirect
2:172.16.255.1:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[EVPN/170] 05:27:43
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:00:43
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:00:57
                       Indirect
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:45:59
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[EVPN/170] 05:27:11
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:00:43
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 00:58:28
                       Indirect
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[EVPN/170] 03:59:43
                       Indirect
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[EVPN/170] 03:59:43
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[EVPN/170] 03:53:30
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[EVPN/170] 02:53:38
                       Indirect
2:172.16.255.2:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627201
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[BGP/170] 05:21:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:01:34, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:12:13, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627713
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[BGP/170] 05:21:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:00:42, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:00:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[BGP/170] 05:21:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:00:43, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 00:58:28, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 03:47:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 636929
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[BGP/170] 03:47:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 634369
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 03:47:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 635137
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 01:13:04, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 641025
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:34:05, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[BGP/170] 00:34:05, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:34:05, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 01:28:10, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 627457, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 627457, Push 299952(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[BGP/170] 01:28:10, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 622337, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 299952(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:35:07, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 632577, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 632577, Push 299952(top)
3:172.16.255.1:10::11::172.16.255.1/248 IM
                   *[EVPN/170] 05:46:55
                       Indirect
3:172.16.255.1:10::12::172.16.255.1/248 IM
                   *[EVPN/170] 05:46:55
                       Indirect
3:172.16.255.1:10::13::172.16.255.1/248 IM
                   *[EVPN/170] 05:46:55
                       Indirect
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[EVPN/170] 03:59:42
                       Indirect
3:172.16.255.2:10::11::172.16.255.2/248 IM
                   *[BGP/170] 02:55:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.2:10::12::172.16.255.2/248 IM
                   *[BGP/170] 02:55:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.2:10::13::172.16.255.2/248 IM
                   *[BGP/170] 02:55:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[BGP/170] 02:55:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[BGP/170] 00:34:05, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[BGP/170] 01:28:09, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300416
                       to 172.16.15.0 via ge-0/0/5.0, Push 299952
4:172.16.255.1:0::010000000000000001:172.16.255.1/296 ES
                   *[EVPN/170] 05:02:03
                       Indirect
4:172.16.255.1:0::010000000000000002:172.16.255.1/296 ES
                   *[EVPN/170] 02:53:28
                       Indirect
4:172.16.255.2:0::010000000000000001:172.16.255.2/296 ES
                   *[BGP/170] 05:02:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
4:172.16.255.2:0::010000000000000002:172.16.255.2/296 ES
                   *[BGP/170] 02:54:52, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0

ASSVILLE-EVPN-VLAN-AWARE.evpn.0: 73 destinations, 73 routes (73 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:10::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 05:02:13
                       Indirect
1:172.16.255.1:10::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:53:39
                       Indirect
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 03:58:58, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 02:54:51, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:46:00, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:10::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 05:02:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
1:172.16.255.2:10::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:55:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.1:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:11
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 05:28:41
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:01:36
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:12:15
                       Indirect
2:172.16.255.1:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:11
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 05:27:44
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:00:44
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:00:58
                       Indirect
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:11
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 05:27:12
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:00:44
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 00:58:29
                       Indirect
2:172.16.255.2:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:46:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627201
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 05:46:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 05:21:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:01:35, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:12:14, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:46:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627713
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 05:46:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 05:21:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:00:43, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:00:57, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 05:46:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 05:21:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:00:43, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:58:28, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.1:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[EVPN/170] 05:28:41
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:01:36
                       Indirect
2:172.16.255.1:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:12:15
                       Indirect
2:172.16.255.1:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[EVPN/170] 05:27:44
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:00:44
                       Indirect
2:172.16.255.1:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:00:58
                       Indirect
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:46:00
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[EVPN/170] 05:27:13
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:00:45
                       Indirect
2:172.16.255.1:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 00:58:30
                       Indirect
2:172.16.255.2:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:46:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627201
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[BGP/170] 05:46:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[BGP/170] 05:21:39, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:01:36, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:12:15, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:46:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 627713
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[BGP/170] 05:46:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[BGP/170] 05:21:39, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:00:44, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:00:58, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:46:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[BGP/170] 05:21:39, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 625409
2:172.16.255.2:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:00:44, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 630017
2:172.16.255.2:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 00:58:29, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 640769
3:172.16.255.1:10::11::172.16.255.1/248 IM
                   *[EVPN/170] 05:46:56
                       Indirect
3:172.16.255.1:10::12::172.16.255.1/248 IM
                   *[EVPN/170] 05:46:56
                       Indirect
3:172.16.255.1:10::13::172.16.255.1/248 IM
                   *[EVPN/170] 05:46:56
                       Indirect
3:172.16.255.2:10::11::172.16.255.2/248 IM
                   *[BGP/170] 02:55:13, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.2:10::12::172.16.255.2/248 IM
                   *[BGP/170] 02:55:13, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.2:10::13::172.16.255.2/248 IM
                   *[BGP/170] 02:55:13, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0

__default_evpn__.evpn.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 03:59:30
                       Indirect
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 02:53:28
                       Indirect
1:172.16.255.1:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:46:00
                       Indirect
1:172.16.255.1:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:46:00
                       Indirect
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 03:59:44
                       Indirect
4:172.16.255.1:0::010000000000000001:172.16.255.1/296 ES
                   *[EVPN/170] 05:02:04
                       Indirect
4:172.16.255.1:0::010000000000000002:172.16.255.1/296 ES
                   *[EVPN/170] 02:53:29
                       Indirect
4:172.16.255.2:0::010000000000000001:172.16.255.2/296 ES
                   *[BGP/170] 05:02:03, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
4:172.16.255.2:0::010000000000000002:172.16.255.2/296 ES
                   *[BGP/170] 02:54:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0

ASSVILLE-EVPN-VLAN-BASED.evpn.0: 47 destinations, 47 routes (47 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 03:59:41
                       Indirect
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:53:39
                       Indirect
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 03:58:59, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 02:54:52, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 03:47:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 03:59:10, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 635137
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:55:03, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 641025
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:46, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 300416
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299952
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:28:10, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300416
                       to 172.16.15.0 via ge-0/0/5.0, Push 299952
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:12:57, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 632577, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 632577, Push 299952(top)
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 03:59:45
                       Indirect
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[EVPN/170] 03:59:45
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 03:55:16
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 03:53:32
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 02:53:40
                       Indirect
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 03:47:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 636929
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 03:47:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 634369
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 03:47:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 635137
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:13:05, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 641025
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:28:11, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 627457, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 627457, Push 299952(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 01:28:11, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 622337, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 299952(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:56:09, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 632577, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632577, Push 299952(top)
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[EVPN/170] 03:59:45
                       Indirect
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[EVPN/170] 03:59:45
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[EVPN/170] 03:53:32
                       Indirect
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[EVPN/170] 02:53:40
                       Indirect
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 03:47:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 636929
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[BGP/170] 03:47:38, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 634369
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 03:47:37, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 635137
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 01:13:05, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 641025
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 01:28:11, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 627457, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 627457, Push 299952(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[BGP/170] 01:28:11, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 622337, Push 300416(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 622337, Push 299952(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:35:08, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 632577, Push 300416(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 632577, Push 299952(top)
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[EVPN/170] 03:59:43
                       Indirect
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[BGP/170] 02:55:13, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[BGP/170] 00:34:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300016
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[BGP/170] 01:28:10, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300416
                       to 172.16.15.0 via ge-0/0/5.0, Push 299952
```
### PE2
```
root@PE2> show route | no-more

inet.0: 23 destinations, 28 routes (23 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[Direct/0] 2d 14:17:04
                    >  via ge-0/0/1.0
172.16.12.1/32     *[Local/0] 2d 14:17:04
                       Local via ge-0/0/1.0
172.16.15.0/31     *[OSPF/10] 1d 07:47:21, metric 200
                    >  to 172.16.12.0 via ge-0/0/1.0
172.16.26.0/31     *[Direct/0] 2d 14:17:04
                    >  via ge-0/0/6.0
172.16.26.1/32     *[Local/0] 2d 14:17:04
                       Local via ge-0/0/6.0
172.16.34.0/31     *[OSPF/10] 2d 11:45:54, metric 300
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.35.0/31     *[OSPF/10] 1d 07:47:21, metric 300
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.46.0/31     *[OSPF/10] 2d 11:45:54, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.56.0/31     *[OSPF/10] 2d 11:45:54, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.255.1/32    @[OSPF/10] 2d 11:47:25, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
                   #[LDP/9] 2d 11:47:25, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
172.16.255.2/32    *[Direct/0] 2d 11:47:37
                    >  via lo0.0
172.16.255.3/32    @[OSPF/10] 00:35:09, metric 300
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 00:35:09, metric 300
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302528
                       to 172.16.26.0 via ge-0/0/6.0, Push 300016
172.16.255.4/32    @[OSPF/10] 2d 11:45:54, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 2d 11:45:54, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
172.16.255.5/32    @[OSPF/10] 1d 07:47:21, metric 200
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 07:47:21, metric 200
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300528
                       to 172.16.26.0 via ge-0/0/6.0, Push 299968
172.16.255.6/32    @[OSPF/10] 2d 11:45:54, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 2d 11:45:54, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0
192.168.1.0/24     *[Direct/0] 05:47:05
                    >  via irb.11
192.168.1.2/32     *[EVPN/7] 05:02:38
                    >  via irb.11
192.168.1.3/32     *[EVPN/7] 01:13:18
                    >  via irb.11
192.168.1.4/32     *[EVPN/7] 05:22:41
                    >  via irb.11
192.168.1.252/32   *[Local/0] 05:47:05
                       Local via irb.11
192.168.2.0/24     *[OSPF/10] 01:38:07, metric 300
                    >  to 172.16.26.0 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 2d 14:17:04, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 2d 14:17:04, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1/32    *[LDP/9] 2d 11:47:25, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
172.16.255.3/32    *[LDP/9] 00:35:09, metric 300
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302528
                       to 172.16.26.0 via ge-0/0/6.0, Push 300016
172.16.255.4/32    *[LDP/9] 2d 11:45:54, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
172.16.255.5/32    *[LDP/9] 1d 07:47:21, metric 200
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300528
                       to 172.16.26.0 via ge-0/0/6.0, Push 299968
172.16.255.6/32    *[LDP/9] 2d 11:45:54, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0

L3VPN-12.inet.0: 10 destinations, 15 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[Direct/0] 05:47:05
                    >  via irb.12
                    [BGP/170] 05:47:03, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.1/32     *[BGP/170] 05:28:47, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.2/32     *[EVPN/7] 05:01:46
                    >  via irb.12
                    [BGP/170] 05:01:47, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.3/32     *[EVPN/7] 01:02:00
                    >  via irb.12
                    [BGP/170] 01:02:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.4/32     *[EVPN/7] 05:22:41
                    >  via irb.12
192.168.1.252/32   *[Local/0] 05:47:05
                       Local via irb.12
192.168.2.0/24     *[BGP/170] 01:38:07, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299936(top)
                    [BGP/170] 00:36:43, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300016(top)
192.168.2.1/32     *[BGP/170] 00:36:43, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300016(top)
192.168.2.2/32     *[BGP/170] 00:36:30, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299936(top)
                    [BGP/170] 00:36:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300016(top)
192.168.2.3/32     *[BGP/170] 01:24:51, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299936(top)

L3VPN-13.inet.0: 10 destinations, 15 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[Direct/0] 05:47:05
                    >  via irb.13
                    [BGP/170] 05:47:03, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
192.168.1.1/32     *[BGP/170] 05:28:15, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
192.168.1.2/32     *[EVPN/7] 05:01:46
                    >  via irb.13
                    [BGP/170] 05:01:47, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
192.168.1.3/32     *[EVPN/7] 00:59:31
                    >  via irb.13
                    [BGP/170] 00:59:32, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
192.168.1.4/32     *[EVPN/7] 05:22:41
                    >  via irb.13
192.168.1.254/32   *[Local/0] 05:47:05
                       Local via irb.13
192.168.2.0/24     *[BGP/170] 01:38:07, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299936(top)
                    [BGP/170] 00:36:43, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300016(top)
192.168.2.1/32     *[BGP/170] 00:36:43, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300016(top)
192.168.2.2/32     *[BGP/170] 00:36:31, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299936(top)
                    [BGP/170] 00:36:32, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300016(top)
192.168.2.3/32     *[BGP/170] 01:24:51, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299936(top)

L3VPN-100200.inet.0: 6 destinations, 11 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.100.0/24   *[Direct/0] 03:48:41
                    >  via irb.100
                    [BGP/170] 04:00:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
192.168.100.2/32   *[EVPN/7] 03:48:40
                    >  via irb.100
                    [BGP/170] 03:54:35, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
192.168.100.3/32   *[EVPN/7] 01:14:08
                    >  via irb.100
                    [BGP/170] 02:54:43, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
192.168.100.252/32 *[Local/0] 03:48:41
                       Local via irb.100
192.168.200.0/24   *[BGP/170] 01:29:14, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299936(top)
                    [BGP/170] 00:36:44, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300016(top)
192.168.200.2/32   *[BGP/170] 00:36:12, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299936(top)
                    [BGP/170] 00:36:12, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300016(top)

mpls.0: 67 destinations, 77 routes (67 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2d 14:17:05, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2d 14:17:05, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2d 14:17:05, metric 1
                       Receive
2                  *[MPLS/0] 2d 14:17:05, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2d 14:17:05, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2d 14:17:05, metric 1
                       Receive
16                 *[VPN/0] 05:47:06
                    >  via lsi.256 (L3VPN-12), Pop
17                 *[VPN/0] 05:47:06
                    >  via lsi.257 (L3VPN-13), Pop
18                 *[VPN/0] 04:00:18
                    >  via lsi.258 (L3VPN-100200), Pop
300304             *[LDP/9] 2d 11:47:36, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Pop
300304(S=0)        *[LDP/9] 2d 11:47:36, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Pop
300416             *[LDP/9] 2d 11:45:55, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 299936
300432             *[LDP/9] 1d 07:47:22, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 300528
                       to 172.16.26.0 via ge-0/0/6.0, Swap 299968
300448             *[LDP/9] 2d 11:46:05, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Pop
300448(S=0)        *[LDP/9] 2d 11:46:05, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Pop
301232             *[EVPN/7] 05:47:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:47:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:47:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301248             *[EVPN/7] 05:47:03, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:0b:00
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301472
301264             *[EVPN/7] 05:47:03, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:0c:00
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301504
301296             *[EVPN/7] 05:47:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 13
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301360
301312             *[EVPN/7] 05:47:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 11
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301328
301328             *[EVPN/7] 05:47:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 12
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301344
301344             *[EVPN/7] 05:47:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301376             *[EVPN/7] 05:47:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301408             *[EVPN/7] 05:47:04, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301424             *[EVPN/7] 05:47:04, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301440             *[EVPN/7] 05:47:04, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301456             *[EVPN/7] 05:47:04, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301264
301472             *[EVPN/7] 05:47:03, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301472
301488             *[EVPN/7] 05:47:03, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301504
301504             *[EVPN/7] 05:03:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:01
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301552
301520             *[EVPN/7] 05:03:17, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:02:39, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:01:47, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 05:01:47, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
301552             *[EVPN/7] 02:54:31, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:02
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302160
301664             *[EVPN/7] 05:03:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301552
301680             *[EVPN/7] 05:03:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 11
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 301568, Push 301328(top)
301696             *[EVPN/7] 05:03:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 12
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 301568, Push 301344(top)
301712             *[EVPN/7] 05:03:06, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 13
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 301568, Push 301360(top)
301792             *[EVPN/7] 03:48:41, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301808             *[EVPN/7] 04:00:18, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:64:00
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301888
301824             *[EVPN/7] 04:00:18, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:01
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301872
301840             *[EVPN/7] 04:00:14, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
                    [EVPN/7] 03:48:40, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301856             *[EVPN/7] 04:00:18, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301872
301872             *[EVPN/7] 04:00:18, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301888
301888             *[EVPN/7] 04:00:18, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301824
301904             *[EVPN/7] 04:00:18, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 100
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301920
301920             *[EVPN/7] 04:00:18, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-SH, vlan-id 100
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 301568, Push 301920(top)
301936             *[EVPN/7] 04:00:17, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-IM, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
301952             *[EVPN/7] 03:48:41, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
302176             *[EVPN/7] 01:14:08, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:02
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302192
302192             *[EVPN/7] 02:56:06, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:13:19, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:02:01, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 00:59:32, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table ASSVILLE-EVPN-VLAN-AWARE.evpn-mac.0
302208             *[EVPN/7] 02:56:06, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-Aliasing
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
                    [EVPN/7] 01:14:08, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 100
                       to table ASSVILLE-EVPN-VLAN-BASED.evpn-mac.0
302272             *[EVPN/7] 02:54:31, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302160
302288             *[EVPN/7] 02:54:31, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302192
302304             *[EVPN/7] 02:54:31, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 11
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 302176, Push 301328(top)
302320             *[EVPN/7] 02:54:31, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 12
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 302176, Push 301344(top)
302336             *[EVPN/7] 02:54:31, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 13
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 302176, Push 301360(top)
302352             *[EVPN/7] 02:54:31, remote-pe 172.16.255.1, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-SH, vlan-id 100
                    >  to 172.16.12.0 via ge-0/0/1.0, Swap 302176, Push 301920(top)
302384             *[EVPN/7] 00:36:43, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:c8:00
                       to 172.16.12.0 via ge-0/0/1.0, Push 303744, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 303744, Push 300016(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 301360, Push 299936(top)
302432             *[EVPN/7] 01:29:14, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 301040, Push 299936(top)
302448             *[EVPN/7] 01:29:13, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 301360, Push 299936(top)
302464             *[EVPN/7] 01:29:13, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 301392, Push 299936(top)
302544             *[EVPN/7] 00:36:23, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:02:00:00:00:00:00:00:00:01
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301648, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 301648, Push 300016(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 301680, Push 299936(top)
302560             *[EVPN/7] 01:13:49, remote-pe 172.16.255.4, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 301680, Push 299936(top)
302592             *[LDP/9] 00:35:10, metric 1
                       to 172.16.12.0 via ge-0/0/1.0, Swap 302528
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 300016
302720             *[EVPN/7] 00:36:44, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 200
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301344, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 301344, Push 300016(top)
302736             *[EVPN/7] 00:36:44, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301040, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 301040, Push 300016(top)
302752             *[EVPN/7] 00:36:43, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 303744, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 303744, Push 300016(top)
302768             *[EVPN/7] 00:36:24, remote-pe 172.16.255.3, routing-instance ASSVILLE-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 301648, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 301648, Push 300016(top)

bgp.l3vpn.0: 27 destinations, 27 routes (27 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1:8:192.168.1.0/24
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
172.16.255.1:8:192.168.1.1/32
                   *[BGP/170] 05:28:49, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
172.16.255.1:8:192.168.1.2/32
                   *[BGP/170] 05:01:49, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
172.16.255.1:8:192.168.1.3/32
                   *[BGP/170] 01:02:03, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
172.16.255.1:9:192.168.1.0/24
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
172.16.255.1:9:192.168.1.1/32
                   *[BGP/170] 05:28:17, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
172.16.255.1:9:192.168.1.2/32
                   *[BGP/170] 05:01:49, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
172.16.255.1:9:192.168.1.3/32
                   *[BGP/170] 00:59:34, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
172.16.255.1:11:192.168.100.0/24
                   *[BGP/170] 04:00:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
172.16.255.1:11:192.168.100.2/32
                   *[BGP/170] 03:54:36, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
172.16.255.1:11:192.168.100.3/32
                   *[BGP/170] 02:54:44, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
172.16.255.3:8:192.168.2.0/24
                   *[BGP/170] 00:36:45, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300016(top)
172.16.255.3:8:192.168.2.1/32
                   *[BGP/170] 00:36:45, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300016(top)
172.16.255.3:8:192.168.2.2/32
                   *[BGP/170] 00:36:33, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300016(top)
172.16.255.3:9:192.168.2.0/24
                   *[BGP/170] 00:36:45, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300016(top)
172.16.255.3:9:192.168.2.1/32
                   *[BGP/170] 00:36:45, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300016(top)
172.16.255.3:9:192.168.2.2/32
                   *[BGP/170] 00:36:34, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300016(top)
172.16.255.3:11:192.168.200.0/24
                   *[BGP/170] 00:36:45, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300016(top)
172.16.255.3:11:192.168.200.2/32
                   *[BGP/170] 00:36:13, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300016(top)
172.16.255.4:8:192.168.2.0/24
                   *[BGP/170] 01:38:09, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299936(top)
172.16.255.4:8:192.168.2.2/32
                   *[BGP/170] 00:36:32, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299936(top)
172.16.255.4:8:192.168.2.3/32
                   *[BGP/170] 01:24:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299936(top)
172.16.255.4:9:192.168.2.0/24
                   *[BGP/170] 01:38:09, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299936(top)
172.16.255.4:9:192.168.2.2/32
                   *[BGP/170] 00:36:33, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299936(top)
172.16.255.4:9:192.168.2.3/32
                   *[BGP/170] 01:24:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299936(top)
172.16.255.4:11:192.168.200.0/24
                   *[BGP/170] 01:29:15, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299936(top)
172.16.255.4:11:192.168.200.2/32
                   *[BGP/170] 00:36:13, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299936(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 2d 14:30:03
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 14:30:14
                       MultiRecv

bgp.evpn.0: 127 destinations, 127 routes (127 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 04:00:34, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 02:54:32, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:47:04, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:47:04, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 04:00:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:10::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 05:03:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
1:172.16.255.1:10::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:54:43, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 04:00:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:54:43, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640769
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 04:00:04
                       Indirect
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 02:55:56
                       Indirect
1:172.16.255.2:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:47:06
                       Indirect
1:172.16.255.2:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:47:06
                       Indirect
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 03:48:41
                       Indirect
1:172.16.255.2:10::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 05:03:18
                       Indirect
1:172.16.255.2:10::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:56:07
                       Indirect
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 04:00:15
                       Indirect
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:56:07
                       Indirect
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:24, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 302528
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300016
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:44, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302528
                       to 172.16.26.0 via ge-0/0/6.0, Push 300016
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:36:35, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:13:50, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:29:14, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:14:01, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632577, Push 299936(top)
2:172.16.255.1:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629249
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 05:03:16, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 05:29:46, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:02:40, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:13:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629761
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 05:03:16, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 05:28:49, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:01:49, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:02:03, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 05:47:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 05:03:16, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 05:28:17, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:01:49, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:59:34, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 04:00:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635905
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 04:00:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 634881
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 03:56:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 03:54:36, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 02:54:44, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640769
2:172.16.255.2:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:47:07
                       Indirect
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[EVPN/170] 05:47:07
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 05:22:43
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:40
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:13:21
                       Indirect
2:172.16.255.2:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 05:22:44
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:01:49
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:02:03
                       Indirect
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 05:22:44
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:01:49
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 00:59:34
                       Indirect
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 03:48:43
                       Indirect
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[EVPN/170] 03:48:43
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 03:48:42
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:14:10
                       Indirect
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:36:46, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 665601, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:36:46, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 622337, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:36:36, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:36:14, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:29:16, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 627457, Push 299936(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 01:29:16, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 299936(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:57:14, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632577, Push 299936(top)
2:172.16.255.1:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629249
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[BGP/170] 05:29:47, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:02:41, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:13:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629761
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[BGP/170] 05:28:50, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:01:50, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:02:04, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[BGP/170] 05:28:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:01:50, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 00:59:35, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 04:00:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635905
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[BGP/170] 04:00:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 634881
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 03:54:37, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 02:54:45, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640769
2:172.16.255.2:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[EVPN/170] 05:22:44
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:02:41
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:13:21
                       Indirect
2:172.16.255.2:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[EVPN/170] 05:22:44
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:01:49
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:02:03
                       Indirect
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:47:08
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[EVPN/170] 05:22:44
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:01:49
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 00:59:34
                       Indirect
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[EVPN/170] 03:48:43
                       Indirect
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[EVPN/170] 03:48:43
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[EVPN/170] 03:48:42
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[EVPN/170] 01:14:10
                       Indirect
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:36:46, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 665601, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[BGP/170] 00:36:46, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 622337, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:36:14, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 01:29:16, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 627457, Push 299936(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[BGP/170] 01:29:16, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 299936(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:36:13, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632577, Push 299936(top)
3:172.16.255.1:10::11::172.16.255.1/248 IM
                   *[BGP/170] 02:56:28, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.1:10::12::172.16.255.1/248 IM
                   *[BGP/170] 02:56:28, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.1:10::13::172.16.255.1/248 IM
                   *[BGP/170] 02:56:28, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[BGP/170] 02:56:28, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.2:10::11::172.16.255.2/248 IM
                   *[EVPN/170] 05:47:06
                       Indirect
3:172.16.255.2:10::12::172.16.255.2/248 IM
                   *[EVPN/170] 05:47:06
                       Indirect
3:172.16.255.2:10::13::172.16.255.2/248 IM
                   *[EVPN/170] 05:47:06
                       Indirect
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[EVPN/170] 04:00:19
                       Indirect
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[BGP/170] 00:36:46, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302528
                       to 172.16.26.0 via ge-0/0/6.0, Push 300016
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[BGP/170] 01:29:15, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
4:172.16.255.1:0::010000000000000001:172.16.255.1/296 ES
                   *[BGP/170] 05:03:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
4:172.16.255.1:0::010000000000000002:172.16.255.1/296 ES
                   *[BGP/170] 02:54:34, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
4:172.16.255.2:0::010000000000000001:172.16.255.2/296 ES
                   *[EVPN/170] 05:03:09
                       Indirect
4:172.16.255.2:0::010000000000000002:172.16.255.2/296 ES
                   *[EVPN/170] 02:55:58
                       Indirect

ASSVILLE-EVPN-VLAN-AWARE.evpn.0: 73 destinations, 73 routes (73 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 04:00:36, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 02:54:34, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 05:47:06, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:10::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 05:03:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
1:172.16.255.1:10::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:54:45, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
1:172.16.255.2:10::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 05:03:20
                       Indirect
1:172.16.255.2:10::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:56:09
                       Indirect
2:172.16.255.1:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629249
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 05:03:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 05:29:48, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:02:42, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:13:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629761
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 05:03:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 05:28:51, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:01:51, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:02:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 05:03:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 05:28:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 05:01:51, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:59:36, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.2:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 05:22:45
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:02:42
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:13:22
                       Indirect
2:172.16.255.2:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 05:22:45
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:01:50
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:02:04
                       Indirect
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 05:22:45
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 05:01:50
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 00:59:35
                       Indirect
2:172.16.255.1:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629249
2:172.16.255.1:10::11::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[BGP/170] 05:29:48, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:02:42, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:13:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 629761
2:172.16.255.1:10::12::2c:6b:f5:fe:aa:f0::192.168.1.253/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[BGP/170] 05:28:51, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:01:51, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 01:02:05, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.1:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[BGP/170] 05:47:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:00:b0:00::192.168.1.1/304 MAC/IP
                   *[BGP/170] 05:28:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 625921
2:172.16.255.1:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[BGP/170] 05:01:51, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 630529
2:172.16.255.1:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[BGP/170] 00:59:36, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640257
2:172.16.255.2:10::11::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::11::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[EVPN/170] 05:22:45
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:02:42
                       Indirect
2:172.16.255.2:10::11::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:13:22
                       Indirect
2:172.16.255.2:10::12::00:00:5e:00:01:01::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::12::2c:6b:f5:7e:74:f0::192.168.1.252/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[EVPN/170] 05:22:45
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:01:50
                       Indirect
2:172.16.255.2:10::12::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 01:02:04
                       Indirect
2:172.16.255.2:10::13::aa:aa:aa:aa:aa:aa::192.168.1.254/304 MAC/IP
                   *[EVPN/170] 05:47:09
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:00:80:00::192.168.1.4/304 MAC/IP
                   *[EVPN/170] 05:22:45
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:80:70:00::192.168.1.2/304 MAC/IP
                   *[EVPN/170] 05:01:50
                       Indirect
2:172.16.255.2:10::13::aa:bb:cc:81:30:00::192.168.1.3/304 MAC/IP
                   *[EVPN/170] 00:59:35
                       Indirect
3:172.16.255.1:10::11::172.16.255.1/248 IM
                   *[BGP/170] 02:56:29, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.1:10::12::172.16.255.1/248 IM
                   *[BGP/170] 02:56:29, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.1:10::13::172.16.255.1/248 IM
                   *[BGP/170] 02:56:29, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.2:10::11::172.16.255.2/248 IM
                   *[EVPN/170] 05:47:07
                       Indirect
3:172.16.255.2:10::12::172.16.255.2/248 IM
                   *[EVPN/170] 05:47:07
                       Indirect
3:172.16.255.2:10::13::172.16.255.2/248 IM
                   *[EVPN/170] 05:47:07
                       Indirect

__default_evpn__.evpn.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 04:00:07
                       Indirect
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 02:55:59
                       Indirect
1:172.16.255.2:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:47:09
                       Indirect
1:172.16.255.2:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 05:47:09
                       Indirect
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 03:48:44
                       Indirect
4:172.16.255.1:0::010000000000000001:172.16.255.1/296 ES
                   *[BGP/170] 05:03:11, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
4:172.16.255.1:0::010000000000000002:172.16.255.1/296 ES
                   *[BGP/170] 02:54:36, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
4:172.16.255.2:0::010000000000000001:172.16.255.2/296 ES
                   *[EVPN/170] 05:03:11
                       Indirect
4:172.16.255.2:0::010000000000000002:172.16.255.2/296 ES
                   *[EVPN/170] 02:56:00
                       Indirect

ASSVILLE-EVPN-VLAN-BASED.evpn.0: 47 destinations, 47 routes (47 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 02:54:35, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 02:54:46, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640769
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 04:00:18
                       Indirect
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 02:56:10
                       Indirect
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:27, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 302528
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300016
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:47, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302528
                       to 172.16.26.0 via ge-0/0/6.0, Push 300016
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:36:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:13:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:29:17, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:14:04, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632577, Push 299936(top)
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635905
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 634881
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 03:56:23, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 03:54:39, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 02:54:47, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640769
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 03:48:45
                       Indirect
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[EVPN/170] 03:48:45
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 03:48:44
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[EVPN/170] 01:14:12
                       Indirect
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:36:48, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 665601, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:36:48, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 622337, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:36:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:36:16, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:29:18, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 627457, Push 299936(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 01:29:18, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 299936(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:57:16, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632577, Push 299936(top)
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635905
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[BGP/170] 04:00:22, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 634881
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 03:54:39, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 635649
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 02:54:47, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 640769
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[EVPN/170] 03:48:45
                       Indirect
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[EVPN/170] 03:48:45
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[EVPN/170] 03:48:44
                       Indirect
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[EVPN/170] 01:14:12
                       Indirect
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:36:48, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 665601, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 665601, Push 300016(top)
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[BGP/170] 00:36:48, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 622337, Push 302528(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 300016(top)
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:36:16, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 632065, Push 302528(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 632065, Push 300016(top)
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 01:29:18, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 627457, Push 299936(top)
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[BGP/170] 01:29:18, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 622337, Push 299936(top)
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:36:15, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 632577, Push 299936(top)
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[BGP/170] 02:56:30, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[EVPN/170] 04:00:21
                       Indirect
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[BGP/170] 00:36:48, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 302528
                       to 172.16.26.0 via ge-0/0/6.0, Push 300016
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[BGP/170] 01:29:17, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299936
```
### PE3
```
root@PE3> show route | no-more

inet.0: 23 destinations, 29 routes (23 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 00:36:17, metric 300
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.15.0/31     *[OSPF/10] 00:36:17, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.26.0/31     *[OSPF/10] 00:36:17, metric 300
                    >  to 172.16.34.1 via ge-0/0/4.0
                       to 172.16.35.0 via ge-0/0/5.0
172.16.34.0/31     *[Direct/0] 00:46:25
                    >  via ge-0/0/4.0
172.16.34.0/32     *[Local/0] 00:46:25
                       Local via ge-0/0/4.0
172.16.35.0/31     *[Direct/0] 00:36:28
                    >  via ge-0/0/5.0
172.16.35.1/32     *[Local/0] 00:36:28
                       Local via ge-0/0/5.0
172.16.46.0/31     *[OSPF/10] 00:46:14, metric 200
                    >  to 172.16.34.1 via ge-0/0/4.0
172.16.56.0/31     *[OSPF/10] 00:36:17, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.255.1/32    @[OSPF/10] 00:36:17, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 00:36:17, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
172.16.255.2/32    @[OSPF/10] 00:36:17, metric 300
                    >  to 172.16.34.1 via ge-0/0/4.0
                       to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 00:36:17, metric 300
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299968
                       to 172.16.35.0 via ge-0/0/5.0, Push 299936
172.16.255.3/32    *[Direct/0] 2d 11:48:16
                    >  via lo0.0
172.16.255.4/32    @[OSPF/10] 00:46:14, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
                   #[LDP/9] 00:46:14, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
172.16.255.5/32    @[OSPF/10] 00:36:17, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 00:36:17, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.255.6/32    @[OSPF/10] 00:36:17, metric 200
                    >  to 172.16.34.1 via ge-0/0/4.0
                       to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 00:36:17, metric 200
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300000
                       to 172.16.35.0 via ge-0/0/5.0, Push 300000
192.168.1.0/24     *[OSPF/10] 00:36:17, metric 300
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.2.0/24     *[Direct/0] 01:39:14
                    >  via irb.11
                    [Direct/0] 01:39:14
                    >  via irb.11
192.168.2.1/32     *[EVPN/7] 01:26:21
                    >  via irb.11
192.168.2.2/32     *[EVPN/7] 00:37:41
                    >  via irb.11
192.168.2.252/32   *[Local/0] 01:39:14
                       Local via irb.11
192.168.2.253/32   *[Local/0] 01:39:14
                       Local via irb.11
224.0.0.2/32       *[LDP/9] 2d 14:18:14, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 2d 14:18:14, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1/32    *[LDP/9] 00:36:17, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
172.16.255.2/32    *[LDP/9] 00:36:17, metric 300
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299968
                       to 172.16.35.0 via ge-0/0/5.0, Push 299936
172.16.255.4/32    *[LDP/9] 00:46:14, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
172.16.255.5/32    *[LDP/9] 00:36:17, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.255.6/32    *[LDP/9] 00:36:17, metric 200
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300000
                       to 172.16.35.0 via ge-0/0/5.0, Push 300000

L3VPN-12.inet.0: 11 destinations, 17 routes (11 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[BGP/170] 00:36:17, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
                    [BGP/170] 00:37:52, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
192.168.1.1/32     *[BGP/170] 00:36:17, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
192.168.1.2/32     *[BGP/170] 00:36:17, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
                    [BGP/170] 00:37:52, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
192.168.1.3/32     *[BGP/170] 00:36:17, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
                    [BGP/170] 00:37:52, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
192.168.1.4/32     *[BGP/170] 00:37:52, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
192.168.2.0/24     *[Direct/0] 01:39:14
                    >  via irb.12
                    [Direct/0] 01:39:14
                    >  via irb.12
                    [BGP/170] 00:37:52, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.2.1/32     *[EVPN/7] 01:26:21
                    >  via irb.12
192.168.2.2/32     *[EVPN/7] 00:37:39
                    >  via irb.12
                    [BGP/170] 00:37:39, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.2.3/32     *[BGP/170] 00:37:52, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.2.252/32   *[Local/0] 01:39:14
                       Local via irb.12
192.168.2.253/32   *[Local/0] 01:39:14
                       Local via irb.12

L3VPN-13.inet.0: 10 destinations, 15 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.1.1/32     *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
192.168.1.2/32     *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.1.3/32     *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.1.4/32     *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.2.0/24     *[Direct/0] 01:39:15
                    >  via irb.13
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
192.168.2.1/32     *[EVPN/7] 01:26:22
                    >  via irb.13
192.168.2.2/32     *[EVPN/7] 00:37:41
                    >  via irb.13
                    [BGP/170] 00:37:41, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
192.168.2.3/32     *[BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
192.168.2.254/32   *[Local/0] 01:39:15
                       Local via irb.13

L3VPN-100200.inet.0: 6 destinations, 11 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.100.0/24   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299968(top)
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
192.168.100.2/32   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299968(top)
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
192.168.100.3/32   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299968(top)
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
192.168.200.0/24   *[Direct/0] 00:37:53
                    >  via irb.200
                    [BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18
192.168.200.2/32   *[EVPN/7] 00:37:20
                    >  via irb.200
                    [BGP/170] 00:37:20, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18
192.168.200.253/32 *[Local/0] 00:37:53
                       Local via irb.200

mpls.0: 60 destinations, 66 routes (60 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2d 14:18:15, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2d 14:18:15, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2d 14:18:15, metric 1
                       Receive
2                  *[MPLS/0] 2d 14:18:15, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2d 14:18:15, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2d 14:18:15, metric 1
                       Receive
16                 *[VPN/0] 01:39:20
                    >  via lsi.256 (L3VPN-12), Pop
17                 *[VPN/0] 01:39:20
                    >  via lsi.257 (L3VPN-13), Pop
18                 *[VPN/0] 01:30:26
                    >  via lsi.258 (L3VPN-100200), Pop
300768             *[EVPN/7] 01:39:15, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:39:15, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:39:15, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300784             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:0b:00
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300880
300800             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:0c:00
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300912
300832             *[EVPN/7] 01:39:18, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300848             *[EVPN/7] 01:39:18, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300864             *[EVPN/7] 01:39:18, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 13
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300960             *[EVPN/7] 01:39:15, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300992             *[EVPN/7] 01:39:15, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
301040             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
301056             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:c8:00
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301360
301344             *[EVPN/7] 01:30:24, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-IM, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
301584             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 00:02:00:00:00:00:00:00:00:01
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301632
301600             *[EVPN/7] 00:37:43, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-Aliasing
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 00:37:43, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 00:37:43, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 00:37:43, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
301632             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:02:00:00:00:00:00:00:00:01
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301680
301648             *[EVPN/7] 00:37:43, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-Aliasing
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
                    [EVPN/7] 00:37:43, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
302288             *[LDP/9] 00:46:25, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Pop
302288(S=0)        *[LDP/9] 00:46:25, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Pop
302304             *[LDP/9] 00:36:18, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Swap 299968
302320             *[LDP/9] 00:36:18, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 299968
                       to 172.16.35.0 via ge-0/0/5.0, Swap 299936
302336             *[LDP/9] 00:36:18, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Pop
302336(S=0)        *[LDP/9] 00:36:18, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Pop
302352             *[LDP/9] 00:36:18, metric 1
                       to 172.16.34.1 via ge-0/0/4.0, Swap 300000
                    >  to 172.16.35.0 via ge-0/0/5.0, Swap 300000
303296             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:02
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 302192, Push 299968(top)
                       to 172.16.34.1 via ge-0/0/4.0, Push 302208, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 302208, Push 299936(top)
303312             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:01
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301872, Push 299968(top)
                       to 172.16.34.1 via ge-0/0/4.0, Push 301840, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 301840, Push 299936(top)
303328             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:64:00
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301888, Push 299968(top)
                       to 172.16.34.1 via ge-0/0/4.0, Push 301952, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 301952, Push 299936(top)
303344             *[EVPN/7] 00:37:53, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301840, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 301840, Push 299936(top)
303360             *[EVPN/7] 00:37:53, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                       to 172.16.34.1 via ge-0/0/4.0, Push 302208, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 302208, Push 299936(top)
303376             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301632
303392             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301680
303408             *[EVPN/7] 00:37:53, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                       to 172.16.34.1 via ge-0/0/4.0, Push 301952, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301952, Push 299936(top)
303424             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300768
303440             *[EVPN/7] 00:37:53, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 100
                       to 172.16.34.1 via ge-0/0/4.0, Push 301936, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301936, Push 299936(top)
303456             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 11
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300944
303472             *[EVPN/7] 00:37:53, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                       to 172.16.34.1 via ge-0/0/4.0, Push 301792, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301792, Push 299936(top)
303488             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301360
303504             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301040
303520             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300880
303536             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300912
303552             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 11
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 301648, Push 300944(top)
303568             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 200
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 301392
303584             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 12
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300960
303600             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 13
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300976
303616             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-SH, vlan-id 200
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 301648, Push 301392(top)
303632             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 12
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 301648, Push 300960(top)
303648             *[EVPN/7] 00:37:53, remote-pe 172.16.255.4, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 13
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 301648, Push 300976(top)
303664             *[EVPN/7] 00:36:18, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301872, Push 299968(top)
303680             *[EVPN/7] 00:36:18, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 302192, Push 299968(top)
303696             *[EVPN/7] 00:36:18, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301888, Push 299968(top)
303712             *[EVPN/7] 00:36:18, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301824, Push 299968(top)
303728             *[EVPN/7] 00:36:18, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 100
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 301920, Push 299968(top)
303744             *[EVPN/7] 00:37:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0

bgp.l3vpn.0: 30 destinations, 30 routes (30 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1:8:192.168.1.0/24
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
172.16.255.1:8:192.168.1.1/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
172.16.255.1:8:192.168.1.2/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
172.16.255.1:8:192.168.1.3/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299968(top)
172.16.255.1:9:192.168.1.0/24
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
172.16.255.1:9:192.168.1.1/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
172.16.255.1:9:192.168.1.2/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
172.16.255.1:9:192.168.1.3/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299968(top)
172.16.255.1:11:192.168.100.0/24
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299968(top)
172.16.255.1:11:192.168.100.2/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299968(top)
172.16.255.1:11:192.168.100.3/32
                   *[BGP/170] 00:36:18, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299968(top)
172.16.255.2:8:192.168.1.0/24
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
172.16.255.2:8:192.168.1.2/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
172.16.255.2:8:192.168.1.3/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
172.16.255.2:8:192.168.1.4/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
172.16.255.2:9:192.168.1.0/24
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
172.16.255.2:9:192.168.1.2/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
172.16.255.2:9:192.168.1.3/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
172.16.255.2:9:192.168.1.4/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
172.16.255.2:11:192.168.100.0/24
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
172.16.255.2:11:192.168.100.2/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
172.16.255.2:11:192.168.100.3/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
172.16.255.4:8:192.168.2.0/24
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
172.16.255.4:8:192.168.2.2/32
                   *[BGP/170] 00:37:40, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
172.16.255.4:8:192.168.2.3/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
172.16.255.4:9:192.168.2.0/24
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
172.16.255.4:9:192.168.2.2/32
                   *[BGP/170] 00:37:41, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
172.16.255.4:9:192.168.2.3/32
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
172.16.255.4:11:192.168.200.0/24
                   *[BGP/170] 00:37:53, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18
172.16.255.4:11:192.168.200.2/32
                   *[BGP/170] 00:37:20, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 2d 14:30:57
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 14:31:08
                       MultiRecv

bgp.evpn.0: 115 destinations, 115 routes (115 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 640769, Push 299968(top)
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 635137, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 635137, Push 299936(top)
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 641025, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 641025, Push 299936(top)
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 00:37:33
                       Indirect
1:172.16.255.3:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:39:15
                       Indirect
1:172.16.255.3:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:39:15
                       Indirect
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 00:37:53
                       Indirect
1:172.16.255.3:10::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 00:37:44
                       Indirect
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 00:37:44
                       Indirect
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:10::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 632577
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635905, Push 299968(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 634881, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:36:19, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 640769, Push 299968(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 636929, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 636929, Push 299936(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 634369, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 634369, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 635137, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 635137, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 641025, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 641025, Push 299936(top)
2:172.16.255.3:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:39:16
                       Indirect
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[EVPN/170] 01:39:16
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:01:00:00/304 MAC/IP
                   *[EVPN/170] 01:26:23
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.3:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:39:16
                       Indirect
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[EVPN/170] 01:39:16
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:01:00:00/304 MAC/IP
                   *[EVPN/170] 01:26:23
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:42
                       Indirect
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 01:39:16
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:01:00:00/304 MAC/IP
                   *[EVPN/170] 01:26:23
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:42
                       Indirect
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 00:37:54
                       Indirect
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[EVPN/170] 00:37:54
                       Indirect
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:22
                       Indirect
2:172.16.255.4:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 619777
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 620289
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 627457
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 622337
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 632577
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 00:36:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635905, Push 299968(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[BGP/170] 00:36:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 634881, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 00:36:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 00:36:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 640769, Push 299968(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 636929, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 636929, Push 299936(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 634369, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 634369, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 635137, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 635137, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 641025, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 641025, Push 299936(top)
2:172.16.255.3:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[EVPN/170] 01:26:24
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:37:45
                       Indirect
2:172.16.255.3:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[EVPN/170] 01:26:24
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:37:42
                       Indirect
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:39:17
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[EVPN/170] 01:26:24
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:37:43
                       Indirect
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[EVPN/170] 00:37:55
                       Indirect
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[EVPN/170] 00:37:55
                       Indirect
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[EVPN/170] 00:37:23
                       Indirect
2:172.16.255.4:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 619777
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:37:44, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 620289
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:37:42, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:37:43, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 627457
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 622337
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:37:22, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 632577
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[BGP/170] 00:36:20, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
3:172.16.255.3:10::11::172.16.255.3/248 IM
                   *[EVPN/170] 01:39:20
                       Indirect
3:172.16.255.3:10::12::172.16.255.3/248 IM
                   *[EVPN/170] 01:39:20
                       Indirect
3:172.16.255.3:10::13::172.16.255.3/248 IM
                   *[EVPN/170] 01:39:20
                       Indirect
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[EVPN/170] 01:30:26
                       Indirect
3:172.16.255.4:10::11::172.16.255.4/248 IM
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
3:172.16.255.4:10::12::172.16.255.4/248 IM
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
3:172.16.255.4:10::13::172.16.255.4/248 IM
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[BGP/170] 00:37:54, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
4:172.16.255.3:0::020000000000000001:172.16.255.3/296 ES
                   *[EVPN/170] 00:37:35
                       Indirect
4:172.16.255.4:0::020000000000000001:172.16.255.4/296 ES
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0

BALLSACKCITY-EVPN-VLAN-AWARE.evpn.0: 62 destinations, 62 routes (62 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.3:10::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 00:37:46
                       Indirect
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:10::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.3:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:46
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:01:00:00/304 MAC/IP
                   *[EVPN/170] 01:26:25
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:46
                       Indirect
2:172.16.255.3:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:46
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:01:00:00/304 MAC/IP
                   *[EVPN/170] 01:26:25
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:46
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:01:00:00/304 MAC/IP
                   *[EVPN/170] 01:26:25
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.4:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 619777
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 620289
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.3:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[EVPN/170] 01:26:25
                       Indirect
2:172.16.255.3:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:37:46
                       Indirect
2:172.16.255.3:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[EVPN/170] 01:26:25
                       Indirect
2:172.16.255.3:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:37:43
                       Indirect
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:39:18
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[EVPN/170] 01:26:25
                       Indirect
2:172.16.255.3:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:37:44
                       Indirect
2:172.16.255.4:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 619777
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:37:45, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 620289
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:37:43, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 617985
2:172.16.255.4:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:37:44, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 631809
3:172.16.255.3:10::11::172.16.255.3/248 IM
                   *[EVPN/170] 01:39:21
                       Indirect
3:172.16.255.3:10::12::172.16.255.3/248 IM
                   *[EVPN/170] 01:39:21
                       Indirect
3:172.16.255.3:10::13::172.16.255.3/248 IM
                   *[EVPN/170] 01:39:21
                       Indirect
3:172.16.255.4:10::11::172.16.255.4/248 IM
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
3:172.16.255.4:10::12::172.16.255.4/248 IM
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
3:172.16.255.4:10::13::172.16.255.4/248 IM
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0

__default_evpn__.evpn.0: 6 destinations, 6 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 00:37:35
                       Indirect
1:172.16.255.3:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:39:17
                       Indirect
1:172.16.255.3:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:39:17
                       Indirect
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 00:37:55
                       Indirect
4:172.16.255.3:0::020000000000000001:172.16.255.3/296 ES
                   *[EVPN/170] 00:37:36
                       Indirect
4:172.16.255.4:0::020000000000000001:172.16.255.4/296 ES
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0

BALLSACKCITY-EVPN-VLAN-BASED.evpn.0: 48 destinations, 48 routes (48 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 640769, Push 299968(top)
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 635137, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 635137, Push 299936(top)
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 641025, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 641025, Push 299936(top)
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 00:37:46
                       Indirect
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 632577
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635905, Push 299968(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 634881, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 640769, Push 299968(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 636929, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 636929, Push 299936(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 634369, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 634369, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 635137, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 635137, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 641025, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 641025, Push 299936(top)
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 00:37:56
                       Indirect
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[EVPN/170] 00:37:56
                       Indirect
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[EVPN/170] 00:37:46
                       Indirect
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:37:24
                       Indirect
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 627457
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 622337
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 632577
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635905, Push 299968(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 634881, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 635649, Push 299968(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 640769, Push 299968(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 636929, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 636929, Push 299936(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 634369, Push 299968(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 634369, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 635137, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 635137, Push 299936(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 641025, Push 299968(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 641025, Push 299936(top)
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[EVPN/170] 00:37:56
                       Indirect
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[EVPN/170] 00:37:56
                       Indirect
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[EVPN/170] 00:37:24
                       Indirect
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 627457
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[BGP/170] 00:37:56, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 622337
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:37:23, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 632577
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[BGP/170] 00:36:21, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299968
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299968
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[EVPN/170] 01:30:27
                       Indirect
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[BGP/170] 00:37:55, localpref 100, from 172.16.255.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0
```
### PE4
```
root@PE4> show route | no-more

inet.0: 23 destinations, 29 routes (23 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 2d 11:47:48, metric 300
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.15.0/31     *[OSPF/10] 00:37:02, metric 300
                    >  to 172.16.34.0 via ge-0/0/3.0
                       to 172.16.46.0 via ge-0/0/6.0
172.16.26.0/31     *[OSPF/10] 2d 11:47:48, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.34.0/31     *[Direct/0] 2d 14:19:01
                    >  via ge-0/0/3.0
172.16.34.1/32     *[Local/0] 2d 14:19:01
                       Local via ge-0/0/3.0
172.16.35.0/31     *[OSPF/10] 00:37:13, metric 200
                    >  to 172.16.34.0 via ge-0/0/3.0
172.16.46.0/31     *[Direct/0] 2d 14:19:01
                    >  via ge-0/0/6.0
172.16.46.1/32     *[Local/0] 2d 14:19:01
                       Local via ge-0/0/6.0
172.16.56.0/31     *[OSPF/10] 2d 11:47:48, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.255.1/32    @[OSPF/10] 00:37:02, metric 300
                    >  to 172.16.34.0 via ge-0/0/3.0
                       to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 00:37:02, metric 300
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 302304
                       to 172.16.46.0 via ge-0/0/6.0, Push 299984
172.16.255.2/32    @[OSPF/10] 2d 11:47:48, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 2d 11:47:48, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
172.16.255.3/32    @[OSPF/10] 00:46:59, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
                   #[LDP/9] 00:46:59, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
172.16.255.4/32    *[Direct/0] 2d 11:48:45
                    >  via lo0.0
172.16.255.5/32    @[OSPF/10] 00:37:02, metric 200
                    >  to 172.16.34.0 via ge-0/0/3.0
                       to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 00:37:02, metric 200
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 302336
                       to 172.16.46.0 via ge-0/0/6.0, Push 299968
172.16.255.6/32    @[OSPF/10] 2d 11:47:48, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 2d 11:47:48, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0
192.168.1.0/24     *[OSPF/10] 05:25:24, metric 300
                    >  to 172.16.46.0 via ge-0/0/6.0
192.168.2.0/24     *[Direct/0] 01:40:01
                    >  via irb.11
                    [Direct/0] 01:40:01
                    >  via irb.11
192.168.2.2/32     *[EVPN/7] 00:38:26
                    >  via irb.11
192.168.2.3/32     *[EVPN/7] 01:26:45
                    >  via irb.11
192.168.2.252/32   *[Local/0] 01:40:01
                       Local via irb.11
192.168.2.253/32   *[Local/0] 01:40:01
                       Local via irb.11
224.0.0.2/32       *[LDP/9] 2d 14:19:01, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 2d 14:19:01, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1/32    *[LDP/9] 00:37:02, metric 300
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 302304
                       to 172.16.46.0 via ge-0/0/6.0, Push 299984
172.16.255.2/32    *[LDP/9] 2d 11:47:48, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
172.16.255.3/32    *[LDP/9] 00:46:59, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
172.16.255.5/32    *[LDP/9] 00:37:02, metric 200
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 302336
                       to 172.16.46.0 via ge-0/0/6.0, Push 299968
172.16.255.6/32    *[LDP/9] 2d 11:47:48, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0

L3VPN-12.inet.0: 11 destinations, 17 routes (11 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
                    [BGP/170] 01:40:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
192.168.1.1/32     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
192.168.1.2/32     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
                    [BGP/170] 01:40:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
192.168.1.3/32     *[BGP/170] 01:03:54, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
                    [BGP/170] 01:03:54, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
192.168.1.4/32     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
192.168.2.0/24     *[Direct/0] 01:40:01
                    >  via irb.12
                    [Direct/0] 01:40:01
                    >  via irb.12
                    [BGP/170] 00:38:37, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
192.168.2.1/32     *[BGP/170] 00:38:37, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
192.168.2.2/32     *[EVPN/7] 00:38:24
                    >  via irb.12
                    [BGP/170] 00:38:24, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
192.168.2.3/32     *[EVPN/7] 01:26:45
                    >  via irb.12
192.168.2.252/32   *[Local/0] 01:40:01
                       Local via irb.12
192.168.2.253/32   *[Local/0] 01:40:01
                       Local via irb.12

L3VPN-13.inet.0: 10 destinations, 15 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.0/24     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
                    [BGP/170] 01:40:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.1.1/32     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.1.2/32     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
                    [BGP/170] 01:40:01, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.1.3/32     *[BGP/170] 01:01:25, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
                    [BGP/170] 01:01:25, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.1.4/32     *[BGP/170] 01:40:01, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
192.168.2.0/24     *[Direct/0] 01:40:01
                    >  via irb.13
                    [BGP/170] 00:38:37, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
192.168.2.1/32     *[BGP/170] 00:38:37, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
192.168.2.2/32     *[EVPN/7] 00:38:25
                    >  via irb.13
                    [BGP/170] 00:38:25, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
192.168.2.3/32     *[EVPN/7] 01:26:45
                    >  via irb.13
192.168.2.254/32   *[Local/0] 01:40:01
                       Local via irb.13

L3VPN-100200.inet.0: 6 destinations, 11 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.100.0/24   *[BGP/170] 01:31:07, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 300000(top)
                    [BGP/170] 01:31:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299984(top)
192.168.100.2/32   *[BGP/170] 01:31:07, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 300000(top)
                    [BGP/170] 01:31:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299984(top)
192.168.100.3/32   *[BGP/170] 01:31:07, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 300000(top)
                    [BGP/170] 01:31:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299984(top)
192.168.200.0/24   *[Direct/0] 01:31:07
                    >  via irb.200
                    [BGP/170] 00:38:37, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18
192.168.200.2/32   *[EVPN/7] 00:38:04
                    >  via irb.200
                    [BGP/170] 00:38:05, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18
192.168.200.252/32 *[Local/0] 01:31:07
                       Local via irb.200

mpls.0: 60 destinations, 66 routes (60 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2d 14:19:01, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2d 14:19:01, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2d 14:19:01, metric 1
                       Receive
2                  *[MPLS/0] 2d 14:19:01, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2d 14:19:01, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2d 14:19:01, metric 1
                       Receive
16                 *[VPN/0] 01:40:01
                    >  via lsi.256 (L3VPN-12), Pop
17                 *[VPN/0] 01:40:01
                    >  via lsi.257 (L3VPN-13), Pop
18                 *[VPN/0] 01:31:08
                    >  via lsi.258 (L3VPN-100200), Pop
299936             *[LDP/9] 00:37:02, metric 1
                    >  to 172.16.34.0 via ge-0/0/3.0, Swap 302304
                       to 172.16.46.0 via ge-0/0/6.0, Swap 299984
299968             *[LDP/9] 2d 11:47:48, metric 1
                    >  to 172.16.46.0 via ge-0/0/6.0, Swap 300000
299984             *[LDP/9] 00:37:02, metric 1
                    >  to 172.16.34.0 via ge-0/0/3.0, Swap 302336
                       to 172.16.46.0 via ge-0/0/6.0, Swap 299968
300000             *[LDP/9] 2d 11:47:58, metric 1
                    >  to 172.16.46.0 via ge-0/0/6.0, Pop
300000(S=0)        *[LDP/9] 2d 11:47:58, metric 1
                    >  to 172.16.46.0 via ge-0/0/6.0, Pop
300768             *[EVPN/7] 01:40:01, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:40:01, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:40:01, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300784             *[EVPN/7] 00:38:37, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:0b:00
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300960
300800             *[EVPN/7] 00:38:37, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:0c:00
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300992
300880             *[EVPN/7] 01:40:01, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300912             *[EVPN/7] 01:40:01, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300944             *[EVPN/7] 01:40:00, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300960             *[EVPN/7] 01:40:00, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
300976             *[EVPN/7] 01:39:59, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-IM, vlan-id 13
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
301040             *[EVPN/7] 01:31:07, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
301056             *[EVPN/7] 00:38:36, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:c8:00
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 303744
301072             *[EVPN/7] 01:16:01, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:02
                       to 172.16.34.0 via ge-0/0/3.0, Push 302192, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 302192, Push 299984(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 302208, Push 300000(top)
301152             *[EVPN/7] 01:31:07, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:64:00
                       to 172.16.34.0 via ge-0/0/3.0, Push 301888, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 301888, Push 299984(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301952, Push 300000(top)
301168             *[EVPN/7] 01:31:07, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:01:00:00:00:00:00:00:00:01
                       to 172.16.34.0 via ge-0/0/3.0, Push 301872, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 301872, Push 299984(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301840, Push 300000(top)
301184             *[EVPN/7] 01:31:07, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301872, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 301872, Push 299984(top)
301200             *[EVPN/7] 01:31:07, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 302192, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 302192, Push 299984(top)
301216             *[EVPN/7] 01:31:07, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301840, Push 300000(top)
301232             *[EVPN/7] 01:31:07, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 302208, Push 300000(top)
301264             *[EVPN/7] 01:31:07, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301888, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 301888, Push 299984(top)
301280             *[EVPN/7] 01:31:07, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301952, Push 300000(top)
301296             *[EVPN/7] 01:31:07, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301792, Push 300000(top)
301312             *[EVPN/7] 01:31:07, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                       to 172.16.34.0 via ge-0/0/3.0, Push 301824, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301824, Push 299984(top)
301328             *[EVPN/7] 01:31:07, remote-pe 172.16.255.2, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 100
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301936, Push 300000(top)
301344             *[EVPN/7] 01:31:07, remote-pe 172.16.255.1, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 100
                       to 172.16.34.0 via ge-0/0/3.0, Push 301920, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 301920, Push 299984(top)
301360             *[EVPN/7] 01:31:07, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
301392             *[EVPN/7] 01:31:06, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-IM, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
301616             *[EVPN/7] 00:38:16, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC, ESI 00:02:00:00:00:00:00:00:00:01
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301600
301632             *[EVPN/7] 01:15:53, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-Aliasing
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:12:55, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 12
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 01:01:25, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 13
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
                    [EVPN/7] 00:48:25, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Ingress-MAC, vlan-id 11
                       to table BALLSACKCITY-EVPN-VLAN-AWARE.evpn-mac.0
301664             *[EVPN/7] 00:38:16, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC, ESI 00:02:00:00:00:00:00:00:00:01
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301648
301680             *[EVPN/7] 01:15:53, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-Aliasing
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
                    [EVPN/7] 00:59:05, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Ingress-MAC, vlan-id 200
                       to table BALLSACKCITY-EVPN-VLAN-BASED.evpn-mac.0
301792             *[LDP/9] 00:47:09, metric 1
                    >  to 172.16.34.0 via ge-0/0/3.0, Pop
301792(S=0)        *[LDP/9] 00:47:09, metric 1
                    >  to 172.16.34.0 via ge-0/0/3.0, Pop
302432             *[EVPN/7] 00:38:37, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300768
302448             *[EVPN/7] 00:38:37, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300992
302464             *[EVPN/7] 00:38:37, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 12
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300848
302480             *[EVPN/7] 00:38:37, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 13
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300864
302496             *[EVPN/7] 00:38:37, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-IM, vlan-id 11
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300832
302512             *[EVPN/7] 00:38:38, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-IM, vlan-id 200
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301344
302528             *[EVPN/7] 00:38:38, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 300960
302544             *[EVPN/7] 00:38:38, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301040
302560             *[EVPN/7] 00:38:37, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 303744
302576             *[EVPN/7] 00:38:17, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301600
302592             *[EVPN/7] 00:38:17, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 301648
302608             *[EVPN/7] 00:38:17, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 11
                    >  to 172.16.34.0 via ge-0/0/3.0, Swap 301616, Push 300832(top)
302624             *[EVPN/7] 00:38:17, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 12
                    >  to 172.16.34.0 via ge-0/0/3.0, Swap 301616, Push 300848(top)
302640             *[EVPN/7] 00:38:17, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-AWARE, route-type Egress-SH, vlan-id 13
                    >  to 172.16.34.0 via ge-0/0/3.0, Swap 301616, Push 300864(top)
302656             *[EVPN/7] 00:38:17, remote-pe 172.16.255.3, routing-instance BALLSACKCITY-EVPN-VLAN-BASED, route-type Egress-SH, vlan-id 200
                    >  to 172.16.34.0 via ge-0/0/3.0, Swap 301616, Push 301344(top)

bgp.l3vpn.0: 30 destinations, 30 routes (30 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1:8:192.168.1.0/24
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
172.16.255.1:8:192.168.1.1/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
172.16.255.1:8:192.168.1.2/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
172.16.255.1:8:192.168.1.3/32
                   *[BGP/170] 01:03:55, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299984(top)
172.16.255.1:9:192.168.1.0/24
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
172.16.255.1:9:192.168.1.1/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
172.16.255.1:9:192.168.1.2/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
172.16.255.1:9:192.168.1.3/32
                   *[BGP/170] 01:01:26, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299984(top)
172.16.255.1:11:192.168.100.0/24
                   *[BGP/170] 01:31:08, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299984(top)
172.16.255.1:11:192.168.100.2/32
                   *[BGP/170] 01:31:08, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299984(top)
172.16.255.1:11:192.168.100.3/32
                   *[BGP/170] 01:31:08, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299984(top)
172.16.255.2:8:192.168.1.0/24
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
172.16.255.2:8:192.168.1.2/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
172.16.255.2:8:192.168.1.3/32
                   *[BGP/170] 01:03:55, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
172.16.255.2:8:192.168.1.4/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 300000(top)
172.16.255.2:9:192.168.1.0/24
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
172.16.255.2:9:192.168.1.2/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
172.16.255.2:9:192.168.1.3/32
                   *[BGP/170] 01:01:26, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
172.16.255.2:9:192.168.1.4/32
                   *[BGP/170] 01:40:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 300000(top)
172.16.255.2:11:192.168.100.0/24
                   *[BGP/170] 01:31:08, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 300000(top)
172.16.255.2:11:192.168.100.2/32
                   *[BGP/170] 01:31:08, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 300000(top)
172.16.255.2:11:192.168.100.3/32
                   *[BGP/170] 01:31:08, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 300000(top)
172.16.255.3:8:192.168.2.0/24
                   *[BGP/170] 00:38:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
172.16.255.3:8:192.168.2.1/32
                   *[BGP/170] 00:38:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
172.16.255.3:8:192.168.2.2/32
                   *[BGP/170] 00:38:25, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
172.16.255.3:9:192.168.2.0/24
                   *[BGP/170] 00:38:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
172.16.255.3:9:192.168.2.1/32
                   *[BGP/170] 00:38:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
172.16.255.3:9:192.168.2.2/32
                   *[BGP/170] 00:38:26, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
172.16.255.3:11:192.168.200.0/24
                   *[BGP/170] 00:38:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18
172.16.255.3:11:192.168.200.2/32
                   *[BGP/170] 00:38:06, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 18

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe04:0/128
                   *[Local/0] 2d 14:31:40
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 14:31:51
                       MultiRecv

bgp.evpn.0: 115 destinations, 115 routes (115 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 640769, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 640769, Push 299984(top)
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635137, Push 300000(top)
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 641025, Push 300000(top)
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:18, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:38, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:10::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:15:44
                       Indirect
1:172.16.255.4:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:40:02
                       Indirect
1:172.16.255.4:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:40:02
                       Indirect
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:31:08
                       Indirect
1:172.16.255.4:10::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 01:15:55
                       Indirect
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 01:15:55
                       Indirect
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635905, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635905, Push 299984(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 634881, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 634881, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 640769, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 640769, Push 299984(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 636929, Push 300000(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 634369, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 01:31:09, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635137, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:16:02, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 641025, Push 300000(top)
2:172.16.255.3:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621057
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::11::aa:bb:cc:01:00:00/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621569
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::12::aa:bb:cc:01:00:00/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:26, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::13::aa:bb:cc:01:00:00/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:27, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 665601
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:38:39, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 622337
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:07, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
2:172.16.255.4:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:40:03
                       Indirect
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 01:26:48
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:48:28
                       Indirect
2:172.16.255.4:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 01:26:48
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 01:12:58
                       Indirect
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 01:26:48
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 01:01:28
                       Indirect
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:31:10
                       Indirect
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[EVPN/170] 01:31:10
                       Indirect
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:59:08
                       Indirect
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 635905, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635905, Push 299984(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 634881, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 634881, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 640769, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 640769, Push 299984(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 636929, Push 300000(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 634369, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 01:31:10, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635137, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 01:16:03, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 641025, Push 300000(top)
2:172.16.255.3:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621057
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:38:30, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621569
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:38:27, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:38:28, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 665601
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[BGP/170] 00:38:40, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 622337
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:38:08, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
2:172.16.255.4:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[EVPN/170] 01:26:48
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:38:29
                       Indirect
2:172.16.255.4:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[EVPN/170] 01:26:48
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:38:27
                       Indirect
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:40:04
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[EVPN/170] 01:26:48
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:38:28
                       Indirect
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[EVPN/170] 01:31:11
                       Indirect
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[EVPN/170] 01:31:11
                       Indirect
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[EVPN/170] 00:38:08
                       Indirect
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[BGP/170] 01:16:07, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[BGP/170] 01:16:07, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
3:172.16.255.3:10::11::172.16.255.3/248 IM
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.3:10::12::172.16.255.3/248 IM
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.3:10::13::172.16.255.3/248 IM
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.4:10::11::172.16.255.4/248 IM
                   *[EVPN/170] 01:40:04
                       Indirect
3:172.16.255.4:10::12::172.16.255.4/248 IM
                   *[EVPN/170] 01:40:04
                       Indirect
3:172.16.255.4:10::13::172.16.255.4/248 IM
                   *[EVPN/170] 01:40:03
                       Indirect
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[EVPN/170] 01:31:10
                       Indirect
4:172.16.255.3:0::020000000000000001:172.16.255.3/296 ES
                   *[BGP/170] 00:38:21, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
4:172.16.255.4:0::020000000000000001:172.16.255.4/296 ES
                   *[EVPN/170] 01:15:47
                       Indirect

BALLSACKCITY-EVPN-VLAN-AWARE.evpn.0: 62 destinations, 62 routes (62 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:20, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:10::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:38:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
1:172.16.255.4:10::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 01:15:57
                       Indirect
2:172.16.255.3:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621057
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::11::aa:bb:cc:01:00:00/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621569
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::12::aa:bb:cc:01:00:00/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:28, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::13::aa:bb:cc:01:00:00/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.4:10::11::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 01:26:49
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:48:29
                       Indirect
2:172.16.255.4:10::12::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 01:26:49
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 01:12:59
                       Indirect
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 01:26:49
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 01:01:29
                       Indirect
2:172.16.255.3:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621057
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:38:31, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 621569
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.252/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::2c:6b:f5:9b:d3:f0::192.168.2.253/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:38:28, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.3:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:01:00:00::192.168.2.1/304 MAC/IP
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 617985
2:172.16.255.3:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[BGP/170] 00:38:29, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 631297
2:172.16.255.4:10::11::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::11::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[EVPN/170] 01:26:49
                       Indirect
2:172.16.255.4:10::11::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:38:30
                       Indirect
2:172.16.255.4:10::12::00:00:5e:00:01:01::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.252/304 MAC/IP
                   *[EVPN/170] 01:40:05
                       Indirect
2:172.16.255.4:10::12::2c:6b:f5:ea:f4:f0::192.168.2.253/304 MAC/IP
                   *[EVPN/170] 01:40:06
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[EVPN/170] 01:26:50
                       Indirect
2:172.16.255.4:10::12::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:38:29
                       Indirect
2:172.16.255.4:10::13::aa:aa:aa:aa:aa:aa::192.168.2.254/304 MAC/IP
                   *[EVPN/170] 01:40:06
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:00:c0:00::192.168.2.3/304 MAC/IP
                   *[EVPN/170] 01:26:50
                       Indirect
2:172.16.255.4:10::13::aa:bb:cc:80:90:00::192.168.2.2/304 MAC/IP
                   *[EVPN/170] 00:38:30
                       Indirect
3:172.16.255.3:10::11::172.16.255.3/248 IM
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.3:10::12::172.16.255.3/248 IM
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.3:10::13::172.16.255.3/248 IM
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.4:10::11::172.16.255.4/248 IM
                   *[EVPN/170] 01:40:05
                       Indirect
3:172.16.255.4:10::12::172.16.255.4/248 IM
                   *[EVPN/170] 01:40:05
                       Indirect
3:172.16.255.4:10::13::172.16.255.4/248 IM
                   *[EVPN/170] 01:40:04
                       Indirect

__default_evpn__.evpn.0: 6 destinations, 6 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.4:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:15:47
                       Indirect
1:172.16.255.4:0::050000ffdc0000000b00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:40:05
                       Indirect
1:172.16.255.4:0::050000ffdc0000000c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:40:05
                       Indirect
1:172.16.255.4:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 01:31:11
                       Indirect
4:172.16.255.3:0::020000000000000001:172.16.255.3/296 ES
                   *[BGP/170] 00:38:22, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
4:172.16.255.4:0::020000000000000001:172.16.255.4/296 ES
                   *[EVPN/170] 01:15:48
                       Indirect

BALLSACKCITY-EVPN-VLAN-BASED.evpn.0: 48 destinations, 48 routes (48 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:172.16.255.1:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
1:172.16.255.1:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
1:172.16.255.1:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
1:172.16.255.1:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
1:172.16.255.1:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 640769, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 640769, Push 299984(top)
1:172.16.255.2:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
1:172.16.255.2:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
1:172.16.255.2:0::050000ffdc0000006400::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
1:172.16.255.2:12::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635137, Push 300000(top)
1:172.16.255.2:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 641025, Push 300000(top)
1:172.16.255.3:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:21, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:0::050000ffdc000000c800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 00:38:41, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
1:172.16.255.3:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 00:38:32, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
1:172.16.255.4:12::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 01:15:58
                       Indirect
2:172.16.255.1:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635905, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635905, Push 299984(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 634881, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 634881, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 640769, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 640769, Push 299984(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 636929, Push 300000(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 634369, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635137, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00/304 MAC/IP
                   *[BGP/170] 01:16:05, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 641025, Push 300000(top)
2:172.16.255.3:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 665601
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0/304 MAC/IP
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 622337
2:172.16.255.3:12::200::aa:bb:cc:00:90:10/304 MAC/IP
                   *[BGP/170] 00:38:32, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
2:172.16.255.3:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:38:10, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
2:172.16.255.4:12::200::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 01:31:12
                       Indirect
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0/304 MAC/IP
                   *[EVPN/170] 01:31:12
                       Indirect
2:172.16.255.4:12::200::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:59:10
                       Indirect
2:172.16.255.1:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 635905, Push 302304(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635905, Push 299984(top)
2:172.16.255.1:12::100::2c:6b:f5:fe:aa:f0::192.168.100.253/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 634881, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 634881, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 635649, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 635649, Push 299984(top)
2:172.16.255.1:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 640769, Push 302304(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 640769, Push 299984(top)
2:172.16.255.2:12::100::00:00:5e:00:01:01::192.168.100.254/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 636929, Push 300000(top)
2:172.16.255.2:12::100::2c:6b:f5:7e:74:f0::192.168.100.252/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 634369, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:80:70:00::192.168.100.2/304 MAC/IP
                   *[BGP/170] 01:31:12, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 635137, Push 300000(top)
2:172.16.255.2:12::100::aa:bb:cc:81:30:00::192.168.100.3/304 MAC/IP
                   *[BGP/170] 01:16:05, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 641025, Push 300000(top)
2:172.16.255.3:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 665601
2:172.16.255.3:12::200::2c:6b:f5:9b:d3:f0::192.168.200.253/304 MAC/IP
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 622337
2:172.16.255.3:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[BGP/170] 00:38:10, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 632065
2:172.16.255.4:12::200::00:00:5e:00:01:01::192.168.200.254/304 MAC/IP
                   *[EVPN/170] 01:31:12
                       Indirect
2:172.16.255.4:12::200::2c:6b:f5:ea:f4:f0::192.168.200.252/304 MAC/IP
                   *[EVPN/170] 01:31:12
                       Indirect
2:172.16.255.4:12::200::aa:bb:cc:80:90:00::192.168.200.2/304 MAC/IP
                   *[EVPN/170] 00:38:09
                       Indirect
3:172.16.255.1:12::100::172.16.255.1/248 IM
                   *[BGP/170] 01:16:08, localpref 100, from 172.16.255.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 302304
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984
3:172.16.255.2:12::100::172.16.255.2/248 IM
                   *[BGP/170] 01:16:08, localpref 100, from 172.16.255.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300000
3:172.16.255.3:12::200::172.16.255.3/248 IM
                   *[BGP/170] 00:38:42, localpref 100, from 172.16.255.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:172.16.255.4:12::200::172.16.255.4/248 IM
                   *[EVPN/170] 01:31:11
                       Indirect
```
### P5
```
root@P5> show route

inet.0: 20 destinations, 25 routes (20 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 1d 07:47:51, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0
172.16.15.0/31     *[Direct/0] 2d 14:17:40
                    >  via ge-0/0/1.0
172.16.15.0/32     *[Local/0] 2d 14:17:40
                       Local via ge-0/0/1.0
172.16.26.0/31     *[OSPF/10] 2d 11:46:25, metric 200
                    >  to 172.16.56.1 via ge-0/0/6.0
172.16.34.0/31     *[OSPF/10] 00:35:39, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0
172.16.35.0/31     *[Direct/0] 2d 14:17:40
                    >  via ge-0/0/3.0
172.16.35.0/32     *[Local/0] 2d 14:17:40
                       Local via ge-0/0/3.0
172.16.46.0/31     *[OSPF/10] 2d 11:46:25, metric 200
                    >  to 172.16.56.1 via ge-0/0/6.0
172.16.56.0/31     *[Direct/0] 2d 14:17:40
                    >  via ge-0/0/6.0
172.16.56.0/32     *[Local/0] 2d 14:17:40
                       Local via ge-0/0/6.0
172.16.255.1/32    @[OSPF/10] 2d 11:46:42, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
                   #[LDP/9] 2d 11:46:42, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
172.16.255.2/32    @[OSPF/10] 1d 07:47:51, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0
                       to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 07:47:51, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0, Push 300480
                       to 172.16.56.1 via ge-0/0/6.0, Push 300000
172.16.255.3/32    @[OSPF/10] 00:35:39, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
                   #[LDP/9] 00:35:39, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
172.16.255.4/32    @[OSPF/10] 00:35:39, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0
                       to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 00:35:39, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0, Push 302288
                       to 172.16.56.1 via ge-0/0/6.0, Push 299936
172.16.255.5/32    *[Direct/0] 2d 11:46:53
                    >  via lo0.0
172.16.255.6/32    @[OSPF/10] 2d 11:46:25, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 2d 11:46:25, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0
192.168.1.0/24     *[OSPF/10] 05:24:26, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0
192.168.2.0/24     *[OSPF/10] 00:35:39, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0
224.0.0.2/32       *[LDP/9] 2d 14:17:40, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 2d 14:17:40, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1/32    *[LDP/9] 2d 11:46:42, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
172.16.255.2/32    *[LDP/9] 1d 07:47:51, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0, Push 300480
                       to 172.16.56.1 via ge-0/0/6.0, Push 300000
172.16.255.3/32    *[LDP/9] 00:35:39, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
172.16.255.4/32    *[LDP/9] 00:35:39, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0, Push 302288
                       to 172.16.56.1 via ge-0/0/6.0, Push 299936
172.16.255.6/32    *[LDP/9] 2d 11:46:25, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0

mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2d 14:17:40, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2d 14:17:40, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2d 14:17:40, metric 1
                       Receive
2                  *[MPLS/0] 2d 14:17:40, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2d 14:17:40, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2d 14:17:40, metric 1
                       Receive
299936             *[LDP/9] 1d 07:47:51, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Swap 300480
                       to 172.16.56.1 via ge-0/0/6.0, Swap 300000
299952             *[LDP/9] 00:35:39, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Swap 302288
                       to 172.16.56.1 via ge-0/0/6.0, Swap 299936
299968             *[LDP/9] 2d 11:46:52, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Pop
299968(S=0)        *[LDP/9] 2d 11:46:52, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Pop
300000             *[LDP/9] 2d 11:46:35, metric 1
                    >  to 172.16.56.1 via ge-0/0/6.0, Pop
300000(S=0)        *[LDP/9] 2d 11:46:35, metric 1
                    >  to 172.16.56.1 via ge-0/0/6.0, Pop
300016             *[LDP/9] 00:35:39, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Pop
300016(S=0)        *[LDP/9] 00:35:39, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Pop

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 2d 14:30:25
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 14:30:36
                       MultiRecv
```
### P6
```
root@P6> show route | no-more

inet.0: 20 destinations, 25 routes (20 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 2d 11:46:44, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0
172.16.15.0/31     *[OSPF/10] 2d 11:46:44, metric 200
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.26.0/31     *[Direct/0] 2d 14:18:02
                    >  via ge-0/0/2.0
172.16.26.0/32     *[Local/0] 2d 14:18:02
                       Local via ge-0/0/2.0
172.16.34.0/31     *[OSPF/10] 2d 11:46:44, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0
172.16.35.0/31     *[OSPF/10] 2d 11:46:44, metric 200
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.46.0/31     *[Direct/0] 2d 14:18:02
                    >  via ge-0/0/4.0
172.16.46.0/32     *[Local/0] 2d 14:18:02
                       Local via ge-0/0/4.0
172.16.56.0/31     *[Direct/0] 2d 14:18:02
                    >  via ge-0/0/5.0
172.16.56.1/32     *[Local/0] 2d 14:18:02
                       Local via ge-0/0/5.0
172.16.255.1/32    @[OSPF/10] 2d 11:46:44, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0
                       to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 2d 11:46:44, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 300304
                       to 172.16.56.0 via ge-0/0/5.0, Push 299968
172.16.255.2/32    @[OSPF/10] 2d 11:46:44, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
                   #[LDP/9] 2d 11:46:44, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
172.16.255.3/32    @[OSPF/10] 00:35:58, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0
                       to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 00:35:58, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0, Push 301792
                       to 172.16.56.0 via ge-0/0/5.0, Push 300016
172.16.255.4/32    @[OSPF/10] 2d 11:46:44, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
                   #[LDP/9] 2d 11:46:44, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
172.16.255.5/32    @[OSPF/10] 2d 11:46:44, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 2d 11:46:44, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.255.6/32    *[Direct/0] 2d 11:46:55
                    >  via lo0.0
192.168.1.0/24     *[OSPF/10] 05:24:20, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0
192.168.2.0/24     *[OSPF/10] 01:38:56, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0
224.0.0.2/32       *[LDP/9] 2d 14:18:02, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 2d 14:18:02, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

172.16.255.1/32    *[LDP/9] 2d 11:46:44, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 300304
                       to 172.16.56.0 via ge-0/0/5.0, Push 299968
172.16.255.2/32    *[LDP/9] 2d 11:46:44, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
172.16.255.3/32    *[LDP/9] 00:35:58, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0, Push 301792
                       to 172.16.56.0 via ge-0/0/5.0, Push 300016
172.16.255.4/32    *[LDP/9] 2d 11:46:44, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
172.16.255.5/32    *[LDP/9] 2d 11:46:44, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0

mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2d 14:18:02, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2d 14:18:02, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2d 14:18:02, metric 1
                       Receive
2                  *[MPLS/0] 2d 14:18:02, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2d 14:18:02, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2d 14:18:02, metric 1
                       Receive
299936             *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop
299936(S=0)        *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop
299968             *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.56.0 via ge-0/0/5.0, Pop
299968(S=0)        *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.56.0 via ge-0/0/5.0, Pop
299984             *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Swap 300304
                       to 172.16.56.0 via ge-0/0/5.0, Swap 299968
300000             *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Pop
300000(S=0)        *[LDP/9] 2d 11:46:54, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Pop
300016             *[LDP/9] 00:35:58, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Swap 301792
                       to 172.16.56.0 via ge-0/0/5.0, Swap 300016

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe06:0/128
                   *[Local/0] 2d 14:30:35
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 14:30:46
                       MultiRecv
```
