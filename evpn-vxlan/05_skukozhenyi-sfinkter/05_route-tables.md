### PE1
```
root@PE1> show route | no-more

inet.0: 20 destinations, 25 routes (20 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

10.120.0.0/24      *[Direct/0] 23:54:34
                    >  via irb.120
10.120.0.1/32      *[EVPN/7] 23:24:33
                    >  via irb.120
10.120.0.254/32    *[Local/0] 23:54:34
                       Local via irb.120
172.16.12.0/31     *[Direct/0] 1d 01:40:07
                    >  via ge-0/0/2.0
172.16.12.0/32     *[Local/0] 1d 01:40:07
                       Local via ge-0/0/2.0
172.16.15.0/31     *[Direct/0] 1d 01:40:07
                    >  via ge-0/0/5.0
172.16.15.1/32     *[Local/0] 1d 01:40:07
                       Local via ge-0/0/5.0
172.16.26.0/31     *[OSPF/10] 1d 00:52:59, metric 200
                    >  to 172.16.12.1 via ge-0/0/2.0
172.16.34.0/31     *[OSPF/10] 1d 00:52:23, metric 300
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.35.0/31     *[OSPF/10] 1d 00:52:23, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.46.0/31     *[OSPF/10] 1d 00:52:07, metric 300
                    >  to 172.16.12.1 via ge-0/0/2.0
                       to 172.16.15.0 via ge-0/0/5.0
172.16.56.0/31     *[OSPF/10] 1d 00:52:23, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.1/32     *[Direct/0] 1d 00:53:28
                    >  via lo0.0
192.168.1.2/32     @[OSPF/10] 1d 00:52:59, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
                   #[LDP/9] 1d 00:52:59, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.3/32     @[OSPF/10] 1d 00:52:23, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:52:23, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
192.168.1.4/32     @[OSPF/10] 1d 00:52:07, metric 300
                       to 172.16.12.1 via ge-0/0/2.0
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:52:07, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 299824
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299792
192.168.1.5/32     @[OSPF/10] 1d 00:52:23, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:52:23, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.6/32     @[OSPF/10] 1d 00:52:07, metric 200
                       to 172.16.12.1 via ge-0/0/2.0
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:52:07, metric 200
                       to 172.16.12.1 via ge-0/0/2.0, Push 299840
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299840
224.0.0.2/32       *[LDP/9] 1d 01:40:07, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 01:40:07, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.2/32     *[LDP/9] 1d 00:52:59, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.3/32     *[LDP/9] 1d 00:52:23, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
192.168.1.4/32     *[LDP/9] 1d 00:52:07, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 299824
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299792
192.168.1.5/32     *[LDP/9] 1d 00:52:23, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.6/32     *[LDP/9] 1d 00:52:07, metric 200
                       to 172.16.12.1 via ge-0/0/2.0, Push 299840
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299840

GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 6 destinations, 7 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.130.12.0/24     *[Direct/0] 22:42:30
                    >  via irb.130
                    [BGP/170] 22:42:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.130.12.1/32     *[EVPN/7] 21:57:00
                    >  via irb.130
10.130.12.2/32     *[BGP/170] 21:56:42, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.130.12.254/32   *[Local/0] 22:42:30
                       Local via irb.130
10.130.30.0/24     *[BGP/170] 22:05:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299776(top)
10.130.40.0/24     *[BGP/170] 22:05:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 299824(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299792(top)

RED-CUSTOMER-HUYASTOMER-L3VPN.inet.0: 6 destinations, 8 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.140.123.0/24    *[Direct/0] 06:45:45
                    >  via irb.140
                    [BGP/170] 06:45:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
                    [BGP/170] 06:45:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299776(top)
10.140.123.1/32    *[EVPN/7] 06:42:25
                    >  via irb.140
10.140.123.2/32    *[BGP/170] 06:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
10.140.123.3/32    *[BGP/170] 06:29:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299776(top)
10.140.123.251/32  *[Local/0] 06:45:45
                       Local via irb.140
10.141.40.0/24     *[BGP/170] 06:45:33, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299792(top)

mpls.0: 41 destinations, 41 routes (41 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 01:04:43, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 01:04:43, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 01:40:07, metric 1
                       Receive
2                  *[MPLS/0] 1d 01:04:43, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 01:04:43, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 01:40:07, metric 1
                       Receive
16                 *[VPN/0] 22:46:45
                    >  via lsi.0 (GREEN-ZALUPA-INCORPORATED-L3VPN), Pop
17                 *[VPN/0] 06:45:45
                    >  via lsi.1 (RED-CUSTOMER-HUYASTOMER-L3VPN), Pop
299776             *[LDP/9] 1d 00:53:10, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Pop
299776(S=0)        *[LDP/9] 1d 00:53:10, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Pop
299792             *[LDP/9] 1d 00:52:33, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Pop
299792(S=0)        *[LDP/9] 1d 00:52:33, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Pop
299808             *[LDP/9] 1d 00:52:33, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 299776
299824             *[LDP/9] 1d 00:52:07, metric 1
                       to 172.16.12.1 via ge-0/0/2.0, Swap 299824
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 299792
299840             *[LDP/9] 1d 00:52:18, metric 1
                       to 172.16.12.1 via ge-0/0/2.0, Swap 299840
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 299840
299856             *[EVPN/7] 1d 00:40:33, routing-instance PURPLE-PILLS-EVPN, route-type Ingress-MAC, vlan-id 110
                       to table PURPLE-PILLS-EVPN.evpn-mac.0
299872             *[EVPN/7] 1d 00:46:51, remote-pe 192.168.1.2, routing-instance PURPLE-PILLS-EVPN, route-type Egress-IM, vlan-id 110
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 299872
299888             *[EVPN/7] 1d 00:46:50, routing-instance PURPLE-PILLS-EVPN, route-type Ingress-IM, vlan-id 110
                       to table PURPLE-PILLS-EVPN.evpn-mac.0
299904             *[EVPN/7] 1d 00:40:24, remote-pe 192.168.1.2, routing-instance PURPLE-PILLS-EVPN, route-type Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 299856
299920             *[EVPN/7] 23:54:34, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-MAC, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
299952             *[EVPN/7] 23:54:33, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-IM, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
299968             *[EVPN/7] 23:54:24, remote-pe 192.168.1.2, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 299920
299984             *[EVPN/7] 23:54:23, remote-pe 192.168.1.2, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 299984
300000             *[EVPN/7] 23:49:53, remote-pe 192.168.1.3, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299856, Push 299776(top)
300016             *[EVPN/7] 23:49:52, remote-pe 192.168.1.3, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299952, Push 299776(top)
300032             *[EVPN/7] 23:49:48, remote-pe 192.168.1.4, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                       to 172.16.12.1 via ge-0/0/2.0, Push 299856, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299856, Push 299792(top)
300048             *[EVPN/7] 23:49:47, remote-pe 192.168.1.4, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                       to 172.16.12.1 via ge-0/0/2.0, Push 299984, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299984, Push 299792(top)
300064             *[EVPN/7] 22:53:19, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Ingress-MAC, vlan-id 130
                       to table GREEN-ZALUPA-INCORPORATED-EVPN.evpn-mac.0
300096             *[EVPN/7] 23:00:12, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Ingress-IM, vlan-id 130
                       to table GREEN-ZALUPA-INCORPORATED-EVPN.evpn-mac.0
300112             *[EVPN/7] 23:00:01, remote-pe 192.168.1.2, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Egress-IM, vlan-id 130
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300112
300128             *[EVPN/7] 22:53:17, remote-pe 192.168.1.2, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300064
300144             *[EVPN/7] 06:42:25, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-MAC, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300160             *[EVPN/7] 06:45:37, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:8c:00
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300320
                       to 172.16.15.0 via ge-0/0/5.0, Push 300160, Push 299776(top)
300208             *[EVPN/7] 07:03:50, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-IM, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300240             *[EVPN/7] 07:03:23, remote-pe 192.168.1.2, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-IM, vlan-id 140
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300240
300272             *[EVPN/7] 07:03:05, remote-pe 192.168.1.3, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-IM, vlan-id 140
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300128, Push 299776(top)
300288             *[EVPN/7] 06:45:45, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-MAC, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300320             *[EVPN/7] 06:45:41, remote-pe 192.168.1.3, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300160, Push 299776(top)
300336             *[EVPN/7] 06:45:37, remote-pe 192.168.1.2, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300320
300352             *[EVPN/7] 06:34:58, remote-pe 192.168.1.2, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 300144
300368             *[EVPN/7] 06:29:04, remote-pe 192.168.1.3, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 300000, Push 299776(top)

bgp.l3vpn.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.2:11:10.130.12.0/24
                   *[BGP/170] 22:42:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.2:11:10.130.12.2/32
                   *[BGP/170] 21:56:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.2:13:10.140.123.0/24
                   *[BGP/170] 06:45:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.2:13:10.140.123.2/32
                   *[BGP/170] 06:34:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.3:9:10.130.30.0/24
                   *[BGP/170] 22:05:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299776(top)
192.168.1.3:11:10.140.123.0/24
                   *[BGP/170] 06:45:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299776(top)
192.168.1.3:11:10.140.123.3/32
                   *[BGP/170] 06:29:05, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299776(top)
192.168.1.4:9:10.130.40.0/24
                   *[BGP/170] 22:05:50, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 299824(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299792(top)
192.168.1.4:10:10.141.40.0/24
                   *[BGP/170] 06:45:34, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299792(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 1d 01:51:08
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 01:51:19
                       MultiRecv

bgp.evpn.0: 52 destinations, 52 routes (52 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 06:45:45
                       Indirect
1:192.168.1.2:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:45:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:192.168.1.3:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:45:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
2:192.168.1.1:8::110::aa:bb:cc:01:20:00/304 MAC/IP
                   *[EVPN/170] 1d 00:40:34
                       Indirect
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[EVPN/170] 23:54:35
                       Indirect
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 23:24:34
                       Indirect
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[EVPN/170] 07:33:39
                       Indirect
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00/304 MAC/IP
                   *[EVPN/170] 22:01:14
                       Indirect
2:192.168.1.1:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 06:45:46
                       Indirect
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 06:42:26
                       Indirect
2:192.168.1.2:8::110::aa:bb:cc:01:40:00/304 MAC/IP
                   *[BGP/170] 1d 00:40:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 603393
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 23:54:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 23:23:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 22:42:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00/304 MAC/IP
                   *[BGP/170] 22:00:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:45:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 610817
2:192.168.1.2:12::140::aa:bb:cc:01:30:00/304 MAC/IP
                   *[BGP/170] 06:34:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 608001
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[BGP/170] 23:49:54, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[BGP/170] 23:20:38, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.3:10::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:45:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 608257, Push 299776(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 06:29:05, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 605697, Push 299776(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[BGP/170] 23:49:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[BGP/170] 23:19:35, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:54:35
                       Indirect
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[EVPN/170] 23:24:34
                       Indirect
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0::10.130.12.254/304 MAC/IP
                   *[EVPN/170] 07:33:39
                       Indirect
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00::10.130.12.1/304 MAC/IP
                   *[EVPN/170] 21:57:01
                       Indirect
2:192.168.1.1:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[EVPN/170] 06:45:46
                       Indirect
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00::10.140.123.1/304 MAC/IP
                   *[EVPN/170] 06:42:26
                       Indirect
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:54:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[BGP/170] 23:23:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0::10.130.12.254/304 MAC/IP
                   *[BGP/170] 22:42:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00::10.130.12.2/304 MAC/IP
                   *[BGP/170] 21:56:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:45:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 610817
2:192.168.1.2:12::140::aa:bb:cc:01:30:00::10.140.123.2/304 MAC/IP
                   *[BGP/170] 06:34:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 608001
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:49:54, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[BGP/170] 23:20:38, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.3:10::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:45:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 608257, Push 299776(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00::10.140.123.3/304 MAC/IP
                   *[BGP/170] 06:29:05, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 605697, Push 299776(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:49:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[BGP/170] 23:19:35, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
3:192.168.1.1:8::110::192.168.1.1/248 IM
                   *[EVPN/170] 1d 00:46:51
                       Indirect
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[EVPN/170] 23:54:34
                       Indirect
3:192.168.1.1:10::130::192.168.1.1/248 IM
                   *[EVPN/170] 23:00:13
                       Indirect
3:192.168.1.1:12::140::192.168.1.1/248 IM
                   *[EVPN/170] 07:03:51
                       Indirect
3:192.168.1.2:8::110::192.168.1.2/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:192.168.1.2:10::130::192.168.1.2/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:192.168.1.2:12::140::192.168.1.2/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
3:192.168.1.3:10::140::192.168.1.3/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 299824
                       to 172.16.15.0 via ge-0/0/5.0, Push 299792

PURPLE-PILLS-EVPN.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:8::110::aa:bb:cc:01:20:00/304 MAC/IP
                   *[EVPN/170] 1d 00:40:34
                       Indirect
2:192.168.1.2:8::110::aa:bb:cc:01:40:00/304 MAC/IP
                   *[BGP/170] 1d 00:40:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 603393
3:192.168.1.1:8::110::192.168.1.1/248 IM
                   *[EVPN/170] 1d 00:46:51
                       Indirect
3:192.168.1.2:8::110::192.168.1.2/248 IM
                   *[BGP/170] 06:45:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0

__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 06:45:45
                       Indirect

BLUE-HUEPLET-LIMITED.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[EVPN/170] 23:54:36
                       Indirect
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[EVPN/170] 23:24:35
                       Indirect
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 23:54:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 23:23:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[BGP/170] 23:49:55, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[BGP/170] 23:20:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[BGP/170] 23:49:50, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[BGP/170] 23:19:36, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:54:36
                       Indirect
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[EVPN/170] 23:24:35
                       Indirect
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:54:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[BGP/170] 23:23:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 604417
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:49:55, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[BGP/170] 23:20:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299776(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:49:50, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[BGP/170] 23:19:36, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 603393, Push 299824(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 603393, Push 299792(top)
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[EVPN/170] 23:54:35
                       Indirect
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[BGP/170] 06:45:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[BGP/170] 06:45:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[BGP/170] 06:45:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 299824
                       to 172.16.15.0 via ge-0/0/5.0, Push 299792

GREEN-ZALUPA-INCORPORATED-EVPN.evpn.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:10::130::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[EVPN/170] 07:33:40
                       Indirect
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00/304 MAC/IP
                   *[EVPN/170] 22:01:15
                       Indirect
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 22:42:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00/304 MAC/IP
                   *[BGP/170] 22:00:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0::10.130.12.254/304 MAC/IP
                   *[EVPN/170] 07:33:40
                       Indirect
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00::10.130.12.1/304 MAC/IP
                   *[EVPN/170] 21:57:02
                       Indirect
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0::10.130.12.254/304 MAC/IP
                   *[BGP/170] 22:42:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00::10.130.12.2/304 MAC/IP
                   *[BGP/170] 21:56:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 606721
3:192.168.1.1:10::130::192.168.1.1/248 IM
                   *[EVPN/170] 23:00:14
                       Indirect
3:192.168.1.2:10::130::192.168.1.2/248 IM
                   *[BGP/170] 06:45:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0

RED-CUSTOMER-HUYASTOMER-EVPN.evpn.0: 17 destinations, 17 routes (17 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.2:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:45:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
1:192.168.1.3:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:45:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
2:192.168.1.1:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 06:45:47
                       Indirect
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[EVPN/170] 06:42:27
                       Indirect
2:192.168.1.2:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:45:40, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 610817
2:192.168.1.2:12::140::aa:bb:cc:01:30:00/304 MAC/IP
                   *[BGP/170] 06:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 608001
2:192.168.1.3:10::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:45:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 608257, Push 299776(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 06:29:06, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 605697, Push 299776(top)
2:192.168.1.1:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[EVPN/170] 06:45:47
                       Indirect
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00::10.140.123.1/304 MAC/IP
                   *[EVPN/170] 06:42:27
                       Indirect
2:192.168.1.2:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:45:40, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 610817
2:192.168.1.2:12::140::aa:bb:cc:01:30:00::10.140.123.2/304 MAC/IP
                   *[BGP/170] 06:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 608001
2:192.168.1.3:10::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:45:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 608257, Push 299776(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00::10.140.123.3/304 MAC/IP
                   *[BGP/170] 06:29:06, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 605697, Push 299776(top)
3:192.168.1.1:12::140::192.168.1.1/248 IM
                   *[EVPN/170] 07:03:52
                       Indirect
3:192.168.1.2:12::140::192.168.1.2/248 IM
                   *[BGP/170] 06:45:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
3:192.168.1.3:10::140::192.168.1.3/248 IM
                   *[BGP/170] 06:45:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299776
```
### PE2
```
root@PE2> show route | no-more

inet.0: 20 destinations, 25 routes (20 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

10.120.0.0/24      *[Direct/0] 23:55:59
                    >  via irb.120
10.120.0.2/32      *[EVPN/7] 23:25:17
                    >  via irb.120
10.120.0.254/32    *[Local/0] 23:55:59
                       Local via irb.120
172.16.12.0/31     *[Direct/0] 1d 01:03:10
                    >  via ge-0/0/1.0
172.16.12.1/32     *[Local/0] 1d 01:03:10
                       Local via ge-0/0/1.0
172.16.15.0/31     *[OSPF/10] 1d 00:54:34, metric 200
                    >  to 172.16.12.0 via ge-0/0/1.0
172.16.26.0/31     *[Direct/0] 1d 01:03:10
                    >  via ge-0/0/6.0
172.16.26.1/32     *[Local/0] 1d 01:03:10
                       Local via ge-0/0/6.0
172.16.34.0/31     *[OSPF/10] 1d 00:53:42, metric 300
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.35.0/31     *[OSPF/10] 1d 00:53:42, metric 300
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.46.0/31     *[OSPF/10] 1d 00:53:42, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.56.0/31     *[OSPF/10] 1d 00:53:42, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
192.168.1.1/32     @[OSPF/10] 1d 00:54:34, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
                   #[LDP/9] 1d 00:54:34, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.2/32     *[Direct/0] 1d 00:54:47
                    >  via lo0.0
192.168.1.3/32     @[OSPF/10] 1d 00:53:42, metric 300
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:53:42, metric 300
                       to 172.16.12.0 via ge-0/0/1.0, Push 299808
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299824
192.168.1.4/32     @[OSPF/10] 1d 00:53:42, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:53:42, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299808
192.168.1.5/32     @[OSPF/10] 1d 00:53:42, metric 200
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:53:42, metric 200
                       to 172.16.12.0 via ge-0/0/1.0, Push 299792
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299840
192.168.1.6/32     @[OSPF/10] 1d 00:53:42, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:53:42, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 1d 01:03:10, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 01:11:17, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 00:54:34, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.3/32     *[LDP/9] 1d 00:53:42, metric 300
                       to 172.16.12.0 via ge-0/0/1.0, Push 299808
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299824
192.168.1.4/32     *[LDP/9] 1d 00:53:42, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299808
192.168.1.5/32     *[LDP/9] 1d 00:53:42, metric 200
                       to 172.16.12.0 via ge-0/0/1.0, Push 299792
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299840
192.168.1.6/32     *[LDP/9] 1d 00:53:42, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0

GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 6 destinations, 7 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.130.12.0/24     *[Direct/0] 22:44:08
                    >  via irb.130
                    [BGP/170] 22:44:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
10.130.12.1/32     *[BGP/170] 21:58:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
10.130.12.2/32     *[EVPN/7] 21:58:17
                    >  via irb.130
10.130.12.254/32   *[Local/0] 22:44:08
                       Local via irb.130
10.130.30.0/24     *[BGP/170] 22:07:20, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299824(top)
10.130.40.0/24     *[BGP/170] 22:07:24, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299808(top)

RED-CUSTOMER-HUYASTOMER-L3VPN.inet.0: 6 destinations, 8 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.140.123.0/24    *[Direct/0] 06:47:13
                    >  via irb.140
                    [BGP/170] 06:47:13, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
                    [BGP/170] 06:47:13, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299824(top)
10.140.123.1/32    *[BGP/170] 06:44:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
10.140.123.2/32    *[EVPN/7] 06:36:33
                    >  via irb.140
10.140.123.3/32    *[BGP/170] 06:30:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299824(top)
10.140.123.252/32  *[Local/0] 06:47:13
                       Local via irb.140
10.141.40.0/24     *[BGP/170] 06:47:08, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299808(top)

mpls.0: 41 destinations, 41 routes (41 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 01:06:28, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 01:06:28, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 01:11:17, metric 1
                       Receive
2                  *[MPLS/0] 1d 01:06:28, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 01:06:28, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 01:11:17, metric 1
                       Receive
16                 *[VPN/0] 22:48:22
                    >  via lsi.0 (GREEN-ZALUPA-INCORPORATED-L3VPN), Pop
17                 *[VPN/0] 06:47:13
                    >  via lsi.1 (RED-CUSTOMER-HUYASTOMER-L3VPN), Pop
299776             *[LDP/9] 1d 00:54:44, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Pop
299776(S=0)        *[LDP/9] 1d 00:54:44, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Pop
299792             *[LDP/9] 1d 00:53:42, metric 1
                       to 172.16.12.0 via ge-0/0/1.0, Swap 299792
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 299840
299808             *[LDP/9] 1d 00:53:42, metric 1
                       to 172.16.12.0 via ge-0/0/1.0, Swap 299808
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 299824
299824             *[LDP/9] 1d 00:53:42, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 299808
299840             *[LDP/9] 1d 00:53:52, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Pop
299840(S=0)        *[LDP/9] 1d 00:53:52, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Pop
299856             *[EVPN/7] 1d 00:41:59, routing-instance PURPLE-PILLS-EVPN, route-type Ingress-MAC, vlan-id 110
                       to table PURPLE-PILLS-EVPN.evpn-mac.0
299872             *[EVPN/7] 1d 00:48:28, routing-instance PURPLE-PILLS-EVPN, route-type Ingress-IM, vlan-id 110
                       to table PURPLE-PILLS-EVPN.evpn-mac.0
299888             *[EVPN/7] 1d 00:48:25, remote-pe 192.168.1.1, routing-instance PURPLE-PILLS-EVPN, route-type Egress-IM, vlan-id 110
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299888
299904             *[EVPN/7] 1d 00:42:09, remote-pe 192.168.1.1, routing-instance PURPLE-PILLS-EVPN, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299856
299920             *[EVPN/7] 23:56:00, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-MAC, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
299952             *[EVPN/7] 23:56:00, remote-pe 192.168.1.1, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299920
299968             *[EVPN/7] 23:56:00, remote-pe 192.168.1.1, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299952
299984             *[EVPN/7] 23:55:59, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-IM, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
300000             *[EVPN/7] 23:51:28, remote-pe 192.168.1.3, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299856, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 299856, Push 299824(top)
300016             *[EVPN/7] 23:51:27, remote-pe 192.168.1.3, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299952, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 299952, Push 299824(top)
300032             *[EVPN/7] 23:51:24, remote-pe 192.168.1.4, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299856, Push 299808(top)
300048             *[EVPN/7] 23:51:23, remote-pe 192.168.1.4, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299984, Push 299808(top)
300064             *[EVPN/7] 22:54:53, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Ingress-MAC, vlan-id 130
                       to table GREEN-ZALUPA-INCORPORATED-EVPN.evpn-mac.0
300096             *[EVPN/7] 23:01:38, remote-pe 192.168.1.1, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Egress-IM, vlan-id 130
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300096
300112             *[EVPN/7] 23:01:37, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Ingress-IM, vlan-id 130
                       to table GREEN-ZALUPA-INCORPORATED-EVPN.evpn-mac.0
300128             *[EVPN/7] 22:54:55, remote-pe 192.168.1.1, routing-instance GREEN-ZALUPA-INCORPORATED-EVPN, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300064
300144             *[EVPN/7] 06:36:34, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-MAC, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300160             *[EVPN/7] 06:47:17, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:8c:00
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300288
                       to 172.16.12.0 via ge-0/0/1.0, Push 300160, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 300160, Push 299824(top)
300224             *[EVPN/7] 07:05:01, remote-pe 192.168.1.1, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-IM, vlan-id 140
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300208
300240             *[EVPN/7] 07:04:59, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-IM, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300272             *[EVPN/7] 07:04:41, remote-pe 192.168.1.3, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-IM, vlan-id 140
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300128, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 300128, Push 299824(top)
300288             *[EVPN/7] 06:47:19, remote-pe 192.168.1.1, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300288
300304             *[EVPN/7] 06:47:17, remote-pe 192.168.1.3, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                       to 172.16.12.0 via ge-0/0/1.0, Push 300160, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300160, Push 299824(top)
300320             *[EVPN/7] 06:47:14, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-MAC, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300352             *[EVPN/7] 06:44:01, remote-pe 192.168.1.1, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 300144
300368             *[EVPN/7] 06:30:40, remote-pe 192.168.1.3, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                       to 172.16.12.0 via ge-0/0/1.0, Push 300000, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300000, Push 299824(top)

bgp.l3vpn.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1:11:10.130.12.0/24
                   *[BGP/170] 22:44:06, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.1:11:10.130.12.1/32
                   *[BGP/170] 21:58:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.1:13:10.140.123.0/24
                   *[BGP/170] 06:47:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
192.168.1.1:13:10.140.123.1/32
                   *[BGP/170] 06:44:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 17
192.168.1.3:9:10.130.30.0/24
                   *[BGP/170] 22:07:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299824(top)
192.168.1.3:11:10.140.123.0/24
                   *[BGP/170] 06:47:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299824(top)
192.168.1.3:11:10.140.123.3/32
                   *[BGP/170] 06:30:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299824(top)
192.168.1.4:9:10.130.40.0/24
                   *[BGP/170] 22:07:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299808(top)
192.168.1.4:10:10.141.40.0/24
                   *[BGP/170] 06:47:09, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299808(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 1d 01:52:37
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 01:52:48
                       MultiRecv

bgp.evpn.0: 52 destinations, 52 routes (52 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 06:47:13
                       Indirect
1:192.168.1.3:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 299808
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299824
2:192.168.1.1:8::110::aa:bb:cc:01:20:00/304 MAC/IP
                   *[BGP/170] 1d 00:42:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 23:56:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 23:26:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 07:35:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00/304 MAC/IP
                   *[BGP/170] 22:02:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.1:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 610305
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 06:44:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 608001
2:192.168.1.2:8::110::aa:bb:cc:01:40:00/304 MAC/IP
                   *[EVPN/170] 1d 00:42:00
                       Indirect
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[EVPN/170] 23:56:00
                       Indirect
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 23:25:18
                       Indirect
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[EVPN/170] 22:44:09
                       Indirect
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00/304 MAC/IP
                   *[EVPN/170] 22:02:19
                       Indirect
2:192.168.1.2:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 06:47:14
                       Indirect
2:192.168.1.2:12::140::aa:bb:cc:01:30:00/304 MAC/IP
                   *[EVPN/170] 06:36:34
                       Indirect
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[BGP/170] 23:51:28, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[BGP/170] 23:22:13, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.3:10::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 608257, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 608257, Push 299824(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 06:30:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 605697, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 605697, Push 299824(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[BGP/170] 23:51:24, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[BGP/170] 23:21:10, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:56:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[BGP/170] 23:26:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0::10.130.12.254/304 MAC/IP
                   *[BGP/170] 07:35:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00::10.130.12.1/304 MAC/IP
                   *[BGP/170] 21:58:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.1:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 610305
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00::10.140.123.1/304 MAC/IP
                   *[BGP/170] 06:44:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 608001
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:56:00
                       Indirect
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[EVPN/170] 23:25:18
                       Indirect
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0::10.130.12.254/304 MAC/IP
                   *[EVPN/170] 22:44:09
                       Indirect
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00::10.130.12.2/304 MAC/IP
                   *[EVPN/170] 21:58:18
                       Indirect
2:192.168.1.2:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[EVPN/170] 06:47:14
                       Indirect
2:192.168.1.2:12::140::aa:bb:cc:01:30:00::10.140.123.2/304 MAC/IP
                   *[EVPN/170] 06:36:34
                       Indirect
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:28, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[BGP/170] 23:22:13, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.3:10::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 608257, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 608257, Push 299824(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00::10.140.123.3/304 MAC/IP
                   *[BGP/170] 06:30:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 605697, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 605697, Push 299824(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:24, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[BGP/170] 23:21:10, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
3:192.168.1.1:8::110::192.168.1.1/248 IM
                   *[BGP/170] 06:47:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[BGP/170] 06:47:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:192.168.1.1:10::130::192.168.1.1/248 IM
                   *[BGP/170] 06:47:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:192.168.1.1:12::140::192.168.1.1/248 IM
                   *[BGP/170] 06:36:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 609024
3:192.168.1.2:8::110::192.168.1.2/248 IM
                   *[EVPN/170] 1d 00:48:28
                       Indirect
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[EVPN/170] 23:55:59
                       Indirect
3:192.168.1.2:10::130::192.168.1.2/248 IM
                   *[EVPN/170] 23:01:37
                       Indirect
3:192.168.1.2:12::140::192.168.1.2/248 IM
                   *[EVPN/170] 07:04:59
                       Indirect
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[BGP/170] 06:47:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299808
                       to 172.16.26.0 via ge-0/0/6.0, Push 299824
3:192.168.1.3:10::140::192.168.1.3/248 IM
                   *[BGP/170] 06:36:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 607744, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 607744, Push 299824(top)
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[BGP/170] 06:47:15, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299808

PURPLE-PILLS-EVPN.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:8::110::aa:bb:cc:01:20:00/304 MAC/IP
                   *[BGP/170] 1d 00:42:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393
2:192.168.1.2:8::110::aa:bb:cc:01:40:00/304 MAC/IP
                   *[EVPN/170] 1d 00:42:01
                       Indirect
3:192.168.1.1:8::110::192.168.1.1/248 IM
                   *[BGP/170] 06:47:15, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:192.168.1.2:8::110::192.168.1.2/248 IM
                   *[EVPN/170] 1d 00:48:29
                       Indirect

__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.2:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 06:47:14
                       Indirect

BLUE-HUEPLET-LIMITED.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 23:56:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 23:26:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[EVPN/170] 23:56:01
                       Indirect
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[EVPN/170] 23:25:19
                       Indirect
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[BGP/170] 23:51:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[BGP/170] 23:22:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[BGP/170] 23:51:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[BGP/170] 23:21:11, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:56:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[BGP/170] 23:26:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 604417
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:56:01
                       Indirect
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[EVPN/170] 23:25:19
                       Indirect
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[BGP/170] 23:22:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 603393, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299824(top)
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[BGP/170] 23:21:11, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 603393, Push 299808(top)
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[BGP/170] 06:47:15, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[EVPN/170] 23:56:00
                       Indirect
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[BGP/170] 06:47:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 299808
                       to 172.16.26.0 via ge-0/0/6.0, Push 299824
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[BGP/170] 06:47:15, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299808

GREEN-ZALUPA-INCORPORATED-EVPN.evpn.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:10::130::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 07:35:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00/304 MAC/IP
                   *[BGP/170] 22:02:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[EVPN/170] 22:44:11
                       Indirect
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00/304 MAC/IP
                   *[EVPN/170] 22:02:21
                       Indirect
2:192.168.1.1:10::130::2c:6b:f5:80:67:f0::10.130.12.254/304 MAC/IP
                   *[BGP/170] 07:35:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.1:10::130::aa:bb:cc:00:e0:00::10.130.12.1/304 MAC/IP
                   *[BGP/170] 21:58:37, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 606721
2:192.168.1.2:10::130::2c:6b:f5:3f:ad:f0::10.130.12.254/304 MAC/IP
                   *[EVPN/170] 22:44:11
                       Indirect
2:192.168.1.2:10::130::aa:bb:cc:00:f0:00::10.130.12.2/304 MAC/IP
                   *[EVPN/170] 21:58:20
                       Indirect
3:192.168.1.1:10::130::192.168.1.1/248 IM
                   *[BGP/170] 06:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
3:192.168.1.2:10::130::192.168.1.2/248 IM
                   *[EVPN/170] 23:01:39
                       Indirect

RED-CUSTOMER-HUYASTOMER-EVPN.evpn.0: 17 destinations, 17 routes (17 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
1:192.168.1.3:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:19, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 299808
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299824
2:192.168.1.1:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 610305
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 06:44:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 608001
2:192.168.1.2:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 06:47:16
                       Indirect
2:192.168.1.2:12::140::aa:bb:cc:01:30:00/304 MAC/IP
                   *[EVPN/170] 06:36:36
                       Indirect
2:192.168.1.3:10::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:20, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 608257, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 608257, Push 299824(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 06:30:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 605697, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 605697, Push 299824(top)
2:192.168.1.1:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 610305
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00::10.140.123.1/304 MAC/IP
                   *[BGP/170] 06:44:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 608001
2:192.168.1.2:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[EVPN/170] 06:47:16
                       Indirect
2:192.168.1.2:12::140::aa:bb:cc:01:30:00::10.140.123.2/304 MAC/IP
                   *[EVPN/170] 06:36:36
                       Indirect
2:192.168.1.3:10::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:20, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 608257, Push 299808(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 608257, Push 299824(top)
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00::10.140.123.3/304 MAC/IP
                   *[BGP/170] 06:30:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 605697, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 605697, Push 299824(top)
3:192.168.1.1:12::140::192.168.1.1/248 IM
                   *[BGP/170] 06:36:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 609024
3:192.168.1.2:12::140::192.168.1.2/248 IM
                   *[EVPN/170] 07:05:01
                       Indirect
3:192.168.1.3:10::140::192.168.1.3/248 IM
                   *[BGP/170] 06:36:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 607744, Push 299808(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 607744, Push 299824(top)
```
### PE3
```
root@PE3> show route | no-more

inet.0: 20 destinations, 25 routes (20 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

10.120.0.0/24      *[Direct/0] 23:51:57
                    >  via irb.120
10.120.0.3/32      *[EVPN/7] 23:22:41
                    >  via irb.120
10.120.0.254/32    *[Local/0] 23:51:57
                       Local via irb.120
172.16.12.0/31     *[OSPF/10] 1d 00:54:26, metric 300
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.15.0/31     *[OSPF/10] 1d 00:54:26, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.26.0/31     *[OSPF/10] 1d 00:54:11, metric 300
                    >  to 172.16.34.1 via ge-0/0/4.0
                       to 172.16.35.0 via ge-0/0/5.0
172.16.34.0/31     *[Direct/0] 1d 01:03:23
                    >  via ge-0/0/4.0
172.16.34.0/32     *[Local/0] 1d 01:03:23
                       Local via ge-0/0/4.0
172.16.35.0/31     *[Direct/0] 1d 01:03:23
                    >  via ge-0/0/5.0
172.16.35.1/32     *[Local/0] 1d 01:03:23
                       Local via ge-0/0/5.0
172.16.46.0/31     *[OSPF/10] 1d 00:54:40, metric 200
                    >  to 172.16.34.1 via ge-0/0/4.0
172.16.56.0/31     *[OSPF/10] 1d 00:54:26, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.1.1/32     @[OSPF/10] 1d 00:54:26, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:54:26, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
192.168.1.2/32     @[OSPF/10] 1d 00:54:11, metric 300
                       to 172.16.34.1 via ge-0/0/4.0
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:54:11, metric 300
                       to 172.16.34.1 via ge-0/0/4.0, Push 299824
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299824
192.168.1.3/32     *[Direct/0] 1d 00:55:03
                    >  via lo0.0
192.168.1.4/32     @[OSPF/10] 1d 00:54:40, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
                   #[LDP/9] 1d 00:54:40, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
192.168.1.5/32     @[OSPF/10] 1d 00:54:26, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:54:26, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.1.6/32     @[OSPF/10] 1d 00:54:11, metric 200
                       to 172.16.34.1 via ge-0/0/4.0
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:54:11, metric 200
                       to 172.16.34.1 via ge-0/0/4.0, Push 299840
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299840
224.0.0.2/32       *[LDP/9] 1d 01:03:23, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 01:10:20, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 00:54:26, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
192.168.1.2/32     *[LDP/9] 1d 00:54:11, metric 300
                       to 172.16.34.1 via ge-0/0/4.0, Push 299824
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299824
192.168.1.4/32     *[LDP/9] 1d 00:54:40, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
192.168.1.5/32     *[LDP/9] 1d 00:54:26, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.1.6/32     *[LDP/9] 1d 00:54:11, metric 200
                       to 172.16.34.1 via ge-0/0/4.0, Push 299840
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299840

GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 6 destinations, 7 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.130.12.0/24     *[BGP/170] 22:25:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299808(top)
                    [BGP/170] 22:25:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299824(top)
10.130.12.1/32     *[BGP/170] 21:59:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299808(top)
10.130.12.2/32     *[BGP/170] 21:58:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299824(top)
10.130.30.0/24     *[Direct/0] 22:07:49
                    >  via ge-0/0/8.130
10.130.30.254/32   *[Local/0] 22:07:49
                       Local via ge-0/0/8.130
10.130.40.0/24     *[BGP/170] 22:07:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16

RED-CUSTOMER-HUYASTOMER-L3VPN.inet.0: 6 destinations, 8 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.140.123.0/24    *[Direct/0] 06:47:46
                    >  via irb.140
                    [BGP/170] 06:47:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299808(top)
                    [BGP/170] 06:47:42, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299824(top)
10.140.123.1/32    *[BGP/170] 06:44:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299808(top)
10.140.123.2/32    *[BGP/170] 06:37:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299824(top)
10.140.123.3/32    *[EVPN/7] 06:31:08
                    >  via irb.140
10.140.123.253/32  *[Local/0] 06:47:46
                       Local via irb.140
10.141.40.0/24     *[BGP/170] 06:47:37, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17

mpls.0: 33 destinations, 33 routes (33 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 01:07:05, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 01:07:05, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 01:10:20, metric 1
                       Receive
2                  *[MPLS/0] 1d 01:07:05, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 01:07:05, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 01:10:20, metric 1
                       Receive
16                 *[VPN/0] 22:25:28
                    >  via lsi.0 (GREEN-ZALUPA-INCORPORATED-L3VPN), Pop
17                 *[VPN/0] 06:47:46
                    >  via lsi.1 (RED-CUSTOMER-HUYASTOMER-L3VPN), Pop
299776             *[LDP/9] 1d 00:54:50, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Pop
299776(S=0)        *[LDP/9] 1d 00:54:50, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Pop
299792             *[LDP/9] 1d 00:54:37, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Pop
299792(S=0)        *[LDP/9] 1d 00:54:37, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Pop
299808             *[LDP/9] 1d 00:54:36, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Swap 299808
299824             *[LDP/9] 1d 00:54:11, metric 1
                       to 172.16.34.1 via ge-0/0/4.0, Swap 299824
                    >  to 172.16.35.0 via ge-0/0/5.0, Swap 299824
299840             *[LDP/9] 1d 00:54:21, metric 1
                       to 172.16.34.1 via ge-0/0/4.0, Swap 299840
                    >  to 172.16.35.0 via ge-0/0/5.0, Swap 299840
299856             *[EVPN/7] 23:51:57, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-MAC, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
299888             *[EVPN/7] 23:51:56, remote-pe 192.168.1.1, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299920, Push 299808(top)
299904             *[EVPN/7] 23:51:56, remote-pe 192.168.1.2, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299920, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 299920, Push 299824(top)
299920             *[EVPN/7] 23:51:56, remote-pe 192.168.1.1, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299952, Push 299808(top)
299936             *[EVPN/7] 23:51:56, remote-pe 192.168.1.2, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299984, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 299984, Push 299824(top)
299952             *[EVPN/7] 23:51:55, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-IM, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
299968             *[EVPN/7] 23:51:52, remote-pe 192.168.1.4, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299856
299984             *[EVPN/7] 23:51:51, remote-pe 192.168.1.4, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299984
300000             *[EVPN/7] 06:31:08, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-MAC, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300016             *[EVPN/7] 06:47:41, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC, ESI 05:00:00:ff:dc:00:00:00:8c:00
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 300288, Push 299808(top)
                       to 172.16.34.1 via ge-0/0/4.0, Push 300320, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 300320, Push 299824(top)
300080             *[EVPN/7] 07:05:10, remote-pe 192.168.1.2, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-IM, vlan-id 140
                       to 172.16.34.1 via ge-0/0/4.0, Push 300240, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 300240, Push 299824(top)
300112             *[EVPN/7] 07:05:10, remote-pe 192.168.1.1, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-IM, vlan-id 140
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 300208, Push 299808(top)
300128             *[EVPN/7] 07:05:09, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-IM, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300144             *[EVPN/7] 06:47:47, remote-pe 192.168.1.1, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 300288, Push 299808(top)
300160             *[EVPN/7] 06:47:46, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Ingress-MAC, vlan-id 140
                       to table RED-CUSTOMER-HUYASTOMER-EVPN.evpn-mac.0
300192             *[EVPN/7] 06:47:41, remote-pe 192.168.1.2, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300320, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 300320, Push 299824(top)
300208             *[EVPN/7] 06:44:29, remote-pe 192.168.1.1, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 300144, Push 299808(top)
300224             *[EVPN/7] 06:37:02, remote-pe 192.168.1.2, routing-instance RED-CUSTOMER-HUYASTOMER-EVPN, route-type Egress-MAC
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 300144, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 300144, Push 299824(top)

bgp.l3vpn.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1:11:10.130.12.0/24
                   *[BGP/170] 22:25:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299808(top)
192.168.1.1:11:10.130.12.1/32
                   *[BGP/170] 21:59:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299808(top)
192.168.1.1:13:10.140.123.0/24
                   *[BGP/170] 06:47:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299808(top)
192.168.1.1:13:10.140.123.1/32
                   *[BGP/170] 06:44:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299808(top)
192.168.1.2:11:10.130.12.0/24
                   *[BGP/170] 22:25:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299824(top)
192.168.1.2:11:10.130.12.2/32
                   *[BGP/170] 21:58:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299824(top)
192.168.1.2:13:10.140.123.0/24
                   *[BGP/170] 06:47:42, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299824(top)
192.168.1.2:13:10.140.123.2/32
                   *[BGP/170] 06:37:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299824(top)
192.168.1.4:9:10.130.40.0/24
                   *[BGP/170] 22:07:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.1.4:10:10.141.40.0/24
                   *[BGP/170] 06:47:37, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 1d 01:52:56
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 01:53:07
                       MultiRecv

bgp.evpn.0: 38 destinations, 38 routes (38 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:48, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
1:192.168.1.2:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:42, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299824
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299824
1:192.168.1.3:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 06:47:46
                       Indirect
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 23:26:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.1:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 610305, Push 299808(top)
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 06:44:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299808(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 23:25:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.2:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 610817, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 610817, Push 299824(top)
2:192.168.1.2:12::140::aa:bb:cc:01:30:00/304 MAC/IP
                   *[BGP/170] 06:37:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 608001, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299824(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[EVPN/170] 23:51:58
                       Indirect
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[EVPN/170] 23:22:42
                       Indirect
2:192.168.1.3:10::140::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 06:47:47
                       Indirect
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 06:31:09
                       Indirect
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[BGP/170] 23:51:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[BGP/170] 23:21:39, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[BGP/170] 23:26:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.1:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 610305, Push 299808(top)
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00::10.140.123.1/304 MAC/IP
                   *[BGP/170] 06:44:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299808(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[BGP/170] 23:25:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.2:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 610817, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 610817, Push 299824(top)
2:192.168.1.2:12::140::aa:bb:cc:01:30:00::10.140.123.2/304 MAC/IP
                   *[BGP/170] 06:37:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 608001, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299824(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:51:58
                       Indirect
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[EVPN/170] 23:22:42
                       Indirect
2:192.168.1.3:10::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[EVPN/170] 06:47:47
                       Indirect
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00::10.140.123.3/304 MAC/IP
                   *[EVPN/170] 06:31:09
                       Indirect
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[BGP/170] 23:21:39, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
3:192.168.1.1:12::140::192.168.1.1/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299824
                       to 172.16.35.0 via ge-0/0/5.0, Push 299824
3:192.168.1.2:12::140::192.168.1.2/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299824
                       to 172.16.35.0 via ge-0/0/5.0, Push 299824
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[EVPN/170] 23:51:56
                       Indirect
3:192.168.1.3:10::140::192.168.1.3/248 IM
                   *[EVPN/170] 07:05:10
                       Indirect
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0

BLUE-HUEPLET-LIMITED.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 23:26:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 23:25:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[EVPN/170] 23:51:58
                       Indirect
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[EVPN/170] 23:22:42
                       Indirect
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[BGP/170] 23:51:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[BGP/170] 23:21:39, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[BGP/170] 23:26:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299808(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[BGP/170] 23:25:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 604417, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 604417, Push 299824(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:51:58
                       Indirect
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[EVPN/170] 23:22:42
                       Indirect
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:51:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[BGP/170] 23:21:39, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 603393
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299824
                       to 172.16.35.0 via ge-0/0/5.0, Push 299824
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[EVPN/170] 23:51:56
                       Indirect
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0

__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 06:47:46
                       Indirect

RED-CUSTOMER-HUYASTOMER-EVPN.evpn.0: 17 destinations, 17 routes (17 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:48, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
1:192.168.1.2:0::050000ffdc0000008c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 06:47:42, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 299824
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299824
2:192.168.1.1:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 610305, Push 299808(top)
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00/304 MAC/IP
                   *[BGP/170] 06:44:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299808(top)
2:192.168.1.2:12::140::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 06:47:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 610817, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 610817, Push 299824(top)
2:192.168.1.2:12::140::aa:bb:cc:01:30:00/304 MAC/IP
                   *[BGP/170] 06:37:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 608001, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299824(top)
2:192.168.1.3:10::140::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 06:47:47
                       Indirect
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 06:31:09
                       Indirect
2:192.168.1.1:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 610305, Push 299808(top)
2:192.168.1.1:12::140::aa:bb:cc:00:b0:00::10.140.123.1/304 MAC/IP
                   *[BGP/170] 06:44:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299808(top)
2:192.168.1.2:12::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[BGP/170] 06:47:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 610817, Push 299824(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 610817, Push 299824(top)
2:192.168.1.2:12::140::aa:bb:cc:01:30:00::10.140.123.2/304 MAC/IP
                   *[BGP/170] 06:37:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 608001, Push 299824(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 608001, Push 299824(top)
2:192.168.1.3:10::140::00:00:5e:00:01:01::10.140.123.254/304 MAC/IP
                   *[EVPN/170] 06:47:47
                       Indirect
2:192.168.1.3:10::140::aa:bb:cc:00:c0:00::10.140.123.3/304 MAC/IP
                   *[EVPN/170] 06:31:09
                       Indirect
3:192.168.1.1:12::140::192.168.1.1/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299808
3:192.168.1.2:12::140::192.168.1.2/248 IM
                   *[BGP/170] 06:47:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 299824
                       to 172.16.35.0 via ge-0/0/5.0, Push 299824
3:192.168.1.3:10::140::192.168.1.3/248 IM
                   *[EVPN/170] 07:05:10
                       Indirect
```
### PE4
```
root@PE4> show route | no-more

inet.0: 20 destinations, 25 routes (20 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

10.120.0.0/24      *[Direct/0] 23:52:34
                    >  via irb.120
10.120.0.4/32      *[EVPN/7] 23:22:20
                    >  via irb.120
10.120.0.254/32    *[Local/0] 23:52:34
                       Local via irb.120
172.16.12.0/31     *[OSPF/10] 1d 00:54:53, metric 300
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.15.0/31     *[OSPF/10] 1d 00:54:53, metric 300
                    >  to 172.16.34.0 via ge-0/0/3.0
                       to 172.16.46.0 via ge-0/0/6.0
172.16.26.0/31     *[OSPF/10] 1d 00:54:53, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.34.0/31     *[Direct/0] 1d 01:03:31
                    >  via ge-0/0/3.0
172.16.34.1/32     *[Local/0] 1d 01:03:31
                       Local via ge-0/0/3.0
172.16.35.0/31     *[OSPF/10] 1d 00:55:22, metric 200
                    >  to 172.16.34.0 via ge-0/0/3.0
172.16.46.0/31     *[Direct/0] 1d 01:03:31
                    >  via ge-0/0/6.0
172.16.46.1/32     *[Local/0] 1d 01:03:31
                       Local via ge-0/0/6.0
172.16.56.0/31     *[OSPF/10] 1d 00:54:53, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
192.168.1.1/32     @[OSPF/10] 1d 00:54:53, metric 300
                       to 172.16.34.0 via ge-0/0/3.0
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:54:53, metric 300
                       to 172.16.34.0 via ge-0/0/3.0, Push 299808
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299792
192.168.1.2/32     @[OSPF/10] 1d 00:54:53, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:54:53, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299776
192.168.1.3/32     @[OSPF/10] 1d 00:55:22, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
                   #[LDP/9] 1d 00:55:22, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
192.168.1.4/32     *[Direct/0] 1d 00:55:33
                    >  via lo0.0
192.168.1.5/32     @[OSPF/10] 1d 00:54:53, metric 200
                       to 172.16.34.0 via ge-0/0/3.0
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:54:53, metric 200
                       to 172.16.34.0 via ge-0/0/3.0, Push 299792
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299840
192.168.1.6/32     @[OSPF/10] 1d 00:54:53, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 00:54:53, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 1d 01:03:31, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 01:10:22, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 00:54:53, metric 300
                       to 172.16.34.0 via ge-0/0/3.0, Push 299808
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299792
192.168.1.2/32     *[LDP/9] 1d 00:54:53, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299776
192.168.1.3/32     *[LDP/9] 1d 00:55:22, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
192.168.1.5/32     *[LDP/9] 1d 00:54:53, metric 200
                       to 172.16.34.0 via ge-0/0/3.0, Push 299792
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299840
192.168.1.6/32     *[LDP/9] 1d 00:54:53, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0

GREEN-ZALUPA-INCORPORATED-L3VPN.inet.0: 6 destinations, 7 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.130.12.0/24     *[BGP/170] 22:26:15, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299776(top)
                    [BGP/170] 22:26:15, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299792(top)
10.130.12.1/32     *[BGP/170] 21:59:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299792(top)
10.130.12.2/32     *[BGP/170] 21:59:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299776(top)
10.130.30.0/24     *[BGP/170] 22:08:31, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
10.130.40.0/24     *[Direct/0] 22:08:35
                    >  via ge-0/0/8.130
10.130.40.254/32   *[Local/0] 22:08:35
                       Local via ge-0/0/8.130

RED-CUSTOMER-HUYASTOMER-L3VPN.inet.0: 6 destinations, 8 routes (6 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.140.123.0/24    *[BGP/170] 06:48:19, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
                    [BGP/170] 06:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299776(top)
                    [BGP/170] 06:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299792(top)
10.140.123.1/32    *[BGP/170] 06:45:11, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299792(top)
10.140.123.2/32    *[BGP/170] 06:37:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299776(top)
10.140.123.3/32    *[BGP/170] 06:31:50, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
10.141.40.0/24     *[Direct/0] 06:48:20
                    >  via ge-0/0/9.141
10.141.40.254/32   *[Local/0] 06:48:20
                       Local via ge-0/0/9.141

mpls.0: 23 destinations, 23 routes (23 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 01:07:59, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 01:07:59, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 01:10:22, metric 1
                       Receive
2                  *[MPLS/0] 1d 01:07:59, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 01:07:59, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 01:10:22, metric 1
                       Receive
16                 *[VPN/0] 22:26:16
                    >  via lsi.0 (GREEN-ZALUPA-INCORPORATED-L3VPN), Pop
17                 *[VPN/0] 06:48:20
                    >  via lsi.1 (RED-CUSTOMER-HUYASTOMER-L3VPN), Pop
299776             *[LDP/9] 1d 00:55:32, metric 1
                    >  to 172.16.34.0 via ge-0/0/3.0, Pop
299776(S=0)        *[LDP/9] 1d 00:55:32, metric 1
                    >  to 172.16.34.0 via ge-0/0/3.0, Pop
299792             *[LDP/9] 1d 00:54:53, metric 1
                       to 172.16.34.0 via ge-0/0/3.0, Swap 299792
                    >  to 172.16.46.0 via ge-0/0/6.0, Swap 299840
299808             *[LDP/9] 1d 00:54:53, metric 1
                       to 172.16.34.0 via ge-0/0/3.0, Swap 299808
                    >  to 172.16.46.0 via ge-0/0/6.0, Swap 299792
299824             *[LDP/9] 1d 00:54:53, metric 1
                    >  to 172.16.46.0 via ge-0/0/6.0, Swap 299776
299840             *[LDP/9] 1d 00:55:04, metric 1
                    >  to 172.16.46.0 via ge-0/0/6.0, Pop
299840(S=0)        *[LDP/9] 1d 00:55:04, metric 1
                    >  to 172.16.46.0 via ge-0/0/6.0, Pop
299856             *[EVPN/7] 23:52:34, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-MAC, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0
299888             *[EVPN/7] 23:52:34, remote-pe 192.168.1.1, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                       to 172.16.34.0 via ge-0/0/3.0, Push 299920, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299920, Push 299792(top)
299904             *[EVPN/7] 23:52:34, remote-pe 192.168.1.2, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299920, Push 299776(top)
299920             *[EVPN/7] 23:52:34, remote-pe 192.168.1.1, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 299952, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 299952, Push 299792(top)
299936             *[EVPN/7] 23:52:34, remote-pe 192.168.1.2, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299984, Push 299776(top)
299952             *[EVPN/7] 23:52:34, remote-pe 192.168.1.3, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-MAC
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 299856
299968             *[EVPN/7] 23:52:34, remote-pe 192.168.1.3, routing-instance BLUE-HUEPLET-LIMITED, route-type Egress-IM, vlan-id 120
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 299952
299984             *[EVPN/7] 23:52:33, routing-instance BLUE-HUEPLET-LIMITED, route-type Ingress-IM, vlan-id 120
                       to table BLUE-HUEPLET-LIMITED.evpn-mac.0

bgp.l3vpn.0: 11 destinations, 11 routes (11 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1:11:10.130.12.0/24
                   *[BGP/170] 22:26:15, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299792(top)
192.168.1.1:11:10.130.12.1/32
                   *[BGP/170] 21:59:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299792(top)
192.168.1.1:13:10.140.123.0/24
                   *[BGP/170] 06:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299792(top)
192.168.1.1:13:10.140.123.1/32
                   *[BGP/170] 06:45:11, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 17, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299792(top)
192.168.1.2:11:10.130.12.0/24
                   *[BGP/170] 22:26:15, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299776(top)
192.168.1.2:11:10.130.12.2/32
                   *[BGP/170] 21:59:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299776(top)
192.168.1.2:13:10.140.123.0/24
                   *[BGP/170] 06:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299776(top)
192.168.1.2:13:10.140.123.2/32
                   *[BGP/170] 06:37:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299776(top)
192.168.1.3:9:10.130.30.0/24
                   *[BGP/170] 22:08:31, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
192.168.1.3:11:10.140.123.0/24
                   *[BGP/170] 06:48:19, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
192.168.1.3:11:10.140.123.3/32
                   *[BGP/170] 06:31:50, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe04:0/128
                   *[Local/0] 1d 01:53:39
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 01:53:50
                       MultiRecv

bgp.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 23:52:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 23:27:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 23:52:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 23:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[BGP/170] 23:52:34, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[BGP/170] 23:23:23, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[EVPN/170] 23:52:34
                       Indirect
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[EVPN/170] 23:22:20
                       Indirect
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:52:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[BGP/170] 23:27:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:52:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[BGP/170] 23:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:52:34, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[BGP/170] 23:23:23, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:52:34
                       Indirect
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[EVPN/170] 23:22:20
                       Indirect
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[BGP/170] 06:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 299808
                       to 172.16.46.0 via ge-0/0/6.0, Push 299792
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[BGP/170] 06:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299776
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[BGP/170] 06:48:19, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[EVPN/170] 23:52:33
                       Indirect

BLUE-HUEPLET-LIMITED.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2:192.168.1.1:9::120::2c:6b:f5:80:67:f0/304 MAC/IP
                   *[BGP/170] 23:52:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00/304 MAC/IP
                   *[BGP/170] 23:27:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0/304 MAC/IP
                   *[BGP/170] 23:52:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00/304 MAC/IP
                   *[BGP/170] 23:26:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0/304 MAC/IP
                   *[BGP/170] 23:52:35, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.3:8::120::aa:bb:cc:00:90:00/304 MAC/IP
                   *[BGP/170] 23:23:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0/304 MAC/IP
                   *[EVPN/170] 23:52:35
                       Indirect
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00/304 MAC/IP
                   *[EVPN/170] 23:22:21
                       Indirect
2:192.168.1.1:9::120::2c:6b:f5:80:67:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:52:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.1:9::120::aa:bb:cc:00:70:00::10.120.0.1/304 MAC/IP
                   *[BGP/170] 23:27:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 604417, Push 299808(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299792(top)
2:192.168.1.2:9::120::2c:6b:f5:3f:ad:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:52:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.2:9::120::aa:bb:cc:00:80:00::10.120.0.2/304 MAC/IP
                   *[BGP/170] 23:26:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 604417, Push 299776(top)
2:192.168.1.3:8::120::2c:6b:f5:e0:f9:f0::10.120.0.254/304 MAC/IP
                   *[BGP/170] 23:52:35, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.3:8::120::aa:bb:cc:00:90:00::10.120.0.3/304 MAC/IP
                   *[BGP/170] 23:23:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 603393
2:192.168.1.4:8::120::2c:6b:f5:c0:e1:f0::10.120.0.254/304 MAC/IP
                   *[EVPN/170] 23:52:35
                       Indirect
2:192.168.1.4:8::120::aa:bb:cc:00:a0:00::10.120.0.4/304 MAC/IP
                   *[EVPN/170] 23:22:21
                       Indirect
3:192.168.1.1:9::120::192.168.1.1/248 IM
                   *[BGP/170] 06:48:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 299808
                       to 172.16.46.0 via ge-0/0/6.0, Push 299792
3:192.168.1.2:9::120::192.168.1.2/248 IM
                   *[BGP/170] 06:48:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299776
3:192.168.1.3:8::120::192.168.1.3/248 IM
                   *[BGP/170] 06:48:20, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0
3:192.168.1.4:8::120::192.168.1.4/248 IM
                   *[EVPN/170] 23:52:34
                       Indirect
```
### P5
```
root@PE5> show route | no-more

inet.0: 19 destinations, 24 routes (19 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

10.120.0.0/24      *[OSPF/10] 23:53:10, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0
                       to 172.16.35.1 via ge-0/0/3.0
172.16.12.0/31     *[OSPF/10] 1d 00:55:40, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0
172.16.15.0/31     *[Direct/0] 1d 01:02:54
                    >  via ge-0/0/1.0
172.16.15.0/32     *[Local/0] 1d 01:02:54
                       Local via ge-0/0/1.0
172.16.26.0/31     *[OSPF/10] 1d 00:55:25, metric 200
                    >  to 172.16.56.1 via ge-0/0/6.0
172.16.34.0/31     *[OSPF/10] 1d 00:55:40, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0
172.16.35.0/31     *[Direct/0] 1d 01:02:54
                    >  via ge-0/0/3.0
172.16.35.0/32     *[Local/0] 1d 01:02:54
                       Local via ge-0/0/3.0
172.16.46.0/31     *[OSPF/10] 1d 00:55:25, metric 200
                    >  to 172.16.56.1 via ge-0/0/6.0
172.16.56.0/31     *[Direct/0] 1d 01:02:54
                    >  via ge-0/0/6.0
172.16.56.0/32     *[Local/0] 1d 01:02:54
                       Local via ge-0/0/6.0
192.168.1.1/32     @[OSPF/10] 1d 00:55:40, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
                   #[LDP/9] 1d 00:55:40, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
192.168.1.2/32     @[OSPF/10] 1d 00:55:25, metric 200
                       to 172.16.15.1 via ge-0/0/1.0
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 00:55:25, metric 200
                       to 172.16.15.1 via ge-0/0/1.0, Push 299776
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 299776
192.168.1.3/32     @[OSPF/10] 1d 00:55:40, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
                   #[LDP/9] 1d 00:55:40, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
192.168.1.4/32     @[OSPF/10] 1d 00:55:25, metric 200
                       to 172.16.35.1 via ge-0/0/3.0
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 00:55:25, metric 200
                       to 172.16.35.1 via ge-0/0/3.0, Push 299776
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 299808
192.168.1.5/32     *[Direct/0] 1d 00:55:51
                    >  via lo0.0
192.168.1.6/32     @[OSPF/10] 1d 00:55:25, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 00:55:25, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 1d 01:02:54, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 01:09:55, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 00:55:40, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
192.168.1.2/32     *[LDP/9] 1d 00:55:25, metric 200
                       to 172.16.15.1 via ge-0/0/1.0, Push 299776
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 299776
192.168.1.3/32     *[LDP/9] 1d 00:55:40, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
192.168.1.4/32     *[LDP/9] 1d 00:55:25, metric 200
                       to 172.16.35.1 via ge-0/0/3.0, Push 299776
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 299808
192.168.1.6/32     *[LDP/9] 1d 00:55:25, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0

mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 01:08:42, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 01:08:42, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 01:09:55, metric 1
                       Receive
2                  *[MPLS/0] 1d 01:08:42, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 01:08:42, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 01:09:55, metric 1
                       Receive
299776             *[LDP/9] 1d 00:55:50, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Pop
299776(S=0)        *[LDP/9] 1d 00:55:50, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Pop
299792             *[LDP/9] 1d 00:55:25, metric 1
                       to 172.16.35.1 via ge-0/0/3.0, Swap 299776
                    >  to 172.16.56.1 via ge-0/0/6.0, Swap 299808
299808             *[LDP/9] 1d 00:55:50, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Pop
299808(S=0)        *[LDP/9] 1d 00:55:50, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Pop
299824             *[LDP/9] 1d 00:55:25, metric 1
                       to 172.16.15.1 via ge-0/0/1.0, Swap 299776
                    >  to 172.16.56.1 via ge-0/0/6.0, Swap 299776
299840             *[LDP/9] 1d 00:55:35, metric 1
                    >  to 172.16.56.1 via ge-0/0/6.0, Pop
299840(S=0)        *[LDP/9] 1d 00:55:35, metric 1
                    >  to 172.16.56.1 via ge-0/0/6.0, Pop

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 1d 01:54:10
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 01:54:21
                       MultiRecv
```
### P6
```
root@PE6> show route | no-more

inet.0: 19 destinations, 24 routes (19 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

10.120.0.0/24      *[OSPF/10] 23:53:24, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0
                       to 172.16.46.1 via ge-0/0/4.0
172.16.12.0/31     *[OSPF/10] 1d 00:55:44, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0
172.16.15.0/31     *[OSPF/10] 1d 00:55:44, metric 200
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.26.0/31     *[Direct/0] 1d 01:02:39
                    >  via ge-0/0/2.0
172.16.26.0/32     *[Local/0] 1d 01:02:39
                       Local via ge-0/0/2.0
172.16.34.0/31     *[OSPF/10] 1d 00:55:44, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0
172.16.35.0/31     *[OSPF/10] 1d 00:55:44, metric 200
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.46.0/31     *[Direct/0] 1d 01:02:39
                    >  via ge-0/0/4.0
172.16.46.0/32     *[Local/0] 1d 01:02:39
                       Local via ge-0/0/4.0
172.16.56.0/31     *[Direct/0] 1d 01:02:39
                    >  via ge-0/0/5.0
172.16.56.1/32     *[Local/0] 1d 01:02:39
                       Local via ge-0/0/5.0
192.168.1.1/32     @[OSPF/10] 1d 00:55:44, metric 200
                       to 172.16.26.1 via ge-0/0/2.0
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:55:44, metric 200
                       to 172.16.26.1 via ge-0/0/2.0, Push 299776
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299808
192.168.1.2/32     @[OSPF/10] 1d 00:55:44, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
                   #[LDP/9] 1d 00:55:44, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
192.168.1.3/32     @[OSPF/10] 1d 00:55:44, metric 200
                       to 172.16.46.1 via ge-0/0/4.0
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:55:44, metric 200
                       to 172.16.46.1 via ge-0/0/4.0, Push 299776
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299776
192.168.1.4/32     @[OSPF/10] 1d 00:55:44, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
                   #[LDP/9] 1d 00:55:44, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
192.168.1.5/32     @[OSPF/10] 1d 00:55:44, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 1d 00:55:44, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0
192.168.1.6/32     *[Direct/0] 1d 00:55:54
                    >  via lo0.0
224.0.0.2/32       *[LDP/9] 1d 01:02:39, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 01:09:36, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 00:55:44, metric 200
                       to 172.16.26.1 via ge-0/0/2.0, Push 299776
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299808
192.168.1.2/32     *[LDP/9] 1d 00:55:44, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
192.168.1.3/32     *[LDP/9] 1d 00:55:44, metric 200
                       to 172.16.46.1 via ge-0/0/4.0, Push 299776
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299776
192.168.1.4/32     *[LDP/9] 1d 00:55:44, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
192.168.1.5/32     *[LDP/9] 1d 00:55:44, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0

mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 01:09:12, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 01:09:12, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 01:09:36, metric 1
                       Receive
2                  *[MPLS/0] 1d 01:09:12, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 01:09:12, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 01:09:36, metric 1
                       Receive
299776             *[LDP/9] 1d 00:55:54, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Pop
299776(S=0)        *[LDP/9] 1d 00:55:54, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Pop
299792             *[LDP/9] 1d 00:55:54, metric 1
                       to 172.16.26.1 via ge-0/0/2.0, Swap 299776
                    >  to 172.16.56.0 via ge-0/0/5.0, Swap 299808
299808             *[LDP/9] 1d 00:55:54, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop
299808(S=0)        *[LDP/9] 1d 00:55:54, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop
299824             *[LDP/9] 1d 00:55:54, metric 1
                       to 172.16.46.1 via ge-0/0/4.0, Swap 299776
                    >  to 172.16.56.0 via ge-0/0/5.0, Swap 299776
299840             *[LDP/9] 1d 00:55:54, metric 1
                    >  to 172.16.56.0 via ge-0/0/5.0, Pop
299840(S=0)        *[LDP/9] 1d 00:55:54, metric 1
                    >  to 172.16.56.0 via ge-0/0/5.0, Pop

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe06:0/128
                   *[Local/0] 1d 01:54:29
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 01:54:40
                       MultiRecv
```
