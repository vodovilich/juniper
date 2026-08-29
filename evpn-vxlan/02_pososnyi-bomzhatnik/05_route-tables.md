### SPINE1

```
root@SPINE1> show route

inet.0: 15 destinations, 17 routes (15 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.100.0/24    *[Direct/0] 3d 09:57:48
                    >  via irb.100
10.200.100.252/32  *[Local/0] 3d 09:57:48
                       Local via irb.100
10.200.101.0/24    *[Direct/0] 2d 23:28:31
                    >  via irb.101
10.200.101.252/32  *[Local/0] 2d 23:28:31
                       Local via irb.101
172.16.13.0/31     *[Direct/0] 1w2d 10:33:21
                    >  via ge-0/0/3.0
172.16.13.0/32     *[Local/0] 1w2d 10:33:21
                       Local via ge-0/0/3.0
172.16.14.0/31     *[Direct/0] 1w2d 10:33:21
                    >  via ge-0/0/4.0
172.16.14.0/32     *[Local/0] 1w2d 10:33:21
                       Local via ge-0/0/4.0
172.16.15.0/31     *[Direct/0] 1w2d 10:33:21
                    >  via ge-0/0/5.0
172.16.15.0/32     *[Local/0] 1w2d 10:33:21
                       Local via ge-0/0/5.0
192.168.1.1/32     *[Direct/0] 1w2d 10:39:25
                    >  via lo0.0
192.168.1.2/32     *[BGP/170] 4d 08:19:11, localpref 100, from 172.16.13.1
                      AS path: 65003 65002 I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
                    [BGP/170] 4d 08:19:11, localpref 100
                      AS path: 65004 65002 I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
                    [BGP/170] 1w1d 08:43:43, localpref 100
                      AS path: 65005 65002 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
192.168.1.3/32     *[BGP/170] 1w1d 08:43:43, localpref 100
                      AS path: 65003 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
192.168.1.4/32     *[BGP/170] 5d 10:12:02, localpref 100
                      AS path: 65004 I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
192.168.1.5/32     *[BGP/170] 1w1d 08:43:43, localpref 100
                      AS path: 65005 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 1w2d 11:05:09
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1w2d 11:05:20
                       MultiRecv

bgp.evpn.0: 46 destinations, 46 routes (46 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 3d 09:57:48
                       Indirect
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 23:28:31
                       Indirect
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:54:20, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:54:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:27:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:20:20, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[EVPN/170] 3d 09:57:47
                       Indirect
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[EVPN/170] 2d 23:28:29
                       Indirect
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:27:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0

VLAN-AWARE_FABRIC-EVI.evpn.0: 44 destinations, 44 routes (44 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:54:20, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:54:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5101
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 4d 07:40:58, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:30:45, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[EVPN/170] 3d 09:57:48
                       Indirect
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[EVPN/170] 2d 23:28:31
                       Indirect
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                       to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 09:35:02, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5100
                       to 172.16.14.1 via ge-0/0/4.0, Push 5100
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                       to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:27:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0, Push 5101
                       to 172.16.14.1 via ge-0/0/4.0, Push 5101
                    >  to 172.16.15.1 via ge-0/0/5.0, Push 5101
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:27:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:20:20, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0, Push 5100
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[EVPN/170] 3d 09:57:47
                       Indirect
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[EVPN/170] 2d 23:28:29
                       Indirect
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
                       to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:27:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                       to 172.16.13.1 via ge-0/0/3.0
                    >  to 172.16.14.1 via ge-0/0/4.0
                       to 172.16.15.1 via ge-0/0/5.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:30, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0

__default_evpn__.evpn.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 3d 09:57:48
                       Indirect
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 23:28:31
                       Indirect
```

