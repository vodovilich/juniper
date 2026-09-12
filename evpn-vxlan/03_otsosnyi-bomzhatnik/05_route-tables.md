### SPINE1
```
root@SPINE1> show route

inet.0: 35 destinations, 35 routes (35 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.100.0/24    *[Direct/0] 5d 02:12:45
                    >  via irb.100
10.200.100.252/32  *[Local/0] 5d 02:12:45
                       Local via irb.100
10.200.101.0/24    *[Direct/0] 5d 02:12:45
                    >  via irb.101
10.200.101.252/32  *[Local/0] 5d 02:12:45
                       Local via irb.101
10.200.102.0/24    *[Direct/0] 5d 02:12:45
                    >  via irb.102
10.200.102.252/32  *[Local/0] 5d 02:12:45
                       Local via irb.102
10.200.103.0/24    *[Direct/0] 5d 02:12:45
                    >  via irb.103
10.200.103.252/32  *[Local/0] 5d 02:12:45
                       Local via irb.103
10.200.104.0/24    *[Direct/0] 5d 02:12:45
                    >  via irb.104
10.200.104.252/32  *[Local/0] 5d 02:12:45
                       Local via irb.104
10.200.105.0/24    *[Direct/0] 3d 04:20:27
                    >  via irb.105
10.200.105.254/32  *[Local/0] 3d 04:20:27
                       Local via irb.105
10.200.106.0/24    *[Direct/0] 3d 04:20:27
                    >  via irb.106
10.200.106.254/32  *[Local/0] 3d 04:20:27
                       Local via irb.106
10.200.107.0/24    *[OSPF/10] 3d 04:21:31, metric 3
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
10.200.108.0/24    *[OSPF/10] 3d 04:21:31, metric 3
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
10.200.109.0/24    *[Direct/0] 4d 03:36:14
                    >  via irb.109
10.200.109.254/32  *[Local/0] 4d 03:36:14
                       Local via irb.109
10.200.110.0/24    *[Direct/0] 4d 03:20:03
                    >  via irb.110
10.200.110.254/32  *[Local/0] 4d 03:20:03
                       Local via irb.110
172.16.13.0/31     *[Direct/0] 3w2d 04:57:37
                    >  via ge-0/0/3.0
172.16.13.0/32     *[Local/0] 3w2d 04:57:37
                       Local via ge-0/0/3.0
172.16.14.0/31     *[Direct/0] 3w2d 04:57:37
                    >  via ge-0/0/4.0
172.16.14.0/32     *[Local/0] 3w2d 04:57:37
                       Local via ge-0/0/4.0
172.16.15.0/31     *[Direct/0] 3w2d 04:57:37
                    >  via ge-0/0/5.0
172.16.15.0/32     *[Local/0] 3w2d 04:57:37
                       Local via ge-0/0/5.0
172.16.23.0/31     *[OSPF/10] 1w5d 18:53:31, metric 2
                    >  to 172.16.13.1 via ge-0/0/3.0
172.16.24.0/31     *[OSPF/10] 1w5d 18:51:11, metric 2
                    >  to 172.16.14.1 via ge-0/0/4.0
172.16.25.0/31     *[OSPF/10] 1w5d 18:50:37, metric 2
                    >  to 172.16.15.1 via ge-0/0/5.0
192.168.1.1/32     *[Direct/0] 3w2d 05:03:41
                    >  via lo0.0
192.168.1.2/32     *[OSPF/10] 1w5d 18:49:58, metric 2
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
192.168.1.3/32     *[OSPF/10] 1w5d 18:53:31, metric 1
                    >  to 172.16.13.1 via ge-0/0/3.0
192.168.1.4/32     *[OSPF/10] 1w5d 18:51:11, metric 1
                    >  to 172.16.14.1 via ge-0/0/4.0
192.168.1.5/32     *[OSPF/10] 1w5d 18:50:37, metric 1
                    >  to 172.16.15.1 via ge-0/0/5.0
224.0.0.5/32       *[OSPF/10] 1w5d 18:57:42, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 3w2d 05:29:25
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3w2d 05:29:36
                       MultiRecv

bgp.evpn.0: 189 destinations, 294 routes (189 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w3d 02:35:21, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
                    [BGP/170] 1w3d 02:35:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w3d 02:35:32, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
                    [BGP/170] 1w3d 02:35:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 21:14:20, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 21:14:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 21:14:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 21:14:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[EVPN/170] 4d 03:36:14
                       Indirect
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[EVPN/170] 4d 03:20:03
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:21:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5107
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5107
                       to 172.16.15.1 via ge-0/0/5.0, Push 5107
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:21:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                       to 172.16.14.1 via ge-0/0/4.0, Push 5108
                       to 172.16.15.1 via ge-0/0/5.0, Push 5108
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                       to 172.16.14.1 via ge-0/0/4.0, Push 5109
                       to 172.16.15.1 via ge-0/0/5.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5110
                       to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:44:50, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w3d 02:44:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:44:34, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w3d 02:44:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:44:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w3d 02:44:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:41:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w3d 02:41:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:41:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w3d 02:41:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:41:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w3d 02:41:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:35:00, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 18:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:35:00, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 18:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:31:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 18:31:41, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:35:34, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w3d 02:35:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:35:33, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w3d 02:35:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 18:16:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5107
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5107
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5108
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 21:14:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 21:14:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 21:14:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 21:14:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 18:16:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:11:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 18:11:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5107
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5107
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5108
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5108
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[EVPN/170] 4d 03:36:14
                       Indirect
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[EVPN/170] 4d 03:20:03
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                       to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                       to 172.16.14.1 via ge-0/0/4.0, Push 5102
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                       to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                       to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                       to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                       to 172.16.14.1 via ge-0/0/4.0, Push 5104
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:21:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5107
                       to 172.16.14.1 via ge-0/0/4.0, Push 5107
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5107
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:21:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5108
                       to 172.16.14.1 via ge-0/0/4.0, Push 5108
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5108
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5109
                       to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
                       to 172.16.15.1 via ge-0/0/5.0, Push 5110
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:03:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:03:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:03:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:03:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:24:53, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 00:24:53, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:21:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 00:21:15, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00::10.200.108.1/304 MAC/IP
                   *[BGP/170] 00:24:06, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 00:24:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:12:28, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 00:12:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:11:52, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:11:52, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:11:52, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:11:52, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00::10.200.103.3/304 MAC/IP
                   *[BGP/170] 00:45:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 00:45:40, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[BGP/170] 01:07:14, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 01:07:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:41:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 00:41:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:41:12, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 00:41:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5108
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[EVPN/170] 3d 04:20:27
                       Indirect
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[EVPN/170] 3d 04:20:27
                       Indirect
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[EVPN/170] 4d 03:36:12
                       Indirect
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[EVPN/170] 4d 03:20:03
                       Indirect
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5107
                       to 172.16.14.1 via ge-0/0/4.0, Push 5107
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5107
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5108
                       to 172.16.14.1 via ge-0/0/4.0, Push 5108
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5108
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 4d 03:36:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5109
                       to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 4d 03:36:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5110
                       to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5107
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5108
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5107
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5107
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5108
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5103
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5107
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5107
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5108
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5108
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
4:192.168.1.4:0::09:192.168.1.4/296 ES
                   *[BGP/170] 1w3d 02:35:22, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
                    [BGP/170] 1w3d 02:35:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
4:192.168.1.5:0::09:192.168.1.5/296 ES
                   *[BGP/170] 1w0d 21:14:21, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 21:14:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0

VLAN-AWARE_FABRIC-EVI.evpn.0: 157 destinations, 241 routes (157 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[EVPN/170] 4d 03:36:14
                       Indirect
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[EVPN/170] 4d 03:20:03
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                       to 172.16.14.1 via ge-0/0/4.0, Push 5109
                       to 172.16.15.1 via ge-0/0/5.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5110
                       to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:31:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:31:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[EVPN/170] 5d 02:12:45
                       Indirect
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[EVPN/170] 3d 04:20:27
                       Indirect
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[EVPN/170] 4d 03:36:14
                       Indirect
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[EVPN/170] 4d 03:20:03
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                       to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                       to 172.16.14.1 via ge-0/0/4.0, Push 5102
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                       to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                       to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                       to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 5d 02:12:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                       to 172.16.14.1 via ge-0/0/4.0, Push 5104
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5109
                       to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 4d 03:36:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
                       to 172.16.15.1 via ge-0/0/5.0, Push 5110
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:03:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:03:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:03:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:03:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:24:53, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 00:24:53, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:21:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 00:21:15, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:11:52, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:11:52, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:11:52, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:11:52, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00::10.200.103.3/304 MAC/IP
                   *[BGP/170] 00:45:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 00:45:40, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[BGP/170] 01:07:14, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 01:07:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:41:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 00:41:44, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[EVPN/170] 5d 02:12:44
                       Indirect
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[EVPN/170] 3d 04:20:27
                       Indirect
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[EVPN/170] 3d 04:20:27
                       Indirect
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[EVPN/170] 4d 03:36:12
                       Indirect
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[EVPN/170] 4d 03:20:03
                       Indirect
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                       to 172.16.15.1 via ge-0/0/5.0, Push 5102
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                       to 172.16.15.1 via ge-0/0/5.0, Push 5103
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 5d 02:19:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                       to 172.16.15.1 via ge-0/0/5.0, Push 5104
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 4d 03:36:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5109
                       to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 4d 03:36:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5110
                       to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5102
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5103
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5104
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5105
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5106
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5109
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5110
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5102
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5103
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5104
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5105
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5106
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5109
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5110
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5102
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5103
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 16:46:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5104
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5105
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
                    [BGP/170] 3d 04:20:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5106
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5109
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:31:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5110

__default_evpn__.evpn.0: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:12:45
                       Indirect
```
### SPINE2
```
root@SPINE2> show route

inet.0: 35 destinations, 35 routes (35 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.100.0/24    *[Direct/0] 5d 02:13:41
                    >  via irb.100
10.200.100.253/32  *[Local/0] 5d 02:13:41
                       Local via irb.100
10.200.101.0/24    *[Direct/0] 5d 02:13:41
                    >  via irb.101
10.200.101.253/32  *[Local/0] 5d 02:13:41
                       Local via irb.101
10.200.102.0/24    *[Direct/0] 5d 02:13:41
                    >  via irb.102
10.200.102.253/32  *[Local/0] 5d 02:13:41
                       Local via irb.102
10.200.103.0/24    *[Direct/0] 5d 02:13:41
                    >  via irb.103
10.200.103.253/32  *[Local/0] 5d 02:13:41
                       Local via irb.103
10.200.104.0/24    *[Direct/0] 5d 02:13:41
                    >  via irb.104
10.200.104.253/32  *[Local/0] 5d 02:13:41
                       Local via irb.104
10.200.105.0/24    *[OSPF/10] 3d 04:21:42, metric 3
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
10.200.106.0/24    *[OSPF/10] 3d 04:21:42, metric 3
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
10.200.107.0/24    *[Direct/0] 3d 04:22:46
                    >  via irb.107
10.200.107.254/32  *[Local/0] 3d 04:22:46
                       Local via irb.107
10.200.108.0/24    *[Direct/0] 3d 04:22:46
                    >  via irb.108
10.200.108.254/32  *[Local/0] 3d 04:22:46
                       Local via irb.108
10.200.109.0/24    *[Direct/0] 4d 03:37:27
                    >  via irb.109
10.200.109.254/32  *[Local/0] 4d 03:37:27
                       Local via irb.109
10.200.110.0/24    *[Direct/0] 4d 03:37:27
                    >  via irb.110
10.200.110.254/32  *[Local/0] 4d 03:37:27
                       Local via irb.110
172.16.13.0/31     *[OSPF/10] 1w5d 18:51:19, metric 2
                    >  to 172.16.23.1 via ge-0/0/3.0
172.16.14.0/31     *[OSPF/10] 1w5d 18:51:19, metric 2
                    >  to 172.16.24.1 via ge-0/0/4.0
172.16.15.0/31     *[OSPF/10] 1w5d 18:51:14, metric 2
                    >  to 172.16.25.1 via ge-0/0/5.0
172.16.23.0/31     *[Direct/0] 3w2d 04:57:24
                    >  via ge-0/0/3.0
172.16.23.0/32     *[Local/0] 3w2d 04:57:24
                       Local via ge-0/0/3.0
172.16.24.0/31     *[Direct/0] 3w2d 04:57:24
                    >  via ge-0/0/4.0
172.16.24.0/32     *[Local/0] 3w2d 04:57:24
                       Local via ge-0/0/4.0
172.16.25.0/31     *[Direct/0] 3w2d 04:57:24
                    >  via ge-0/0/5.0
172.16.25.0/32     *[Local/0] 3w2d 04:57:24
                       Local via ge-0/0/5.0
192.168.1.1/32     *[OSPF/10] 1w5d 18:51:14, metric 2
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
192.168.1.2/32     *[Direct/0] 3w2d 05:04:04
                    >  via lo0.0
192.168.1.3/32     *[OSPF/10] 1w5d 18:51:19, metric 1
                    >  to 172.16.23.1 via ge-0/0/3.0
192.168.1.4/32     *[OSPF/10] 1w5d 18:51:19, metric 1
                    >  to 172.16.24.1 via ge-0/0/4.0
192.168.1.5/32     *[OSPF/10] 1w5d 18:51:14, metric 1
                    >  to 172.16.25.1 via ge-0/0/5.0
224.0.0.5/32       *[OSPF/10] 1w5d 18:51:29, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 3w2d 05:30:31
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3w2d 05:30:42
                       MultiRecv

bgp.evpn.0: 191 destinations, 298 routes (191 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w3d 02:36:35, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w3d 02:36:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w3d 02:36:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w3d 02:36:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 21:15:34, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 21:15:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 21:15:45, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 21:15:44, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                       to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5104
                       to 172.16.24.1 via ge-0/0/4.0, Push 5104
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:21:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5105
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
                       to 172.16.25.1 via ge-0/0/5.0, Push 5105
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:21:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5106
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
                       to 172.16.25.1 via ge-0/0/5.0, Push 5106
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 4d 03:37:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                       to 172.16.24.1 via ge-0/0/4.0, Push 5109
                       to 172.16.25.1 via ge-0/0/5.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 4d 03:21:18, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                       to 172.16.25.1 via ge-0/0/5.0, Push 5110
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:46:05, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w3d 02:46:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:45:48, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w3d 02:45:48, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:45:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w3d 02:45:44, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:42:19, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w3d 02:42:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:42:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w3d 02:42:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:42:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w3d 02:42:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:36:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 18:36:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:54, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 18:17:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:54, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 18:17:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:36:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 18:36:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 18:17:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 18:17:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:32:56, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 18:32:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 18:17:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 18:17:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:36:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w3d 02:36:48, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:36:47, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w3d 02:36:47, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:54, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 18:17:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 18:17:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:01:05, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 00:01:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 18:17:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 21:15:45, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 21:15:44, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 21:15:45, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 21:15:44, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:17:54, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 18:17:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:01:04, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 00:01:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:12:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 18:12:15, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5105
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5105
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5106
                    [BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5106
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                       to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                       to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                       to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                       to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                       to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                       to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:21:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
                       to 172.16.24.1 via ge-0/0/4.0, Push 5105
                       to 172.16.25.1 via ge-0/0/5.0, Push 5105
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:21:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
                       to 172.16.24.1 via ge-0/0/4.0, Push 5106
                       to 172.16.25.1 via ge-0/0/5.0, Push 5106
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 4d 03:37:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5109
                       to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 4d 03:21:18, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                       to 172.16.25.1 via ge-0/0/5.0, Push 5110
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:04:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:04:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:04:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:04:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:26:08, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 00:26:08, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:22:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 00:22:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:13:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 00:13:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:13:07, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:13:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:13:07, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:13:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:01:05, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 00:01:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[BGP/170] 01:08:30, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 01:08:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:42:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 00:42:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:42:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 00:42:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:01:04, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 00:01:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:21:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:21:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5109
                       to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5110
                       to 172.16.24.1 via ge-0/0/4.0, Push 5110
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[EVPN/170] 3d 04:22:46
                       Indirect
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[EVPN/170] 3d 04:22:46
                       Indirect
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[EVPN/170] 4d 03:37:27
                       Indirect
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[EVPN/170] 4d 03:37:27
                       Indirect
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5105
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5106
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5105
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5106
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5105
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5105
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5106
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5106
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
4:192.168.1.4:0::09:192.168.1.4/296 ES
                   *[BGP/170] 1w3d 02:36:36, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w3d 02:36:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
4:192.168.1.5:0::09:192.168.1.5/296 ES
                   *[BGP/170] 1w0d 21:15:35, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 21:15:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0

VLAN-AWARE_FABRIC-EVI.evpn.0: 159 destinations, 245 routes (159 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                       to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5104
                       to 172.16.24.1 via ge-0/0/4.0, Push 5104
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 4d 03:37:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                       to 172.16.24.1 via ge-0/0/4.0, Push 5109
                       to 172.16.25.1 via ge-0/0/5.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 4d 03:21:18, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                       to 172.16.25.1 via ge-0/0/5.0, Push 5110
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:34:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:34:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:01:05, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 00:01:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:32:40, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:01:04, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 00:01:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:32:18, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                       to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                       to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                       to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                       to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                       to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 5d 02:13:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                       to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 4d 03:37:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5109
                       to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 4d 03:21:18, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                       to 172.16.25.1 via ge-0/0/5.0, Push 5110
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[EVPN/170] 5d 02:13:41
                       Indirect
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[EVPN/170] 3d 04:22:46
                       Indirect
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[EVPN/170] 4d 03:37:27
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:04:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:04:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:04:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 00:04:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:26:08, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 00:26:08, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:13:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 00:13:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:13:07, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:13:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:13:07, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 00:13:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:01:05, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 00:01:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:42:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 00:42:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:01:04, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 00:01:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                       to 172.16.25.1 via ge-0/0/5.0, Push 5102
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                       to 172.16.25.1 via ge-0/0/5.0, Push 5103
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 5d 02:13:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                       to 172.16.25.1 via ge-0/0/5.0, Push 5104
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5109
                       to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5110
                       to 172.16.24.1 via ge-0/0/4.0, Push 5110
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[EVPN/170] 5d 02:13:41
                       Indirect
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[EVPN/170] 3d 04:22:46
                       Indirect
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[EVPN/170] 3d 04:22:46
                       Indirect
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[EVPN/170] 4d 03:37:27
                       Indirect
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[EVPN/170] 4d 03:37:27
                       Indirect
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5102
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5103
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5104
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5107
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5108
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5109
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5110
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5102
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5103
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5104
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5107
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5108
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5109
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5110
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5102
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5103
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
                    [BGP/170] 1w0d 16:47:16, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5104
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5107
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
                    [BGP/170] 3d 04:22:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5108
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5109
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110
                    [BGP/170] 3d 04:32:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5110

__default_evpn__.evpn.0: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 5d 02:13:41
                       Indirect
```
### LEAF3
```
root@LEAF3> show route

inet.0: 18 destinations, 18 routes (18 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.105.0/24    *[OSPF/10] 3d 04:23:02, metric 2
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.106.0/24    *[OSPF/10] 3d 04:23:02, metric 2
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.107.0/24    *[OSPF/10] 3d 04:24:06, metric 2
                    >  to 172.16.23.0 via ge-0/0/2.0
10.200.108.0/24    *[OSPF/10] 3d 04:24:06, metric 2
                    >  to 172.16.23.0 via ge-0/0/2.0
172.16.13.0/31     *[Direct/0] 3w2d 04:57:54
                    >  via ge-0/0/1.0
172.16.13.1/32     *[Local/0] 3w2d 04:57:54
                       Local via ge-0/0/1.0
172.16.14.0/31     *[OSPF/10] 1w5d 18:56:04, metric 2
                    >  to 172.16.13.0 via ge-0/0/1.0
172.16.15.0/31     *[OSPF/10] 1w5d 18:56:04, metric 2
                    >  to 172.16.13.0 via ge-0/0/1.0
172.16.23.0/31     *[Direct/0] 3w2d 04:57:54
                    >  via ge-0/0/2.0
172.16.23.1/32     *[Local/0] 3w2d 04:57:54
                       Local via ge-0/0/2.0
172.16.24.0/31     *[OSPF/10] 1w5d 18:52:44, metric 2
                    >  to 172.16.23.0 via ge-0/0/2.0
172.16.25.0/31     *[OSPF/10] 1w5d 18:52:44, metric 2
                    >  to 172.16.23.0 via ge-0/0/2.0
192.168.1.1/32     *[OSPF/10] 1w5d 18:56:04, metric 1
                    >  to 172.16.13.0 via ge-0/0/1.0
192.168.1.2/32     *[OSPF/10] 1w5d 18:52:44, metric 1
                    >  to 172.16.23.0 via ge-0/0/2.0
192.168.1.3/32     *[Direct/0] 3w2d 05:02:59
                    >  via lo0.0
192.168.1.4/32     *[OSPF/10] 1w5d 18:52:44, metric 2
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
192.168.1.5/32     *[OSPF/10] 1w5d 18:52:37, metric 2
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
224.0.0.5/32       *[OSPF/10] 1w5d 18:56:14, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 3w2d 05:31:44
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3w2d 05:31:55
                       MultiRecv

bgp.evpn.0: 189 destinations, 327 routes (189 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w3d 02:37:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:37:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w3d 02:38:08, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:38:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 21:16:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:16:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 21:17:06, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:06, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:35:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:47:27
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:47:10
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:47:06
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:43:41
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:43:39
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:43:39
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:37:36
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:15
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:15
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:37:36
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:03
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:03
                       Indirect
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:18
                       Indirect
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:03
                       Indirect
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:03
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:35
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:24
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:24
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 3d 04:35:24
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:02:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:48:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:02:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:06, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[EVPN/170] 00:06:02
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[EVPN/170] 00:06:02
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[EVPN/170] 00:27:28
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[EVPN/170] 00:23:50
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[EVPN/170] 00:15:03
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[EVPN/170] 00:14:27
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[EVPN/170] 00:14:27
                       Indirect
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:02:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[BGP/170] 01:09:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 01:09:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:44:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:44:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:43:47, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:43:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:02:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[EVPN/170] 1w3d 02:47:27
                       Indirect
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[EVPN/170] 1w3d 02:43:41
                       Indirect
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[EVPN/170] 3d 04:35:36
                       Indirect
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[EVPN/170] 3d 04:35:36
                       Indirect
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[EVPN/170] 3d 04:35:36
                       Indirect
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[EVPN/170] 3d 04:35:36
                       Indirect
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[EVPN/170] 3d 04:35:36
                       Indirect
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[EVPN/170] 3d 04:35:25
                       Indirect
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0

default-switch.evpn.0: 189 destinations, 327 routes (189 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w3d 02:37:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:37:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w3d 02:38:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:38:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 21:16:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:16:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 21:17:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:47:28
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:47:11
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:47:07
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:43:42
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:43:40
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:43:40
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:37:37
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:16
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:16
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:37:37
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:04
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:04
                       Indirect
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:19
                       Indirect
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:04
                       Indirect
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:04
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:19
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:18:56
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:18:56
                       Indirect
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:12
                       Indirect
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:42
                       Indirect
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:42
                       Indirect
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:12
                       Indirect
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:35
                       Indirect
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:35
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:03
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:28
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:28
                       Indirect
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:03
                       Indirect
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:23
                       Indirect
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:23
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:34:03
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:17
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:17
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:02:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:48:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:02:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                       to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5109
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5109
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[EVPN/170] 00:06:03
                       Indirect
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[EVPN/170] 00:06:03
                       Indirect
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[EVPN/170] 00:27:29
                       Indirect
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[EVPN/170] 00:23:51
                       Indirect
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[EVPN/170] 00:15:04
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[EVPN/170] 00:14:28
                       Indirect
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[EVPN/170] 00:14:28
                       Indirect
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:02:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[BGP/170] 01:09:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 01:09:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:44:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:44:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:43:48, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:43:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 319
                       to 172.16.23.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:02:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[EVPN/170] 1w3d 02:47:27
                       Indirect
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[EVPN/170] 1w3d 02:43:41
                       Indirect
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[EVPN/170] 1w0d 18:48:18
                       Indirect
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:33:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
```
### LEAF4
```
root@LEAF4> show route | no-more

inet.0: 18 destinations, 18 routes (18 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.105.0/24    *[OSPF/10] 3d 04:23:27, metric 2
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.106.0/24    *[OSPF/10] 3d 04:23:27, metric 2
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.107.0/24    *[OSPF/10] 3d 04:24:32, metric 2
                    >  to 172.16.24.0 via ge-0/0/2.0
10.200.108.0/24    *[OSPF/10] 3d 04:24:32, metric 2
                    >  to 172.16.24.0 via ge-0/0/2.0
172.16.13.0/31     *[OSPF/10] 1w5d 18:54:13, metric 2
                    >  to 172.16.14.0 via ge-0/0/1.0
172.16.14.0/31     *[Direct/0] 3w2d 04:56:09
                    >  via ge-0/0/1.0
172.16.14.1/32     *[Local/0] 3w2d 04:56:09
                       Local via ge-0/0/1.0
172.16.15.0/31     *[OSPF/10] 1w5d 18:54:13, metric 2
                    >  to 172.16.14.0 via ge-0/0/1.0
172.16.23.0/31     *[OSPF/10] 1w5d 18:53:06, metric 2
                    >  to 172.16.24.0 via ge-0/0/2.0
172.16.24.0/31     *[Direct/0] 2w4d 02:46:33
                    >  via ge-0/0/2.0
172.16.24.1/32     *[Local/0] 2w4d 02:46:33
                       Local via ge-0/0/2.0
172.16.25.0/31     *[OSPF/10] 1w5d 18:53:06, metric 2
                    >  to 172.16.24.0 via ge-0/0/2.0
192.168.1.1/32     *[OSPF/10] 1w5d 18:54:13, metric 1
                    >  to 172.16.14.0 via ge-0/0/1.0
192.168.1.2/32     *[OSPF/10] 1w5d 18:53:06, metric 1
                    >  to 172.16.24.0 via ge-0/0/2.0
192.168.1.3/32     *[OSPF/10] 1w5d 18:53:06, metric 2
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
192.168.1.4/32     *[Direct/0] 3w2d 04:56:09
                    >  via lo0.0
192.168.1.5/32     *[OSPF/10] 1w5d 18:53:01, metric 2
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
224.0.0.5/32       *[OSPF/10] 1w5d 18:54:23, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe04:0/128
                   *[Local/0] 3w2d 05:32:21
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3w2d 05:32:32
                       MultiRecv

bgp.evpn.0: 191 destinations, 352 routes (191 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1w3d 02:38:22
                       Indirect
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[EVPN/170] 1w3d 02:38:33
                       Indirect
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 21:17:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 21:17:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:34:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:34:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:38:36
                       Indirect
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:38:35
                       Indirect
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:41
                       Indirect
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:29
                       Indirect
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:02:51
                       Indirect
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:29
                       Indirect
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:27
                       Indirect
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:27
                       Indirect
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:27
                       Indirect
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:27
                       Indirect
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:27
                       Indirect
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:27
                       Indirect
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:02:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:23, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:06:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:06:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:06:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:06:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:27:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:27:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:24:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:24:17, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:15:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:15:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:14:54, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:14:54, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:14:54, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:14:54, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[EVPN/170] 00:02:52
                       Indirect
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[EVPN/170] 01:10:17
                       Indirect
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[EVPN/170] 00:44:47
                       Indirect
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[EVPN/170] 00:44:15
                       Indirect
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:02:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[EVPN/170] 1w3d 02:38:43
                       Indirect
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[EVPN/170] 1w3d 02:38:43
                       Indirect
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:41
                       Indirect
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:41
                       Indirect
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:41
                       Indirect
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[EVPN/170] 3d 04:34:30
                       Indirect
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[EVPN/170] 3d 04:34:30
                       Indirect
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[EVPN/170] 3d 04:34:30
                       Indirect
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[EVPN/170] 3d 04:34:30
                       Indirect
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[EVPN/170] 3d 04:34:30
                       Indirect
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[EVPN/170] 3d 04:34:30
                       Indirect
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
4:192.168.1.4:0::09:192.168.1.4/296 ES
                   *[EVPN/170] 1w3d 02:38:27
                       Indirect
4:192.168.1.5:0::09:192.168.1.5/296 ES
                   *[BGP/170] 1w0d 21:17:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0

default-switch.evpn.0: 188 destinations, 348 routes (188 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:15:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[EVPN/170] 1w3d 02:38:38
                       Indirect
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 21:17:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w0d 21:17:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:23:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:37, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:37, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:27, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:27, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:38:41
                       Indirect
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w3d 02:38:40
                       Indirect
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:46
                       Indirect
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:34
                       Indirect
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:02:56
                       Indirect
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:34
                       Indirect
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:19:26
                       Indirect
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:17:12
                       Indirect
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:17:05
                       Indirect
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:58
                       Indirect
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:53
                       Indirect
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:16:47
                       Indirect
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w0d 18:46:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 1w0d 18:46:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w0d 18:46:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:02:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                       to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:23:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:23:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:39, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:24:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:06:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:06:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:06:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:06:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:28:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:28:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:24:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:24:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:15:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:15:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:14:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:14:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:14:59, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:14:59, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 319
                       to 172.16.24.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[EVPN/170] 00:02:57
                       Indirect
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00::10.200.105.3/304 MAC/IP
                   *[EVPN/170] 01:10:22
                       Indirect
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[EVPN/170] 00:44:52
                       Indirect
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[EVPN/170] 00:44:20
                       Indirect
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:02:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:02:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:23:36, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:23:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:34:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:41, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:24:41, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:24:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:34, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[EVPN/170] 1w3d 02:38:48
                       Indirect
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[EVPN/170] 1w3d 02:38:48
                       Indirect
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[EVPN/170] 1w0d 18:45:46
                       Indirect
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:34:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0

__default_evpn__.evpn.0: 3 destinations, 4 routes (3 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1w3d 02:38:32
                       Indirect
4:192.168.1.4:0::09:192.168.1.4/296 ES
                   *[EVPN/170] 1w3d 02:38:33
                       Indirect
4:192.168.1.5:0::09:192.168.1.5/296 ES
                   *[BGP/170] 1w0d 21:17:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1w0d 21:17:31, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
```
### LEAF5
```
root@LEAF5> show route | no-more

inet.0: 18 destinations, 18 routes (18 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.105.0/24    *[OSPF/10] 3d 04:24:20, metric 2
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.106.0/24    *[OSPF/10] 3d 04:24:20, metric 2
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.107.0/24    *[OSPF/10] 3d 04:25:24, metric 2
                    >  to 172.16.25.0 via ge-0/0/2.0
10.200.108.0/24    *[OSPF/10] 3d 04:25:24, metric 2
                    >  to 172.16.25.0 via ge-0/0/2.0
172.16.13.0/31     *[OSPF/10] 1w5d 18:54:25, metric 2
                    >  to 172.16.15.0 via ge-0/0/1.0
172.16.14.0/31     *[OSPF/10] 1w5d 18:54:25, metric 2
                    >  to 172.16.15.0 via ge-0/0/1.0
172.16.15.0/31     *[Direct/0] 3w2d 04:55:35
                    >  via ge-0/0/1.0
172.16.15.1/32     *[Local/0] 3w2d 04:55:35
                       Local via ge-0/0/1.0
172.16.23.0/31     *[OSPF/10] 1w5d 18:53:49, metric 2
                    >  to 172.16.25.0 via ge-0/0/2.0
172.16.24.0/31     *[OSPF/10] 1w5d 18:53:49, metric 2
                    >  to 172.16.25.0 via ge-0/0/2.0
172.16.25.0/31     *[Direct/0] 3w2d 04:55:35
                    >  via ge-0/0/2.0
172.16.25.1/32     *[Local/0] 3w2d 04:55:35
                       Local via ge-0/0/2.0
192.168.1.1/32     *[OSPF/10] 1w5d 18:54:25, metric 1
                    >  to 172.16.15.0 via ge-0/0/1.0
192.168.1.2/32     *[OSPF/10] 1w5d 18:53:49, metric 1
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.3/32     *[OSPF/10] 1w5d 18:53:49, metric 2
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.4/32     *[OSPF/10] 1w5d 18:53:49, metric 2
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.5/32     *[Direct/0] 3w2d 04:55:35
                    >  via lo0.0
224.0.0.5/32       *[OSPF/10] 1w5d 18:54:36, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 3w2d 05:32:54
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3w2d 05:33:05
                       MultiRecv

bgp.evpn.0: 190 destinations, 354 routes (190 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:37, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:37, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:38, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:20, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w3d 02:39:14, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:39:14, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w3d 02:39:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:39:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1w0d 21:18:13
                       Indirect
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[EVPN/170] 1w0d 21:18:24
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:25:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:25:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:47, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:47, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:03:45, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:03:45, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:26:56, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 21:18:25
                       Indirect
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 21:18:25
                       Indirect
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:20:33
                       Indirect
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:03:45
                       Indirect
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:14:57
                       Indirect
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:58
                       Indirect
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:58
                       Indirect
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:58
                       Indirect
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:58
                       Indirect
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:58
                       Indirect
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 3d 04:34:58
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:34:58, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:25:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:25:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:07:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:07:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:07:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:07:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:28:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:28:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:25:12, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:25:12, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:16:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:16:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:15:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:15:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:03:47, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:03:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:45:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:45:41, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:45:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:45:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[EVPN/170] 00:03:47
                       Indirect
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:24:24, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:25:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:25:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:25:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:25:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:01, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 21:18:26
                       Indirect
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 21:18:26
                       Indirect
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:45:55
                       Indirect
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:45:55
                       Indirect
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:45:55
                       Indirect
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[EVPN/170] 3d 04:35:01
                       Indirect
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[EVPN/170] 3d 04:35:01
                       Indirect
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[EVPN/170] 3d 04:35:01
                       Indirect
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[EVPN/170] 3d 04:35:01
                       Indirect
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[EVPN/170] 3d 04:35:01
                       Indirect
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[EVPN/170] 3d 04:35:01
                       Indirect
4:192.168.1.4:0::09:192.168.1.4/296 ES
                   *[BGP/170] 1w3d 02:38:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:38:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
4:192.168.1.5:0::09:192.168.1.5/296 ES
                   *[EVPN/170] 1w0d 21:18:18
                       Indirect

default-switch.evpn.0: 187 destinations, 350 routes (187 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 5d 02:16:43, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.2:0::050000ffdc000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ee00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013ef00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000ffdc000013f000::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 5d 02:16:25, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:0::09::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w3d 02:39:19, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:39:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:65500::09::0/192 AD/EVI
                   *[BGP/170] 1w3d 02:39:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:39:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.5:65500::09::0/192 AD/EVI
                   *[EVPN/170] 1w0d 21:18:29
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 04:24:26, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:26, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:25:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 04:25:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10/304 MAC/IP
                   *[BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5102::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:00, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:00, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.3:65500::5103::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.3:65500::5104::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5104::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.3:65500::5105::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5106::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5107::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5109::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 1w3d 02:38:53, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 1w3d 02:38:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 1w3d 02:38:53, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.4:65500::5102::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.4:65500::5103::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5104::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 5d 05:27:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                       to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.4:65500::5105::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5107::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5109::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5110::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 21:18:31
                       Indirect
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 21:18:31
                       Indirect
2:192.168.1.5:65500::5102::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:20:39
                       Indirect
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:03:51
                       Indirect
2:192.168.1.5:65500::5104::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:15:03
                       Indirect
2:192.168.1.5:65500::5105::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:20:20
                       Indirect
2:192.168.1.5:65500::5106::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:18:05
                       Indirect
2:192.168.1.5:65500::5107::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:17:59
                       Indirect
2:192.168.1.5:65500::5108::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:17:51
                       Indirect
2:192.168.1.5:65500::5109::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:17:47
                       Indirect
2:192.168.1.5:65500::5110::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 18:17:41
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5101
2:192.168.1.1:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5102::2c:6b:f5:3e:e0:f0::10.200.102.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5102
2:192.168.1.1:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5103::2c:6b:f5:3e:e0:f0::10.200.103.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5103
2:192.168.1.1:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5104::2c:6b:f5:3e:e0:f0::10.200.104.252/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5104
2:192.168.1.1:8::5105::2c:6b:f5:3e:e0:f0::10.200.105.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5106::2c:6b:f5:3e:e0:f0::10.200.106.254/304 MAC/IP
                   *[BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.1:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5101
2:192.168.1.2:8::5102::00:00:5e:00:01:01::10.200.102.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5102::2c:6b:f5:b9:da:f0::10.200.102.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5102
2:192.168.1.2:8::5103::00:00:5e:00:01:01::10.200.103.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5103::2c:6b:f5:b9:da:f0::10.200.103.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5103
2:192.168.1.2:8::5104::00:00:5e:00:01:01::10.200.104.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5104::2c:6b:f5:b9:da:f0::10.200.104.253/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5104
2:192.168.1.2:8::5107::2c:6b:f5:b9:da:f0::10.200.107.254/304 MAC/IP
                   *[BGP/170] 3d 04:25:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5108::2c:6b:f5:b9:da:f0::10.200.108.254/304 MAC/IP
                   *[BGP/170] 3d 04:25:33, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:25:33, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5109::aa:aa:aa:aa:aa:09::10.200.109.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.2:8::5110::aa:aa:aa:aa:aa:10::10.200.110.254/304 MAC/IP
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5102::aa:bb:cc:80:60:00::10.200.102.1/304 MAC/IP
                   *[BGP/170] 00:07:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:07:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5102::aa:bb:cc:80:70:00::10.200.102.2/304 MAC/IP
                   *[BGP/170] 00:07:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:07:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5103::aa:bb:cc:80:70:00::10.200.103.2/304 MAC/IP
                   *[BGP/170] 00:28:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:28:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5105::aa:bb:cc:80:70:00::10.200.105.2/304 MAC/IP
                   *[BGP/170] 00:25:17, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:25:17, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5108::aa:bb:cc:80:70:00::10.200.108.2/304 MAC/IP
                   *[BGP/170] 00:16:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:16:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:60:00::10.200.110.1/304 MAC/IP
                   *[BGP/170] 00:15:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:15:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.3:65500::5110::aa:bb:cc:80:70:00::10.200.110.2/304 MAC/IP
                   *[BGP/170] 00:15:55, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:15:55, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[BGP/170] 00:03:52, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
                    [BGP/170] 00:03:52, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5106::aa:bb:cc:80:80:00::10.200.106.3/304 MAC/IP
                   *[BGP/170] 00:45:46, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:45:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.4:65500::5108::aa:bb:cc:80:80:00::10.200.108.3/304 MAC/IP
                   *[BGP/170] 00:45:15, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
                    [BGP/170] 00:45:15, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 319
                       to 172.16.25.0 via ge-0/0/2.0, Push 319
2:192.168.1.5:65500::5103::aa:bb:cc:80:90:00::10.200.103.4/304 MAC/IP
                   *[EVPN/170] 00:03:52
                       Indirect
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5102::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5103::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5104::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5105::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5106::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:24:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5109::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5110::192.168.1.1/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5102::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5103::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5104::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5107::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:25:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:25:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5108::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:25:35, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:25:35, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5109::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5110::192.168.1.2/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5102::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5103::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5104::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5105::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5106::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5107::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5108::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5109::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5110::192.168.1.3/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5102::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5103::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5104::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5105::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5106::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5107::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5108::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5109::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5110::192.168.1.4/248 IM
                   *[BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 3d 04:35:07, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 21:18:32
                       Indirect
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 21:18:32
                       Indirect
3:192.168.1.5:65500::5102::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5103::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5104::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5105::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5106::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5107::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5108::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5109::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect
3:192.168.1.5:65500::5110::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 18:46:01
                       Indirect

__default_evpn__.evpn.0: 3 destinations, 4 routes (3 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.5:0::09::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1w0d 21:18:24
                       Indirect
4:192.168.1.4:0::09:192.168.1.4/296 ES
                   *[BGP/170] 1w3d 02:38:57, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w3d 02:38:57, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
4:192.168.1.5:0::09:192.168.1.5/296 ES
                   *[EVPN/170] 1w0d 21:18:25
                       Indirect
```
