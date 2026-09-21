#### PE1
```
root@PE1> show route

inet.0: 17 destinations, 22 routes (17 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[Direct/0] 1d 23:02:42
                    >  via ge-0/0/2.0
172.16.12.0/32     *[Local/0] 1d 23:02:42
                       Local via ge-0/0/2.0
172.16.15.0/31     *[Direct/0] 1d 23:02:42
                    >  via ge-0/0/5.0
172.16.15.1/32     *[Local/0] 1d 23:02:42
                       Local via ge-0/0/5.0
172.16.26.0/31     *[OSPF/10] 1d 16:43:41, metric 200
                    >  to 172.16.12.1 via ge-0/0/2.0
172.16.34.0/31     *[OSPF/10] 1d 16:43:41, metric 300
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.35.0/31     *[OSPF/10] 1d 16:43:41, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
172.16.46.0/31     *[OSPF/10] 1d 16:43:41, metric 300
                    >  to 172.16.12.1 via ge-0/0/2.0
                       to 172.16.15.0 via ge-0/0/5.0
172.16.56.0/31     *[OSPF/10] 1d 16:43:41, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.1/32     *[Direct/0] 1d 23:02:42
                    >  via lo0.0
192.168.1.2/32     @[OSPF/10] 1d 16:43:41, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
                   #[LDP/9] 1d 11:45:14, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.3/32     @[OSPF/10] 1d 16:43:41, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:14, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299920
192.168.1.4/32     @[OSPF/10] 1d 16:43:41, metric 300
                       to 172.16.12.1 via ge-0/0/2.0
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:14, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300096
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904
192.168.1.5/32     @[OSPF/10] 1d 16:43:41, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:14, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.6/32     @[OSPF/10] 1d 16:43:41, metric 200
                       to 172.16.12.1 via ge-0/0/2.0
                    >  to 172.16.15.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:14, metric 200
                       to 172.16.12.1 via ge-0/0/2.0, Push 300080
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299888
224.0.0.2/32       *[LDP/9] 1d 22:06:05, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 22:43:35, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.2/32     *[LDP/9] 1d 11:45:14, metric 100
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.3/32     *[LDP/9] 1d 11:45:14, metric 200
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299920
192.168.1.4/32     *[LDP/9] 1d 11:45:14, metric 300
                       to 172.16.12.1 via ge-0/0/2.0, Push 300096
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299904
192.168.1.5/32     *[LDP/9] 1d 11:45:14, metric 100
                    >  to 172.16.15.0 via ge-0/0/5.0
192.168.1.6/32     *[LDP/9] 1d 11:45:14, metric 200
                       to 172.16.12.1 via ge-0/0/2.0, Push 300080
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 299888

RED-CUSTOMER-HUYASTOMER.inet.0: 7 destinations, 7 routes (7 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.10.0/31       *[Direct/0] 1d 13:05:35
                    >  via ge-0/0/9.10
10.0.10.1/32       *[Local/0] 1d 13:05:35
                       Local via ge-0/0/9.10
10.0.11.0/31       *[BGP/170] 1d 00:48:18, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
10.0.13.0/31       *[BGP/170] 1d 00:48:01, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
192.168.10.1/32    *[BGP/170] 1d 12:57:45, MED 0, localpref 150
                      AS path: 65010 I, validation-state: unverified
                    >  to 10.0.10.0 via ge-0/0/9.10
192.168.10.2/32    *[BGP/170] 23:38:08, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299920(top)
192.168.10.3/32    *[BGP/170] 1d 00:48:01, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)

GREEN-ZALUPA-INCORPORATED.inet.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.21.0/31       *[Direct/0] 1d 00:32:03
                    >  via ge-0/0/8.20
10.0.21.1/32       *[Local/0] 1d 00:32:03
                       Local via ge-0/0/8.20
10.0.22.0/31       *[BGP/170] 1d 00:31:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
10.0.23.0/31       *[BGP/170] 1d 00:19:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299920(top)
10.0.24.0/31       *[BGP/170] 1d 00:18:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299904(top)
192.168.20.1/32    *[BGP/170] 1d 00:28:27, MED 0, localpref 100
                      AS path: 65020 I, validation-state: unverified
                    >  to 10.0.21.0 via ge-0/0/8.20
192.168.20.2/32    *[BGP/170] 1d 00:26:30, MED 0, localpref 100, from 192.168.1.2
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.20.3/32    *[BGP/170] 1d 00:16:47, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299920(top)
192.168.20.4/32    *[BGP/170] 1d 00:16:04, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300096(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299904(top)

BLUE-HUEPLET-LIMITED.inet.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.31.0/31       *[Direct/0] 1d 00:03:58
                    >  via ge-0/0/7.30
10.0.31.1/32       *[Local/0] 1d 00:03:58
                       Local via ge-0/0/7.30
10.0.32.0/31       *[BGP/170] 1d 00:03:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
10.0.33.0/31       *[BGP/170] 23:59:57, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299920(top)
10.0.34.0/31       *[BGP/170] 23:59:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300096(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299904(top)
192.168.30.1/32    *[OSPF/10] 1d 00:02:09, metric 2
                    >  to 10.0.31.0 via ge-0/0/7.30
192.168.30.2/32    *[BGP/170] 1d 00:01:05, MED 2, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
192.168.30.3/32    *[BGP/170] 23:58:26, MED 2, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299920(top)
192.168.30.4/32    *[BGP/170] 23:58:03, MED 2, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299904(top)
224.0.0.5/32       *[OSPF/10] 1d 00:03:59, metric 1
                       MultiRecv

mpls.0: 16 destinations, 16 routes (16 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 15:36:24, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 15:36:24, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 22:06:05, metric 1
                       Receive
2                  *[MPLS/0] 1d 15:36:24, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 15:36:24, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 22:06:05, metric 1
                       Receive
16                 *[VPN/0] 1d 00:48:26
                    >  via lsi.0 (RED-CUSTOMER-HUYASTOMER), Pop
18                 *[VPN/0] 1d 00:33:16
                    >  via lsi.2 (GREEN-ZALUPA-INCORPORATED), Pop
20                 *[VPN/0] 1d 00:03:58
                    >  via lsi.4 (BLUE-HUEPLET-LIMITED), Pop
300000             *[LDP/9] 1d 11:45:14, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Pop
300000(S=0)        *[LDP/9] 1d 11:45:14, metric 1
                    >  to 172.16.12.1 via ge-0/0/2.0, Pop
300032             *[LDP/9] 1d 11:45:14, metric 1
                       to 172.16.12.1 via ge-0/0/2.0, Swap 300096
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 299904
300048             *[LDP/9] 1d 11:45:14, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Pop
300048(S=0)        *[LDP/9] 1d 11:45:14, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Pop
300064             *[LDP/9] 1d 11:45:14, metric 1
                       to 172.16.12.1 via ge-0/0/2.0, Swap 300080
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 299888
300080             *[LDP/9] 1d 11:45:14, metric 1
                    >  to 172.16.15.0 via ge-0/0/5.0, Swap 299920

bgp.l3vpn.0: 16 destinations, 16 routes (16 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.2:8:10.0.11.0/31
                   *[BGP/170] 1d 00:48:18, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16
192.168.1.2:9:10.0.22.0/31
                   *[BGP/170] 1d 00:31:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.2:9:192.168.20.2/32
                   *[BGP/170] 1d 00:26:30, MED 0, localpref 100, from 192.168.1.2
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17
192.168.1.2:10:10.0.32.0/31
                   *[BGP/170] 1d 00:03:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
192.168.1.2:10:192.168.30.2/32
                   *[BGP/170] 1d 00:01:05, MED 2, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18
192.168.1.3:8:192.168.10.2/32
                   *[BGP/170] 23:38:08, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299920(top)
192.168.1.3:9:10.0.23.0/31
                   *[BGP/170] 1d 00:19:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299920(top)
192.168.1.3:9:192.168.20.3/32
                   *[BGP/170] 1d 00:16:47, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299920(top)
192.168.1.3:10:10.0.33.0/31
                   *[BGP/170] 23:59:57, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299920(top)
192.168.1.3:10:192.168.30.3/32
                   *[BGP/170] 23:58:26, MED 2, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299920(top)
192.168.1.4:8:10.0.13.0/31
                   *[BGP/170] 1d 00:48:01, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
192.168.1.4:8:192.168.10.3/32
                   *[BGP/170] 1d 00:48:01, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 16, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 16, Push 299904(top)
192.168.1.4:9:10.0.24.0/31
                   *[BGP/170] 1d 00:18:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299904(top)
192.168.1.4:9:192.168.20.4/32
                   *[BGP/170] 1d 00:16:04, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 17, Push 300096(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 17, Push 299904(top)
192.168.1.4:10:10.0.34.0/31
                   *[BGP/170] 23:59:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300096(top)
                    >  to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299904(top)
192.168.1.4:10:192.168.30.4/32
                   *[BGP/170] 23:58:03, MED 2, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0, Push 18, Push 300096(top)
                       to 172.16.15.0 via ge-0/0/5.0, Push 18, Push 299904(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 1d 23:29:53
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 23:30:04
                       MultiRecv
```
#### PE2
```
root@PE2> show route

inet.0: 17 destinations, 22 routes (17 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[Direct/0] 1d 22:59:45
                    >  via ge-0/0/1.0
172.16.12.1/32     *[Local/0] 1d 22:59:45
                       Local via ge-0/0/1.0
172.16.15.0/31     *[OSPF/10] 1d 16:43:22, metric 200
                    >  to 172.16.12.0 via ge-0/0/1.0
172.16.26.0/31     *[Direct/0] 1d 22:59:45
                    >  via ge-0/0/6.0
172.16.26.1/32     *[Local/0] 1d 22:59:45
                       Local via ge-0/0/6.0
172.16.34.0/31     *[OSPF/10] 1d 16:43:22, metric 300
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.35.0/31     *[OSPF/10] 1d 16:43:22, metric 300
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.46.0/31     *[OSPF/10] 1d 16:43:22, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
172.16.56.0/31     *[OSPF/10] 1d 16:43:22, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
192.168.1.1/32     @[OSPF/10] 1d 16:43:22, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
                   #[LDP/9] 1d 11:45:35, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.2/32     *[Direct/0] 1d 23:01:22
                    >  via lo0.0
192.168.1.3/32     @[OSPF/10] 1d 16:43:22, metric 300
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:45:35, metric 300
                       to 172.16.12.0 via ge-0/0/1.0, Push 300080
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299984
192.168.1.4/32     @[OSPF/10] 1d 16:43:22, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:45:35, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300000
192.168.1.5/32     @[OSPF/10] 1d 16:43:22, metric 200
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:45:35, metric 200
                       to 172.16.12.0 via ge-0/0/1.0, Push 300048
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300016
192.168.1.6/32     @[OSPF/10] 1d 16:43:22, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:45:35, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 1d 21:13:35, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 22:43:05, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 11:45:35, metric 100
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.3/32     *[LDP/9] 1d 11:45:35, metric 300
                       to 172.16.12.0 via ge-0/0/1.0, Push 300080
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 299984
192.168.1.4/32     *[LDP/9] 1d 11:45:35, metric 200
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300000
192.168.1.5/32     *[LDP/9] 1d 11:45:35, metric 200
                       to 172.16.12.0 via ge-0/0/1.0, Push 300048
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 300016
192.168.1.6/32     *[LDP/9] 1d 11:45:35, metric 100
                    >  to 172.16.26.0 via ge-0/0/6.0

RED-CUSTOMER-HUYASTOMER.inet.0: 7 destinations, 8 routes (7 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.10.0/31       *[BGP/170] 1d 00:48:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
10.0.11.0/31       *[Direct/0] 1d 12:42:59
                    >  via ge-0/0/9.10
10.0.11.1/32       *[Local/0] 1d 12:42:59
                       Local via ge-0/0/9.10
10.0.13.0/31       *[BGP/170] 1d 00:48:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300000(top)
192.168.10.1/32    *[BGP/170] 1d 00:48:50, MED 0, localpref 150, from 192.168.1.1
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
                    [BGP/170] 1d 12:39:26, MED 0, localpref 100
                      AS path: 65010 I, validation-state: unverified
                    >  to 10.0.11.0 via ge-0/0/9.10
192.168.10.2/32    *[BGP/170] 23:38:32, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 300080(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299984(top)
192.168.10.3/32    *[BGP/170] 1d 00:48:25, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300000(top)

GREEN-ZALUPA-INCORPORATED.inet.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.21.0/31       *[BGP/170] 1d 00:31:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
10.0.22.0/31       *[Direct/0] 1d 00:31:37
                    >  via ge-0/0/8.20
10.0.22.1/32       *[Local/0] 1d 00:31:37
                       Local via ge-0/0/8.20
10.0.23.0/31       *[BGP/170] 1d 00:20:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 300080(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299984(top)
10.0.24.0/31       *[BGP/170] 1d 00:19:12, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300000(top)
192.168.20.1/32    *[BGP/170] 1d 00:28:51, MED 0, localpref 100, from 192.168.1.1
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
192.168.20.2/32    *[BGP/170] 1d 00:26:55, MED 0, localpref 100
                      AS path: 65020 I, validation-state: unverified
                    >  to 10.0.22.0 via ge-0/0/8.20
192.168.20.3/32    *[BGP/170] 1d 00:17:11, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 300080(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.20.4/32    *[BGP/170] 1d 00:16:28, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300000(top)

BLUE-HUEPLET-LIMITED.inet.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.31.0/31       *[BGP/170] 1d 00:04:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 20
10.0.32.0/31       *[Direct/0] 1d 00:06:25
                    >  via ge-0/0/7.30
10.0.32.1/32       *[Local/0] 1d 00:06:25
                       Local via ge-0/0/7.30
10.0.33.0/31       *[BGP/170] 1d 00:00:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 300080(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299984(top)
10.0.34.0/31       *[BGP/170] 23:59:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300000(top)
192.168.30.1/32    *[BGP/170] 1d 00:02:33, MED 2, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 20
192.168.30.2/32    *[OSPF/10] 1d 00:01:30, metric 2
                    >  to 10.0.32.0 via ge-0/0/7.30
192.168.30.3/32    *[BGP/170] 23:58:50, MED 2, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 300080(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299984(top)
192.168.30.4/32    *[BGP/170] 23:58:27, MED 2, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300000(top)
224.0.0.5/32       *[OSPF/10] 1d 00:06:26, metric 1
                       MultiRecv

mpls.0: 16 destinations, 16 routes (16 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 15:35:56, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 15:35:56, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 22:06:25, metric 1
                       Receive
2                  *[MPLS/0] 1d 15:35:56, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 15:35:56, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 22:06:25, metric 1
                       Receive
16                 *[VPN/0] 1d 00:48:43
                    >  via lsi.0 (RED-CUSTOMER-HUYASTOMER), Pop
17                 *[VPN/0] 1d 00:31:37
                    >  via lsi.1 (GREEN-ZALUPA-INCORPORATED), Pop
18                 *[VPN/0] 1d 00:06:25
                    >  via lsi.2 (BLUE-HUEPLET-LIMITED), Pop
300016             *[LDP/9] 1d 11:45:35, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Pop
300016(S=0)        *[LDP/9] 1d 11:45:35, metric 1
                    >  to 172.16.12.0 via ge-0/0/1.0, Pop
300032             *[LDP/9] 1d 11:45:35, metric 1
                       to 172.16.12.0 via ge-0/0/1.0, Swap 300080
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 299984
300064             *[LDP/9] 1d 11:45:35, metric 1
                       to 172.16.12.0 via ge-0/0/1.0, Swap 300048
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 300016
300080             *[LDP/9] 1d 11:45:35, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Pop
300080(S=0)        *[LDP/9] 1d 11:45:35, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Pop
300096             *[LDP/9] 1d 11:45:35, metric 1
                    >  to 172.16.26.0 via ge-0/0/6.0, Swap 300000

bgp.l3vpn.0: 17 destinations, 17 routes (17 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1:8:10.0.10.0/31
                   *[BGP/170] 1d 00:48:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.1:8:192.168.10.1/32
                   *[BGP/170] 1d 00:48:50, MED 0, localpref 150, from 192.168.1.1
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16
192.168.1.1:9:10.0.21.0/31
                   *[BGP/170] 1d 00:31:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
192.168.1.1:9:192.168.20.1/32
                   *[BGP/170] 1d 00:28:51, MED 0, localpref 100, from 192.168.1.1
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18
192.168.1.1:10:10.0.31.0/31
                   *[BGP/170] 1d 00:04:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 20
192.168.1.1:10:192.168.30.1/32
                   *[BGP/170] 1d 00:02:33, MED 2, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 20
192.168.1.3:8:192.168.10.2/32
                   *[BGP/170] 23:38:32, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 16, Push 300080(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 299984(top)
192.168.1.3:9:10.0.23.0/31
                   *[BGP/170] 1d 00:20:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 300080(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.1.3:9:192.168.20.3/32
                   *[BGP/170] 1d 00:17:11, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 17, Push 300080(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 299984(top)
192.168.1.3:10:10.0.33.0/31
                   *[BGP/170] 1d 00:00:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 300080(top)
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299984(top)
192.168.1.3:10:192.168.30.3/32
                   *[BGP/170] 23:58:50, MED 2, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 18, Push 300080(top)
                       to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 299984(top)
192.168.1.4:8:10.0.13.0/31
                   *[BGP/170] 1d 00:48:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300000(top)
192.168.1.4:8:192.168.10.3/32
                   *[BGP/170] 1d 00:48:25, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 16, Push 300000(top)
192.168.1.4:9:10.0.24.0/31
                   *[BGP/170] 1d 00:19:12, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300000(top)
192.168.1.4:9:192.168.20.4/32
                   *[BGP/170] 1d 00:16:28, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 17, Push 300000(top)
192.168.1.4:10:10.0.34.0/31
                   *[BGP/170] 23:59:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300000(top)
192.168.1.4:10:192.168.30.4/32
                   *[BGP/170] 23:58:27, MED 2, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.26.0 via ge-0/0/6.0, Push 18, Push 300000(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 1d 23:06:11
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 23:06:22
                       MultiRecv
```
#### PE3
```
root@PE3> show route

inet.0: 17 destinations, 22 routes (17 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 1d 16:43:39, metric 300
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.15.0/31     *[OSPF/10] 1d 16:43:39, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
172.16.26.0/31     *[OSPF/10] 1d 16:43:39, metric 300
                    >  to 172.16.34.1 via ge-0/0/4.0
                       to 172.16.35.0 via ge-0/0/5.0
172.16.34.0/31     *[Direct/0] 1d 22:52:25
                    >  via ge-0/0/4.0
172.16.34.0/32     *[Local/0] 1d 22:52:25
                       Local via ge-0/0/4.0
172.16.35.0/31     *[Direct/0] 1d 22:52:25
                    >  via ge-0/0/5.0
172.16.35.1/32     *[Local/0] 1d 22:52:25
                       Local via ge-0/0/5.0
172.16.46.0/31     *[OSPF/10] 1d 16:43:39, metric 200
                    >  to 172.16.34.1 via ge-0/0/4.0
172.16.56.0/31     *[OSPF/10] 1d 16:43:39, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.1.1/32     @[OSPF/10] 1d 16:43:39, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:47, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299856
192.168.1.2/32     @[OSPF/10] 1d 16:43:39, metric 300
                       to 172.16.34.1 via ge-0/0/4.0
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:47, metric 300
                       to 172.16.34.1 via ge-0/0/4.0, Push 300032
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
192.168.1.3/32     *[Direct/0] 1d 22:52:25
                    >  via lo0.0
192.168.1.4/32     @[OSPF/10] 1d 16:43:39, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
                   #[LDP/9] 1d 11:45:47, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
192.168.1.5/32     @[OSPF/10] 1d 16:43:39, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:47, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.1.6/32     @[OSPF/10] 1d 16:43:39, metric 200
                       to 172.16.34.1 via ge-0/0/4.0
                    >  to 172.16.35.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:45:47, metric 200
                       to 172.16.34.1 via ge-0/0/4.0, Push 300016
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299888
224.0.0.2/32       *[LDP/9] 1d 22:01:59, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 22:42:51, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 11:45:47, metric 200
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299856
192.168.1.2/32     *[LDP/9] 1d 11:45:47, metric 300
                       to 172.16.34.1 via ge-0/0/4.0, Push 300032
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299936
192.168.1.4/32     *[LDP/9] 1d 11:45:47, metric 100
                    >  to 172.16.34.1 via ge-0/0/4.0
192.168.1.5/32     *[LDP/9] 1d 11:45:47, metric 100
                    >  to 172.16.35.0 via ge-0/0/5.0
192.168.1.6/32     *[LDP/9] 1d 11:45:47, metric 200
                       to 172.16.34.1 via ge-0/0/4.0, Push 300016
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 299888

RED-CUSTOMER-HUYASTOMER.inet.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.10.0/31       *[BGP/170] 1d 00:49:11, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299856(top)
10.0.11.0/31       *[BGP/170] 1d 00:49:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 300032(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
10.0.12.0/31       *[Direct/0] 1d 12:33:30
                    >  via ge-0/0/9.10
10.0.12.1/32       *[Local/0] 1d 12:33:30
                       Local via ge-0/0/9.10
10.0.13.0/31       *[BGP/170] 1d 00:48:47, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.10.1/32    *[BGP/170] 1d 00:49:11, MED 0, localpref 150, from 192.168.1.1
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299856(top)
192.168.10.2/32    *[BGP/170] 23:47:23, MED 0, localpref 100
                      AS path: 65010 I, validation-state: unverified
                    >  to 10.0.12.0 via ge-0/0/9.10
192.168.10.3/32    *[BGP/170] 1d 00:48:47, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16

GREEN-ZALUPA-INCORPORATED.inet.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.21.0/31       *[BGP/170] 1d 00:20:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299856(top)
10.0.22.0/31       *[BGP/170] 1d 00:20:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 300032(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
10.0.23.0/31       *[Direct/0] 1d 00:20:36
                    >  via ge-0/0/8.20
10.0.23.1/32       *[Local/0] 1d 00:20:36
                       Local via ge-0/0/8.20
10.0.24.0/31       *[BGP/170] 1d 00:19:34, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
192.168.20.1/32    *[BGP/170] 1d 00:20:36, MED 0, localpref 100, from 192.168.1.1
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299856(top)
192.168.20.2/32    *[BGP/170] 1d 00:20:36, MED 0, localpref 100, from 192.168.1.2
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 300032(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.20.3/32    *[BGP/170] 1d 00:17:32, MED 0, localpref 100
                      AS path: 65020 I, validation-state: unverified
                    >  to 10.0.23.0 via ge-0/0/8.20
192.168.20.4/32    *[BGP/170] 1d 00:16:50, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17

BLUE-HUEPLET-LIMITED.inet.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.31.0/31       *[BGP/170] 1d 00:00:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 20, Push 299856(top)
10.0.32.0/31       *[BGP/170] 1d 00:00:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 300032(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
10.0.33.0/31       *[Direct/0] 1d 00:00:43
                    >  via ge-0/0/7.30
10.0.33.1/32       *[Local/0] 1d 00:00:43
                       Local via ge-0/0/7.30
10.0.34.0/31       *[BGP/170] 1d 00:00:02, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18
192.168.30.1/32    *[BGP/170] 1d 00:00:43, MED 2, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 20, Push 299856(top)
192.168.30.2/32    *[BGP/170] 1d 00:00:43, MED 2, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 300032(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
192.168.30.3/32    *[OSPF/10] 23:59:11, metric 2
                    >  to 10.0.33.0 via ge-0/0/7.30
192.168.30.4/32    *[BGP/170] 23:58:49, MED 2, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18
224.0.0.5/32       *[OSPF/10] 1d 00:00:44, metric 1
                       MultiRecv

mpls.0: 16 destinations, 16 routes (16 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 15:35:56, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 15:35:56, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 22:01:59, metric 1
                       Receive
2                  *[MPLS/0] 1d 15:35:56, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 15:35:56, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 22:01:59, metric 1
                       Receive
16                 *[VPN/0] 1d 00:48:51
                    >  via lsi.0 (RED-CUSTOMER-HUYASTOMER), Pop
17                 *[VPN/0] 1d 00:20:36
                    >  via lsi.1 (GREEN-ZALUPA-INCORPORATED), Pop
18                 *[VPN/0] 1d 00:00:43
                    >  via lsi.2 (BLUE-HUEPLET-LIMITED), Pop
299968             *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 300032
                       to 172.16.35.0 via ge-0/0/5.0, Swap 299936
299984             *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Pop
299984(S=0)        *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Pop
300000             *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Pop
300000(S=0)        *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Pop
300016             *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.34.1 via ge-0/0/4.0, Swap 300016
                       to 172.16.35.0 via ge-0/0/5.0, Swap 299888
300032             *[LDP/9] 1d 11:45:47, metric 1
                    >  to 172.16.35.0 via ge-0/0/5.0, Swap 299856

bgp.l3vpn.0: 17 destinations, 17 routes (17 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1:8:10.0.10.0/31
                   *[BGP/170] 1d 00:49:11, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299856(top)
192.168.1.1:8:192.168.10.1/32
                   *[BGP/170] 1d 00:49:11, MED 0, localpref 150, from 192.168.1.1
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299856(top)
192.168.1.1:9:10.0.21.0/31
                   *[BGP/170] 1d 00:20:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299856(top)
192.168.1.1:9:192.168.20.1/32
                   *[BGP/170] 1d 00:20:36, MED 0, localpref 100, from 192.168.1.1
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299856(top)
192.168.1.1:10:10.0.31.0/31
                   *[BGP/170] 1d 00:00:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 20, Push 299856(top)
192.168.1.1:10:192.168.30.1/32
                   *[BGP/170] 1d 00:00:43, MED 2, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 20, Push 299856(top)
192.168.1.2:8:10.0.11.0/31
                   *[BGP/170] 1d 00:49:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16, Push 300032(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 16, Push 299936(top)
192.168.1.2:9:10.0.22.0/31
                   *[BGP/170] 1d 00:20:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 300032(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.1.2:9:192.168.20.2/32
                   *[BGP/170] 1d 00:20:36, MED 0, localpref 100, from 192.168.1.2
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 17, Push 300032(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 17, Push 299936(top)
192.168.1.2:10:10.0.32.0/31
                   *[BGP/170] 1d 00:00:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 300032(top)
                    >  to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
192.168.1.2:10:192.168.30.2/32
                   *[BGP/170] 1d 00:00:43, MED 2, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18, Push 300032(top)
                       to 172.16.35.0 via ge-0/0/5.0, Push 18, Push 299936(top)
192.168.1.4:8:10.0.13.0/31
                   *[BGP/170] 1d 00:48:47, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.1.4:8:192.168.10.3/32
                   *[BGP/170] 1d 00:48:47, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 16
192.168.1.4:9:10.0.24.0/31
                   *[BGP/170] 1d 00:19:34, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
192.168.1.4:9:192.168.20.4/32
                   *[BGP/170] 1d 00:16:50, MED 0, localpref 100, from 192.168.1.4
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 17
192.168.1.4:10:10.0.34.0/31
                   *[BGP/170] 1d 00:00:02, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18
192.168.1.4:10:192.168.30.4/32
                   *[BGP/170] 23:58:49, MED 2, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.1 via ge-0/0/4.0, Push 18

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 1d 22:55:50
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 22:56:01
                       MultiRecv
```
#### PE4
```
root@PE4> show route

inet.0: 17 destinations, 22 routes (17 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 1d 16:43:54, metric 300
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.15.0/31     *[OSPF/10] 1d 16:43:54, metric 300
                    >  to 172.16.34.0 via ge-0/0/3.0
                       to 172.16.46.0 via ge-0/0/6.0
172.16.26.0/31     *[OSPF/10] 1d 16:43:54, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
172.16.34.0/31     *[Direct/0] 1d 22:51:18
                    >  via ge-0/0/3.0
172.16.34.1/32     *[Local/0] 1d 22:51:18
                       Local via ge-0/0/3.0
172.16.35.0/31     *[OSPF/10] 1d 16:43:54, metric 200
                    >  to 172.16.34.0 via ge-0/0/3.0
172.16.46.0/31     *[Direct/0] 1d 22:51:18
                    >  via ge-0/0/6.0
172.16.46.1/32     *[Local/0] 1d 22:51:18
                       Local via ge-0/0/6.0
172.16.56.0/31     *[OSPF/10] 1d 16:43:54, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
192.168.1.1/32     @[OSPF/10] 1d 16:43:54, metric 300
                       to 172.16.34.0 via ge-0/0/3.0
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:04, metric 300
                       to 172.16.34.0 via ge-0/0/3.0, Push 300032
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299952
192.168.1.2/32     @[OSPF/10] 1d 16:43:54, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:04, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299968
192.168.1.3/32     @[OSPF/10] 1d 16:43:54, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
                   #[LDP/9] 1d 11:46:04, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
192.168.1.4/32     *[Direct/0] 1d 22:51:18
                    >  via lo0.0
192.168.1.5/32     @[OSPF/10] 1d 16:43:54, metric 200
                       to 172.16.34.0 via ge-0/0/3.0
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:04, metric 200
                       to 172.16.34.0 via ge-0/0/3.0, Push 300000
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300016
192.168.1.6/32     @[OSPF/10] 1d 16:43:54, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:04, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 1d 22:02:08, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 22:42:58, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 11:46:04, metric 300
                       to 172.16.34.0 via ge-0/0/3.0, Push 300032
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299952
192.168.1.2/32     *[LDP/9] 1d 11:46:04, metric 200
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 299968
192.168.1.3/32     *[LDP/9] 1d 11:46:04, metric 100
                    >  to 172.16.34.0 via ge-0/0/3.0
192.168.1.5/32     *[LDP/9] 1d 11:46:04, metric 200
                       to 172.16.34.0 via ge-0/0/3.0, Push 300000
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 300016
192.168.1.6/32     *[LDP/9] 1d 11:46:04, metric 100
                    >  to 172.16.46.0 via ge-0/0/6.0

RED-CUSTOMER-HUYASTOMER.inet.0: 7 destinations, 7 routes (7 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.10.0/31       *[BGP/170] 1d 00:49:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 300032(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299952(top)
10.0.11.0/31       *[BGP/170] 1d 00:49:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299968(top)
10.0.13.0/31       *[Direct/0] 1d 12:17:11
                    >  via ge-0/0/9.10
10.0.13.1/32       *[Local/0] 1d 12:17:11
                       Local via ge-0/0/9.10
192.168.10.1/32    *[BGP/170] 1d 00:49:30, MED 0, localpref 150, from 192.168.1.1
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16, Push 300032(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 16, Push 299952(top)
192.168.10.2/32    *[BGP/170] 23:39:13, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65010 I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 16
192.168.10.3/32    *[BGP/170] 1d 11:30:24, MED 0, localpref 100
                      AS path: 65010 I, validation-state: unverified
                    >  to 10.0.13.0 via ge-0/0/9.10

GREEN-ZALUPA-INCORPORATED.inet.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.21.0/31       *[BGP/170] 1d 00:19:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 300032(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299952(top)
10.0.22.0/31       *[BGP/170] 1d 00:19:53, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299968(top)
10.0.23.0/31       *[BGP/170] 1d 00:19:53, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
10.0.24.0/31       *[Direct/0] 1d 00:19:53
                    >  via ge-0/0/8.20
10.0.24.1/32       *[Local/0] 1d 00:19:53
                       Local via ge-0/0/8.20
192.168.20.1/32    *[BGP/170] 1d 00:19:53, MED 0, localpref 100, from 192.168.1.1
                      AS path: 65020 I, validation-state: unverified
                       to 172.16.34.0 via ge-0/0/3.0, Push 18, Push 300032(top)
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299952(top)
192.168.20.2/32    *[BGP/170] 1d 00:19:53, MED 0, localpref 100, from 192.168.1.2
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 17, Push 299968(top)
192.168.20.3/32    *[BGP/170] 1d 00:17:52, MED 0, localpref 100, from 192.168.1.3
                      AS path: 65020 I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 17
192.168.20.4/32    *[BGP/170] 1d 00:17:09, MED 0, localpref 100
                      AS path: 65020 I, validation-state: unverified
                    >  to 10.0.24.0 via ge-0/0/8.20

BLUE-HUEPLET-LIMITED.inet.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.0.31.0/31       *[BGP/170] 1d 00:00:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.34.0 via ge-0/0/3.0, Push 20, Push 300032(top)
                       to 172.16.46.0 via ge-0/0/6.0, Push 20, Push 299952(top)
10.0.32.0/31       *[BGP/170] 1d 00:00:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.46.0 via ge-0/0/6.0, Push 18, Push 299968(top)
10.0.33.0/31       *[BGP/170] 1d 00:00:22, localpref 100, from 192.168.1.3
```
#### P5
```
root@P5> show route

inet.0: 18 destinations, 23 routes (18 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 1d 15:35:49, metric 200
                    >  to 172.16.15.1 via ge-0/0/1.0
172.16.15.0/31     *[Direct/0] 1d 22:55:43
                    >  via ge-0/0/1.0
172.16.15.0/32     *[Local/0] 1d 22:55:43
                       Local via ge-0/0/1.0
172.16.26.0/31     *[OSPF/10] 1d 15:35:49, metric 200
                    >  to 172.16.56.1 via ge-0/0/6.0
172.16.34.0/31     *[OSPF/10] 1d 15:35:49, metric 200
                    >  to 172.16.35.1 via ge-0/0/3.0
172.16.35.0/31     *[Direct/0] 1d 22:55:43
                    >  via ge-0/0/3.0
172.16.35.0/32     *[Local/0] 1d 22:55:43
                       Local via ge-0/0/3.0
172.16.46.0/31     *[OSPF/10] 1d 15:35:49, metric 200
                    >  to 172.16.56.1 via ge-0/0/6.0
172.16.56.0/31     *[Direct/0] 1d 22:55:43
                    >  via ge-0/0/6.0
172.16.56.0/32     *[Local/0] 1d 22:55:43
                       Local via ge-0/0/6.0
192.168.1.1/32     @[OSPF/10] 1d 15:35:49, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
                   #[LDP/9] 1d 11:46:35, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
192.168.1.2/32     @[OSPF/10] 1d 15:35:49, metric 200
                       to 172.16.15.1 via ge-0/0/1.0
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:35, metric 200
                       to 172.16.15.1 via ge-0/0/1.0, Push 300000
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 299968
192.168.1.3/32     @[OSPF/10] 1d 15:35:49, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
                   #[LDP/9] 1d 11:46:35, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
192.168.1.4/32     @[OSPF/10] 1d 15:35:49, metric 200
                       to 172.16.35.1 via ge-0/0/3.0
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:35, metric 200
                       to 172.16.35.1 via ge-0/0/3.0, Push 299984
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 300000
192.168.1.5/32     *[Direct/0] 1d 22:55:43
                    >  via lo0.0
192.168.1.6/32     @[OSPF/10] 1d 15:35:49, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0
                   #[LDP/9] 1d 11:46:35, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0
224.0.0.2/32       *[LDP/9] 1d 22:02:15, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 22:42:03, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 11:46:35, metric 100
                    >  to 172.16.15.1 via ge-0/0/1.0
192.168.1.2/32     *[LDP/9] 1d 11:46:35, metric 200
                       to 172.16.15.1 via ge-0/0/1.0, Push 300000
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 299968
192.168.1.3/32     *[LDP/9] 1d 11:46:35, metric 100
                    >  to 172.16.35.1 via ge-0/0/3.0
192.168.1.4/32     *[LDP/9] 1d 11:46:35, metric 200
                       to 172.16.35.1 via ge-0/0/3.0, Push 299984
                    >  to 172.16.56.1 via ge-0/0/6.0, Push 300000
192.168.1.6/32     *[LDP/9] 1d 11:46:35, metric 100
                    >  to 172.16.56.1 via ge-0/0/6.0

mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 15:36:50, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 15:36:50, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 22:02:15, metric 1
                       Receive
2                  *[MPLS/0] 1d 15:36:50, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 15:36:50, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 22:02:15, metric 1
                       Receive
299856             *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Pop
299856(S=0)        *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Pop
299888             *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.56.1 via ge-0/0/6.0, Pop
299888(S=0)        *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.56.1 via ge-0/0/6.0, Pop
299904             *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Swap 299984
                       to 172.16.56.1 via ge-0/0/6.0, Swap 300000
299920             *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Pop
299920(S=0)        *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.35.1 via ge-0/0/3.0, Pop
299936             *[LDP/9] 1d 11:46:35, metric 1
                    >  to 172.16.15.1 via ge-0/0/1.0, Swap 300000
                       to 172.16.56.1 via ge-0/0/6.0, Swap 299968

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 1d 22:57:22
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 22:57:33
                       MultiRecv
```
#### P6
```
root@P6> show route

inet.0: 18 destinations, 23 routes (18 active, 0 holddown, 0 hidden)
@ = Routing Use Only, # = Forwarding Use Only
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[OSPF/10] 1d 15:36:12, metric 200
                    >  to 172.16.26.1 via ge-0/0/2.0
172.16.15.0/31     *[OSPF/10] 1d 15:36:12, metric 200
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.26.0/31     *[Direct/0] 1d 22:55:15
                    >  via ge-0/0/2.0
172.16.26.0/32     *[Local/0] 1d 22:55:15
                       Local via ge-0/0/2.0
172.16.34.0/31     *[OSPF/10] 1d 15:36:12, metric 200
                    >  to 172.16.46.1 via ge-0/0/4.0
172.16.35.0/31     *[OSPF/10] 1d 15:36:12, metric 200
                    >  to 172.16.56.0 via ge-0/0/5.0
172.16.46.0/31     *[Direct/0] 1d 22:55:15
                    >  via ge-0/0/4.0
172.16.46.0/32     *[Local/0] 1d 22:55:15
                       Local via ge-0/0/4.0
172.16.56.0/31     *[Direct/0] 1d 22:55:15
                    >  via ge-0/0/5.0
172.16.56.1/32     *[Local/0] 1d 22:55:15
                       Local via ge-0/0/5.0
192.168.1.1/32     @[OSPF/10] 1d 15:36:12, metric 200
                       to 172.16.26.1 via ge-0/0/2.0
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:47:00, metric 200
                       to 172.16.26.1 via ge-0/0/2.0, Push 300016
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299856
192.168.1.2/32     @[OSPF/10] 1d 15:36:12, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
                   #[LDP/9] 1d 11:47:00, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
192.168.1.3/32     @[OSPF/10] 1d 15:36:12, metric 200
                       to 172.16.46.1 via ge-0/0/4.0
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:47:00, metric 200
                       to 172.16.46.1 via ge-0/0/4.0, Push 299984
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299920
192.168.1.4/32     @[OSPF/10] 1d 15:36:12, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
                   #[LDP/9] 1d 11:47:00, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
192.168.1.5/32     @[OSPF/10] 1d 15:36:12, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0
                   #[LDP/9] 1d 11:47:00, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0
192.168.1.6/32     *[Direct/0] 1d 22:55:15
                    >  via lo0.0
224.0.0.2/32       *[LDP/9] 1d 22:02:32, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 1d 22:42:17, metric 1
                       MultiRecv

inet.3: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.1.1/32     *[LDP/9] 1d 11:47:00, metric 200
                       to 172.16.26.1 via ge-0/0/2.0, Push 300016
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299856
192.168.1.2/32     *[LDP/9] 1d 11:47:00, metric 100
                    >  to 172.16.26.1 via ge-0/0/2.0
192.168.1.3/32     *[LDP/9] 1d 11:47:00, metric 200
                       to 172.16.46.1 via ge-0/0/4.0, Push 299984
                    >  to 172.16.56.0 via ge-0/0/5.0, Push 299920
192.168.1.4/32     *[LDP/9] 1d 11:47:00, metric 100
                    >  to 172.16.46.1 via ge-0/0/4.0
192.168.1.5/32     *[LDP/9] 1d 11:47:00, metric 100
                    >  to 172.16.56.0 via ge-0/0/5.0

mpls.0: 14 destinations, 14 routes (14 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 1d 15:37:12, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 1d 15:37:12, metric 1
                       to table mpls.0
1                  *[MPLS/0] 1d 22:02:32, metric 1
                       Receive
2                  *[MPLS/0] 1d 15:37:12, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 1d 15:37:12, metric 1
                       to table mpls.0
13                 *[MPLS/0] 1d 22:02:32, metric 1
                       Receive
299952             *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Swap 300016
                       to 172.16.56.0 via ge-0/0/5.0, Swap 299856
299968             *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Pop
299968(S=0)        *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.26.1 via ge-0/0/2.0, Pop
299984             *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Swap 299984
                       to 172.16.56.0 via ge-0/0/5.0, Swap 299920
300000             *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop
300000(S=0)        *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.46.1 via ge-0/0/4.0, Pop
300016             *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.56.0 via ge-0/0/5.0, Pop
300016(S=0)        *[LDP/9] 1d 11:47:00, metric 1
                    >  to 172.16.56.0 via ge-0/0/5.0, Pop

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe06:0/128
                   *[Local/0] 1d 22:57:36
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 22:57:47
                       MultiRecv
```