### SPINE2
```
root@SPINE2> show route

inet.0: 15 destinations, 23 routes (15 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.100.0/24    *[Direct/0] 3d 09:35:56
                    >  via irb.100
10.200.100.253/32  *[Local/0] 3d 09:35:56
                       Local via irb.100
10.200.101.0/24    *[Direct/0] 2d 23:28:41
                    >  via irb.101
10.200.101.253/32  *[Local/0] 2d 23:28:41
                       Local via irb.101
172.16.23.0/31     *[Direct/0] 1w2d 10:32:48
                    >  via ge-0/0/3.0
172.16.23.0/32     *[Local/0] 1w2d 10:32:48
                       Local via ge-0/0/3.0
172.16.24.0/31     *[Direct/0] 1w2d 10:32:48
                    >  via ge-0/0/4.0
172.16.24.0/32     *[Local/0] 1w2d 10:32:48
                       Local via ge-0/0/4.0
172.16.25.0/31     *[Direct/0] 1w2d 10:32:48
                    >  via ge-0/0/5.0
172.16.25.0/32     *[Local/0] 1w2d 10:32:48
                       Local via ge-0/0/5.0
192.168.1.1/32     *[BGP/170] 4d 08:20:05, localpref 100, from 172.16.23.1
                      AS path: 65003 65001 I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                    >  to 172.16.24.1 via ge-0/0/4.0
                       to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 4d 08:20:05, localpref 100
                      AS path: 65004 65001 I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w1d 08:43:55, localpref 100
                      AS path: 65005 65001 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
192.168.1.2/32     *[Direct/0] 1w2d 10:39:28
                    >  via lo0.0
192.168.1.3/32     *[BGP/170] 1w1d 08:43:55, localpref 100
                      AS path: 65003 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
                    [BGP/170] 4d 08:20:05, localpref 100
                      AS path: 65004 65001 65003 I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 1w1d 08:43:55, localpref 100
                      AS path: 65005 65001 65003 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
192.168.1.4/32     *[BGP/170] 4d 08:20:05, localpref 100
                      AS path: 65004 I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
                    [BGP/170] 4d 08:20:05, localpref 100
                      AS path: 65003 65001 65004 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
                    [BGP/170] 5d 10:12:55, localpref 100
                      AS path: 65005 65001 65004 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
192.168.1.5/32     *[BGP/170] 1w1d 08:43:55, localpref 100
                      AS path: 65005 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
                    [BGP/170] 1w1d 08:43:55, localpref 100
                      AS path: 65003 65001 65005 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
                    [BGP/170] 4d 08:20:05, localpref 100
                      AS path: 65004 65001 65005 I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 1w2d 11:05:55
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1w2d 11:06:06
                       MultiRecv

bgp.evpn.0: 46 destinations, 46 routes (46 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:29:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 3d 09:35:56
                       Indirect
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 23:28:41
                       Indirect
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:55:14, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:55:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:28:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:21:14, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[EVPN/170] 3d 09:35:54
                       Indirect
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[EVPN/170] 2d 23:28:40
                       Indirect
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101

VLAN-AWARE_FABRIC-EVI.evpn.0: 44 destinations, 44 routes (44 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:29:24, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0
                       to 172.16.24.1 via ge-0/0/4.0
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:55:14, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:55:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5100
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 4d 07:39:22, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 09:58:42, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
                       to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[EVPN/170] 3d 09:35:56
                       Indirect
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[EVPN/170] 2d 23:28:41
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:28:15, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:21:14, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
                       to 172.16.24.1 via ge-0/0/4.0, Push 5100
                       to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                       to 172.16.23.1 via ge-0/0/3.0, Push 5101
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
                       to 172.16.25.1 via ge-0/0/5.0, Push 5101
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[EVPN/170] 3d 09:35:54
                       Indirect
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[EVPN/170] 2d 23:28:40
                       Indirect
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5100
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0, Push 5101
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5100
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0, Push 5101
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5100
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:28:41, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0, Push 5101

__default_evpn__.evpn.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 3d 09:35:56
                       Indirect
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 23:28:41
                       Indirect
```

### LEAF3
```
root@LEAF3> show route

inet.0: 9 destinations, 11 routes (9 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.13.0/31     *[Direct/0] 1w2d 10:32:35
                    >  via ge-0/0/1.0
172.16.13.1/32     *[Local/0] 1w2d 10:32:35
                       Local via ge-0/0/1.0
172.16.23.0/31     *[Direct/0] 1w2d 10:32:35
                    >  via ge-0/0/2.0
172.16.23.1/32     *[Local/0] 1w2d 10:32:35
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 1w1d 08:44:33, localpref 100
                      AS path: 65001 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 1w1d 08:44:33, localpref 100
                      AS path: 65002 I, validation-state: unverified
                     >  to 172.16.23.0 via ge-0/0/2.0
192.168.1.3/32     *[Direct/0] 1w2d 10:37:40
                    >  via lo0.0
192.168.1.4/32     *[BGP/170] 4d 08:20:44, localpref 100, from 172.16.13.0
                      AS path: 65001 65004 I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 4d 08:20:44, localpref 100
                      AS path: 65002 65004 I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
192.168.1.5/32     *[BGP/170] 1w1d 08:44:33, localpref 100, from 172.16.13.0
                      AS path: 65001 65005 I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1w1d 08:44:33, localpref 100
                      AS path: 65002 65005 I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 1w2d 11:06:25
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1w2d 11:06:36
                       MultiRecv

bgp.evpn.0: 50 destinations, 50 routes (50 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:59:21, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:36:36, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:29:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:55:54, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:56:05, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 05:58:16, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 1w0d 05:58:27, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:29:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:29:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w1d 00:11:56
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:47:02
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:43:17
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 00:24:08
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 2d 23:54:43
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 2d 23:53:44
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:00:06, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:48:20, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:30:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 02:47:09, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:29:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:29:21, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[EVPN/170] 00:28:55
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00::10.200.100.2/304 MAC/IP
                   *[EVPN/170] 00:00:07
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:21:53, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:06, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:06, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:53:50, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:30:03, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:53:50, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:29:19, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[EVPN/170] 1w1d 03:01:59
                       Indirect
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[EVPN/170] 3d 00:25:19
                       Indirect
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:53:50, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:53:50, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:53:50, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:53:50, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0

default-switch.evpn.0: 50 destinations, 50 routes (50 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:59:22, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:36:37, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:29:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:55:55, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:56:06, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 1w0d 05:58:17, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 1w0d 05:58:28, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:29:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:29:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 1w1d 00:11:57
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:47:03
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:43:18
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[EVPN/170] 3d 00:24:09
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[EVPN/170] 2d 23:54:44
                       Indirect
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[EVPN/170] 2d 23:53:45
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:00:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:53:52, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5101
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:48:21, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:30:05, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 02:47:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:29:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:29:22, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[EVPN/170] 00:28:56
                       Indirect
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00::10.200.100.2/304 MAC/IP
                   *[EVPN/170] 00:00:08
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:21:54, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:07, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 318
                       to 172.16.23.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:30:04, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:29:20, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[EVPN/170] 1w1d 03:02:00
                       Indirect
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[EVPN/170] 3d 00:25:20
                       Indirect
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:53:51, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
```

### LEAF4
```
root@LEAF4> show route

inet.0: 9 destinations, 13 routes (9 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.14.0/31     *[Direct/0] 1w2d 10:30:52
                    >  via ge-0/0/1.0
172.16.14.1/32     *[Local/0] 1w2d 10:30:52
                       Local via ge-0/0/1.0
172.16.24.0/31     *[Direct/0] 4d 08:21:16
                    >  via ge-0/0/2.0
172.16.24.1/32     *[Local/0] 4d 08:21:16
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 5d 10:14:03, localpref 100
                      AS path: 65001 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                    [BGP/170] 4d 08:21:11, localpref 100
                      AS path: 65002 65003 65001 I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
192.168.1.2/32     *[BGP/170] 4d 08:21:11, localpref 100
                      AS path: 65002 I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 5d 10:14:03, localpref 100
                      AS path: 65001 65003 65002 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
192.168.1.3/32     *[BGP/170] 4d 08:21:11, localpref 100, from 172.16.14.0
                      AS path: 65001 65003 I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 4d 08:21:11, localpref 100
                      AS path: 65002 65003 I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
192.168.1.4/32     *[Direct/0] 1w2d 10:30:52
                    >  via lo0.0
192.168.1.5/32     *[BGP/170] 4d 08:21:11, localpref 100, from 172.16.14.0
                      AS path: 65001 65005 I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 4d 08:21:11, localpref 100
                      AS path: 65002 65005 I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe04:0/128
                   *[Local/0] 1w2d 11:07:04
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1w2d 11:07:15
                       MultiRecv

bgp.evpn.0: 52 destinations, 52 routes (52 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:59:48, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:37:03, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:29:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 23:56:21
                       Indirect
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[EVPN/170] 2d 23:56:32
                       Indirect
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 10:14:01, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 5d 10:14:01, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:29:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:29:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:55:09, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:54:11, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:43:44
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:00:34
                       Indirect
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 2d 23:55:26
                       Indirect
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:48:47, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:30:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 02:46:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:29:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:29:48, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:29:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00::10.200.100.2/304 MAC/IP
                   *[BGP/170] 00:00:33, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[EVPN/170] 00:22:21
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[EVPN/170] 00:00:34
                       Indirect
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:33, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 00:03:28, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:30:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 00:03:28, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:29:46, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 3d 00:03:28, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 3d 00:03:28, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[EVPN/170] 1w1d 03:02:17
                       Indirect
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[EVPN/170] 3d 00:25:31
                       Indirect
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 3d 00:03:28, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:57:26, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
4:192.168.1.4:0::11:192.168.1.4/296 ES
                   *[EVPN/170] 2d 23:56:23
                       Indirect
4:192.168.1.5:0::11:192.168.1.5/296 ES
                   *[BGP/170] 5d 10:14:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0

default-switch.evpn.0: 49 destinations, 49 routes (49 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:59:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:37:04, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:29:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[EVPN/170] 2d 23:56:33
                       Indirect
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 5d 10:14:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[BGP/170] 5d 10:14:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:29:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:29:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:30, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5101
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5101
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:55:10, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:54:12, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:43:45
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 00:00:35
                       Indirect
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[EVPN/170] 2d 23:55:27
                       Indirect
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 2d 23:48:48, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:30:32, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 02:46:30, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:29:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:29:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:29:22, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00::10.200.100.2/304 MAC/IP
                   *[BGP/170] 00:00:34, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[EVPN/170] 00:22:22
                       Indirect
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[EVPN/170] 00:00:35
                       Indirect
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:34, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 318
                       to 172.16.24.0 via ge-0/0/2.0, Push 318
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 3d 00:03:29, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:30:31, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 3d 00:03:29, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:29:47, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 3d 00:03:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 3d 00:03:29, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[EVPN/170] 1w1d 03:02:18
                       Indirect
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[EVPN/170] 3d 00:25:32
                       Indirect
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[BGP/170] 3d 00:03:29, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[BGP/170] 2d 23:57:27, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0

__default_evpn__.evpn.0: 3 destinations, 3 routes (3 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 23:56:22
                       Indirect
4:192.168.1.4:0::11:192.168.1.4/296 ES
                   *[EVPN/170] 2d 23:56:23
                       Indirect
4:192.168.1.5:0::11:192.168.1.5/296 ES
                   *[BGP/170] 5d 10:14:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
```

### LEAF5
```
root@LEAF5> show route

inet.0: 9 destinations, 13 routes (9 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.15.0/31     *[Direct/0] 1w2d 10:29:51
                    >  via ge-0/0/1.0
172.16.15.1/32     *[Local/0] 1w2d 10:29:51
                       Local via ge-0/0/1.0
172.16.25.0/31     *[Direct/0] 1w2d 10:29:51
                    >  via ge-0/0/2.0
172.16.25.1/32     *[Local/0] 1w2d 10:29:51
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 1w1d 08:45:14, localpref 100
                      AS path: 65001 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 1w1d 00:22:14, localpref 100
                      AS path: 65002 65003 65001 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.2/32     *[BGP/170] 1w1d 08:45:14, localpref 100
                      AS path: 65002 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w1d 08:45:14, localpref 100
                      AS path: 65001 65003 65002 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
192.168.1.3/32     *[BGP/170] 1w1d 08:45:14, localpref 100, from 172.16.15.0
                      AS path: 65001 65003 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1w1d 08:45:14, localpref 100
                      AS path: 65002 65003 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.4/32     *[BGP/170] 4d 08:21:33, localpref 100, from 172.16.15.0
                      AS path: 65001 65004 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 4d 08:21:33, localpref 100
                      AS path: 65002 65004 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.5/32     *[Direct/0] 1w2d 10:29:51
                    >  via lo0.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 1w2d 11:07:10
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1w2d 11:07:21
                       MultiRecv

bgp.evpn.0: 52 destinations, 52 routes (52 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 10:00:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:37:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:56:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:56:54, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1w0d 05:59:04
                       Indirect
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[EVPN/170] 1w0d 05:59:15
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 06:07:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:55:32, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:54:33, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:00:56, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:55:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:44:05
                       Indirect
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 2d 23:49:09
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:29:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00::10.200.100.2/304 MAC/IP
                   *[BGP/170] 00:00:56, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:22:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:56, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[EVPN/170] 00:00:56
                       Indirect
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:30:52, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:30:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 05:59:14
                       Indirect
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[EVPN/170] 2d 23:57:48
                       Indirect
4:192.168.1.4:0::11:192.168.1.4/296 ES
                   *[BGP/170] 2d 23:56:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
4:192.168.1.5:0::11:192.168.1.5/296 ES
                   *[EVPN/170] 1w0d 05:59:05
                       Indirect

default-switch.evpn.0: 49 destinations, 49 routes (49 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.1:0::050000fde9000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 10:00:10, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.1:0::050000fde9000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 3d 09:37:25, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.2:0::050000fdea000013ed00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:0::11::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 23:56:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:65500::11::0/192 AD/EVI
                   *[BGP/170] 2d 23:56:54, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.5:65500::11::0/192 AD/EVI
                   *[EVPN/170] 1w0d 05:59:15
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 1w0d 06:07:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.3:65500::5101::aa:bb:cc:00:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5101::aa:bb:cc:80:60:00/304 MAC/IP
                   *[BGP/170] 2d 23:55:32, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5101::aa:bb:cc:80:70:00/304 MAC/IP
                   *[BGP/170] 2d 23:54:33, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[BGP/170] 00:00:56, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5101::aa:bb:cc:80:80:00/304 MAC/IP
                   *[BGP/170] 2d 23:55:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 1w0d 05:44:05
                       Indirect
2:192.168.1.5:65500::5101::aa:bb:cc:80:90:00/304 MAC/IP
                   *[EVPN/170] 2d 23:49:09
                       Indirect
2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5100
2:192.168.1.1:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.1:8::5101::2c:6b:f5:3e:e0:f0::10.200.101.252/304 MAC/IP
                   *[BGP/170] 2d 23:30:53, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
                   *[BGP/170] 3d 00:03:51, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5100
2:192.168.1.2:8::5101::00:00:5e:00:01:01::10.200.101.254/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.2:8::5101::2c:6b:f5:b9:da:f0::10.200.101.253/304 MAC/IP
                   *[BGP/170] 2d 23:30:10, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:60:00::10.200.100.1/304 MAC/IP
                   *[BGP/170] 00:29:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.3:65500::5100::aa:bb:cc:80:70:00::10.200.100.2/304 MAC/IP
                   *[BGP/170] 00:00:56, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:80:00::10.200.100.3/304 MAC/IP
                   *[BGP/170] 00:22:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.4:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[BGP/170] 00:00:56, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 318
                       to 172.16.25.0 via ge-0/0/2.0, Push 318
2:192.168.1.5:65500::5100::aa:bb:cc:80:90:00::10.200.100.4/304 MAC/IP
                   *[EVPN/170] 00:00:56
                       Indirect
3:192.168.1.1:8::5100::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.1:8::5101::192.168.1.1/248 IM
                   *[BGP/170] 2d 23:30:52, localpref 100, from 192.168.1.1
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
3:192.168.1.2:8::5100::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.2:8::5101::192.168.1.2/248 IM
                   *[BGP/170] 2d 23:30:08, localpref 100, from 192.168.1.2
                      AS path: I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5100::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.3:65500::5101::192.168.1.3/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5100::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.4:65500::5101::192.168.1.4/248 IM
                   *[BGP/170] 2d 23:57:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
3:192.168.1.5:65500::5100::192.168.1.5/248 IM
                   *[EVPN/170] 1w0d 05:59:14
                       Indirect
3:192.168.1.5:65500::5101::192.168.1.5/248 IM
                   *[EVPN/170] 2d 23:57:48
                       Indirect

__default_evpn__.evpn.0: 3 destinations, 3 routes (3 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.5:0::11::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1w0d 05:59:04
                       Indirect
4:192.168.1.4:0::11:192.168.1.4/296 ES
                   *[BGP/170] 2d 23:56:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
4:192.168.1.5:0::11:192.168.1.5/296 ES
                   *[EVPN/170] 1w0d 05:59:05
                       Indirect
```
