### CORE6
```
root@CORE6> show route | no-more

inet.0: 28 destinations, 43 routes (28 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.111.0/24    *[BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.112.0/24    *[BGP/170] 1d 08:37:02, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.113.0/24    *[BGP/170] 1d 08:37:02, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.114.0/24    *[BGP/170] 1d 08:37:02, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.115.0/24    *[BGP/170] 1d 08:37:02, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:02, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.130.0/24    *[BGP/170] 1d 08:53:45, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.131.0/24    *[BGP/170] 1d 08:53:45, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.132.0/24    *[BGP/170] 1d 08:53:45, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.133.0/24    *[BGP/170] 1d 08:53:45, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.134.0/24    *[BGP/170] 1d 08:53:45, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.135.0/24    *[BGP/170] 1d 08:53:45, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.240.0/24    *[Direct/0] 2d 08:59:17
                    >  via irb.240
10.200.240.252/32  *[Local/0] 2d 08:59:17
                       Local via irb.240
172.16.16.0/31     *[Direct/0] 3d 01:12:19
                    >  via ge-0/0/1.0
172.16.16.0/32     *[Local/0] 3d 01:12:19
                       Local via ge-0/0/1.0
172.16.26.0/31     *[Direct/0] 3d 01:12:19
                    >  via ge-0/0/2.0
172.16.26.0/32     *[Local/0] 3d 01:12:19
                       Local via ge-0/0/2.0
192.168.0.0/31     *[Direct/0] 2d 11:47:09
                    >  via ae0.0
192.168.0.0/32     *[Local/0] 2d 11:47:09
                       Local via ae0.0
192.168.1.1/32     *[BGP/170] 2d 10:00:33, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 2d 10:00:33, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.26.1 via ge-0/0/2.0
192.168.1.3/32     *[BGP/170] 1d 08:54:25, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:25, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
192.168.1.4/32     *[BGP/170] 1d 08:54:11, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:11, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
192.168.1.5/32     *[BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:53:45, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
192.168.1.6/32     *[Direct/0] 3d 01:12:19
                    >  via lo0.0
192.168.1.7/32     *[OSPF/10] 2d 11:47:00, metric 1
                    >  to 192.168.0.1 via ae0.0
224.0.0.5/32       *[OSPF/10] 2d 11:47:15, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 3d 01:27:14
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:27:25
                       MultiRecv

bgp.evpn.0: 21 destinations, 21 routes (21 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.6:0::050000fe4c0000147800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 08:59:17
                       Indirect
1:192.168.1.7:0::050000fe4c0000147800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0
2:192.168.1.3:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 00:04:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 08:45:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
2:192.168.1.6:8::5240::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 08:59:17
                       Indirect
2:192.168.1.6:8::5240::2c:6b:f5:ba:26:f0/304 MAC/IP
                   *[EVPN/170] 2d 08:59:18
                       Indirect
2:192.168.1.7:8::5240::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
2:192.168.1.3:65500::5240::2c:6b:f5:65:cc:c0::10.200.240.1/304 MAC/IP
                   *[BGP/170] 00:04:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0, Push 5240
                       to 172.16.26.1 via ge-0/0/2.0, Push 5240
2:192.168.1.6:8::5240::00:00:5e:00:01:01::10.200.240.254/304 MAC/IP
                   *[EVPN/170] 2d 08:59:17
                       Indirect
2:192.168.1.6:8::5240::2c:6b:f5:ba:26:f0::10.200.240.252/304 MAC/IP
                   *[EVPN/170] 2d 08:59:18
                       Indirect
2:192.168.1.7:8::5240::00:00:5e:00:01:01::10.200.240.254/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0::10.200.240.253/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
3:192.168.1.6:8::5240::192.168.1.6/248 IM
                   *[EVPN/170] 2d 08:59:17
                       Indirect
3:192.168.1.7:8::5240::192.168.1.7/248 IM
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240

VLAN-AWARE_FABRIC-EVI.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
1:192.168.1.7:0::050000fe4c0000147800::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0
2:192.168.1.3:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 00:04:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 08:45:51, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
2:192.168.1.6:8::5240::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 08:59:17
                       Indirect
2:192.168.1.6:8::5240::2c:6b:f5:ba:26:f0/304 MAC/IP
                   *[EVPN/170] 2d 08:59:18
                       Indirect
2:192.168.1.7:8::5240::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
2:192.168.1.3:65500::5240::2c:6b:f5:65:cc:c0::10.200.240.1/304 MAC/IP
                   *[BGP/170] 00:04:16, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0, Push 5240
                       to 172.16.26.1 via ge-0/0/2.0, Push 5240
2:192.168.1.6:8::5240::00:00:5e:00:01:01::10.200.240.254/304 MAC/IP
                   *[EVPN/170] 2d 08:59:17
                       Indirect
2:192.168.1.6:8::5240::2c:6b:f5:ba:26:f0::10.200.240.252/304 MAC/IP
                   *[EVPN/170] 2d 08:59:18
                       Indirect
2:192.168.1.7:8::5240::00:00:5e:00:01:01::10.200.240.254/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0::10.200.240.253/304 MAC/IP
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.26.1 via ge-0/0/2.0, Push 5240
3:192.168.1.6:8::5240::192.168.1.6/248 IM
                   *[EVPN/170] 2d 08:59:17
                       Indirect
3:192.168.1.7:8::5240::192.168.1.7/248 IM
                   *[BGP/170] 2d 08:59:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 192.168.0.1 via ae0.0, Push 5240

__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.6:0::050000fe4c0000147800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 08:59:17
                       Indirect
```
### CORE7
```
root@CORE7> show route | no-more

inet.0: 28 destinations, 43 routes (28 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0
                    >  to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.111.0/24    *[BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0
                    >  to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.112.0/24    *[BGP/170] 1d 08:37:55, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.113.0/24    *[BGP/170] 1d 08:37:55, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.114.0/24    *[BGP/170] 1d 08:37:55, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.115.0/24    *[BGP/170] 1d 08:37:55, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:37:55, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.130.0/24    *[BGP/170] 1d 08:54:38, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.131.0/24    *[BGP/170] 1d 08:54:38, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.132.0/24    *[BGP/170] 1d 08:54:38, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.133.0/24    *[BGP/170] 1d 08:54:38, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.134.0/24    *[BGP/170] 1d 08:54:38, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.135.0/24    *[BGP/170] 1d 08:54:38, localpref 100, from 172.16.27.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
10.200.240.0/24    *[Direct/0] 2d 09:00:25
                    >  via irb.240
10.200.240.253/32  *[Local/0] 2d 09:00:25
                       Local via irb.240
172.16.17.0/31     *[Direct/0] 3d 01:12:14
                    >  via ge-0/0/1.0
172.16.17.0/32     *[Local/0] 3d 01:12:14
                       Local via ge-0/0/1.0
172.16.27.0/31     *[Direct/0] 3d 01:12:14
                    >  via ge-0/0/2.0
172.16.27.0/32     *[Local/0] 3d 01:12:14
                       Local via ge-0/0/2.0
192.168.0.0/31     *[Direct/0] 2d 11:48:02
                    >  via ae0.0
192.168.0.1/32     *[Local/0] 2d 11:48:02
                       Local via ae0.0
192.168.1.1/32     *[BGP/170] 2d 10:01:30, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 2d 10:01:30, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.27.1 via ge-0/0/2.0
192.168.1.3/32     *[BGP/170] 1d 08:55:18, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0
                    >  to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:55:18, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
192.168.1.4/32     *[BGP/170] 1d 08:55:04, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0
                    >  to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:55:04, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
192.168.1.5/32     *[BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0
                    >  to 172.16.27.1 via ge-0/0/2.0
                    [BGP/170] 1d 08:54:38, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
192.168.1.6/32     *[OSPF/10] 2d 11:47:54, metric 1
                    >  to 192.168.0.0 via ae0.0
192.168.1.7/32     *[Direct/0] 3d 01:12:14
                    >  via lo0.0
224.0.0.5/32       *[OSPF/10] 2d 11:48:05, metric 1
                       MultiRecv

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 3d 01:26:37
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:26:48
                       MultiRecv

bgp.evpn.0: 13 destinations, 13 routes (13 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.7:0::050000fe4c0000147800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 09:00:25
                       Indirect
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 08:46:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.27.1 via ge-0/0/2.0, Push 5240
2:192.168.1.7:8::5240::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 09:00:25
                       Indirect
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0/304 MAC/IP
                   *[EVPN/170] 2d 09:00:25
                       Indirect
2:192.168.1.7:8::5240::00:00:5e:00:01:01::10.200.240.254/304 MAC/IP
                   *[EVPN/170] 2d 09:00:25
                       Indirect
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0::10.200.240.253/304 MAC/IP
                   *[EVPN/170] 2d 09:00:25
                       Indirect
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.27.1 via ge-0/0/2.0, Push 5240
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.27.1 via ge-0/0/2.0, Push 5240
3:192.168.1.7:8::5240::192.168.1.7/248 IM
                   *[EVPN/170] 2d 09:00:24
                       Indirect

VLAN-AWARE_FABRIC-EVI.evpn.0: 12 destinations, 12 routes (12 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 09:00:25, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 09:00:26, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 09:00:26, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 09:00:26, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.17.1 via ge-0/0/1.0
                       to 172.16.27.1 via ge-0/0/2.0
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 08:46:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.27.1 via ge-0/0/2.0, Push 5240
2:192.168.1.7:8::5240::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 2d 09:00:26
                       Indirect
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0/304 MAC/IP
                   *[EVPN/170] 2d 09:00:26
                       Indirect
2:192.168.1.7:8::5240::00:00:5e:00:01:01::10.200.240.254/304 MAC/IP
                   *[EVPN/170] 2d 09:00:26
                       Indirect
2:192.168.1.7:8::5240::2c:6b:f5:01:09:f0::10.200.240.253/304 MAC/IP
                   *[EVPN/170] 2d 09:00:26
                       Indirect
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[BGP/170] 2d 09:00:26, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.27.1 via ge-0/0/2.0, Push 5240
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[BGP/170] 2d 09:00:26, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.17.1 via ge-0/0/1.0, Push 5240
                    >  to 172.16.27.1 via ge-0/0/2.0, Push 5240
3:192.168.1.7:8::5240::192.168.1.7/248 IM
                   *[EVPN/170] 2d 09:00:25
                       Indirect

__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.7:0::050000fe4c0000147800::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 09:00:26
                       Indirect
```
### SPINE1
```
root@SPINE1> show route | no-more

inet.0: 27 destinations, 27 routes (27 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 08:38:22, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
10.200.111.0/24    *[BGP/170] 1d 08:38:22, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
10.200.112.0/24    *[BGP/170] 1d 08:38:22, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
10.200.113.0/24    *[BGP/170] 1d 08:38:22, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
10.200.114.0/24    *[BGP/170] 1d 08:38:22, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
10.200.115.0/24    *[BGP/170] 1d 08:38:22, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
10.200.130.0/24    *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
10.200.131.0/24    *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
10.200.132.0/24    *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
10.200.133.0/24    *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
10.200.134.0/24    *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
10.200.135.0/24    *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
172.16.13.0/31     *[Direct/0] 3d 01:07:30
                    >  via ge-0/0/3.0
172.16.13.0/32     *[Local/0] 3d 01:07:30
                       Local via ge-0/0/3.0
172.16.14.0/31     *[Direct/0] 3d 01:07:30
                    >  via ge-0/0/4.0
172.16.14.0/32     *[Local/0] 3d 01:07:30
                       Local via ge-0/0/4.0
172.16.15.0/31     *[Direct/0] 3d 01:07:30
                    >  via ge-0/0/5.0
172.16.15.0/32     *[Local/0] 3d 01:07:30
                       Local via ge-0/0/5.0
172.16.16.0/31     *[Direct/0] 3d 01:10:32
                    >  via ge-0/0/6.0
172.16.16.1/32     *[Local/0] 3d 01:10:32
                       Local via ge-0/0/6.0
172.16.17.0/31     *[Direct/0] 3d 01:10:32
                    >  via ge-0/0/7.0
172.16.17.1/32     *[Local/0] 3d 01:10:32
                       Local via ge-0/0/7.0
192.168.1.1/32     *[Direct/0] 3d 01:10:32
                    >  via lo0.0
192.168.1.3/32     *[BGP/170] 1d 08:55:45, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.13.1 via ge-0/0/3.0
192.168.1.4/32     *[BGP/170] 1d 08:55:31, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.14.1 via ge-0/0/4.0
192.168.1.5/32     *[BGP/170] 1d 08:55:05, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.15.1 via ge-0/0/5.0
192.168.1.7/32     *[BGP/170] 2d 11:42:59, localpref 100
                      AS path: 65100 I, validation-state: unverified
                    >  to 172.16.17.0 via ge-0/0/7.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe0a:0/128
                   *[Local/0] 3d 01:26:48
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:26:59
                       MultiRecv
```
### SPINE2
```
root@SPINE2> show route | no-more

inet.0: 27 destinations, 27 routes (27 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 08:38:52, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
10.200.111.0/24    *[BGP/170] 1d 08:38:52, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
10.200.112.0/24    *[BGP/170] 1d 08:38:52, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
10.200.113.0/24    *[BGP/170] 1d 08:38:52, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
10.200.114.0/24    *[BGP/170] 1d 08:38:52, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
10.200.115.0/24    *[BGP/170] 1d 08:38:52, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
10.200.130.0/24    *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
10.200.131.0/24    *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
10.200.132.0/24    *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
10.200.133.0/24    *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
10.200.134.0/24    *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
10.200.135.0/24    *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
172.16.23.0/31     *[Direct/0] 3d 01:04:58
                    >  via ge-0/0/3.0
172.16.23.0/32     *[Local/0] 3d 01:04:58
                       Local via ge-0/0/3.0
172.16.24.0/31     *[Direct/0] 3d 01:04:58
                    >  via ge-0/0/4.0
172.16.24.0/32     *[Local/0] 3d 01:04:58
                       Local via ge-0/0/4.0
172.16.25.0/31     *[Direct/0] 3d 01:04:58
                    >  via ge-0/0/5.0
172.16.25.0/32     *[Local/0] 3d 01:04:58
                       Local via ge-0/0/5.0
172.16.26.0/31     *[Direct/0] 3d 01:04:58
                    >  via ge-0/0/6.0
172.16.26.1/32     *[Local/0] 3d 01:04:58
                       Local via ge-0/0/6.0
172.16.27.0/31     *[Direct/0] 3d 01:04:58
                    >  via ge-0/0/7.0
172.16.27.1/32     *[Local/0] 3d 01:04:58
                       Local via ge-0/0/7.0
192.168.1.2/32     *[Direct/0] 3d 01:04:58
                    >  via lo0.0
192.168.1.3/32     *[BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.23.1 via ge-0/0/3.0
192.168.1.4/32     *[BGP/170] 1d 08:56:01, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.24.1 via ge-0/0/4.0
192.168.1.5/32     *[BGP/170] 1d 08:55:35, localpref 100
                      AS path: 65300 I, validation-state: unverified
                    >  to 172.16.25.1 via ge-0/0/5.0
192.168.1.7/32     *[BGP/170] 2d 11:42:53, localpref 100
                      AS path: 65100 I, validation-state: unverified
                    >  to 172.16.27.0 via ge-0/0/7.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe0b:0/128
                   *[Local/0] 3d 01:27:15
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:27:26
                       MultiRecv
```
### LEAF3
```
root@LEAF3> show route | no-more

inet.0: 27 destinations, 35 routes (27 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[Direct/0] 3d 00:51:44
                    >  via ge-0/0/8.110
10.200.110.1/32    *[Local/0] 3d 00:51:44
                       Local via ge-0/0/8.110
10.200.111.0/24    *[Direct/0] 3d 00:51:44
                    >  via ge-0/0/8.111
10.200.111.1/32    *[Local/0] 3d 00:51:44
                       Local via ge-0/0/8.111
10.200.112.0/24    *[Direct/0] 3d 00:51:44
                    >  via ge-0/0/8.112
10.200.112.1/32    *[Local/0] 3d 00:51:44
                       Local via ge-0/0/8.112
10.200.113.0/24    *[Direct/0] 3d 00:51:44
                    >  via ge-0/0/8.113
10.200.113.1/32    *[Local/0] 3d 00:51:44
                       Local via ge-0/0/8.113
10.200.114.0/24    *[Direct/0] 3d 00:51:44
                    >  via ge-0/0/8.114
10.200.114.1/32    *[Local/0] 3d 00:51:44
                       Local via ge-0/0/8.114
10.200.115.0/24    *[Direct/0] 3d 00:51:44
                    >  via ge-0/0/8.115
10.200.115.1/32    *[Local/0] 3d 00:51:44
                       Local via ge-0/0/8.115
10.200.130.0/24    *[BGP/170] 1d 08:56:15, localpref 100, from 172.16.23.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.131.0/24    *[BGP/170] 1d 08:56:15, localpref 100, from 172.16.23.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.132.0/24    *[BGP/170] 1d 08:56:15, localpref 100, from 172.16.23.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.133.0/24    *[BGP/170] 1d 08:56:15, localpref 100, from 172.16.23.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.134.0/24    *[BGP/170] 1d 08:56:15, localpref 100, from 172.16.23.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
10.200.135.0/24    *[BGP/170] 1d 08:56:15, localpref 100, from 172.16.23.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
172.16.13.0/31     *[Direct/0] 3d 01:02:22
                    >  via ge-0/0/1.0
172.16.13.1/32     *[Local/0] 3d 01:02:22
                       Local via ge-0/0/1.0
172.16.23.0/31     *[Direct/0] 3d 01:02:22
                    >  via ge-0/0/2.0
172.16.23.1/32     *[Local/0] 3d 01:02:22
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 2d 11:43:11, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 2d 11:43:11, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.23.0 via ge-0/0/2.0
192.168.1.3/32     *[Direct/0] 3d 01:02:22
                    >  via lo0.0
192.168.1.4/32     *[BGP/170] 1d 08:56:40, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:40, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
192.168.1.5/32     *[BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:15, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 3d 01:27:43
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:27:54
                       MultiRecv

bgp.evpn.0: 25 destinations, 25 routes (19 active, 0 holddown, 6 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 13:18:03
                       Indirect
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[EVPN/170] 2d 13:18:14
                       Indirect
2:192.168.1.4:65500::5220::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 2d 11:43:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5220
                       to 172.16.23.0 via ge-0/0/2.0, Push 5220
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 08:48:19, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 327
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 327
2:192.168.1.5:65500::5220::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5220
                       to 172.16.23.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5220::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5220
                       to 172.16.23.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5230::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00::10.200.230.2/304 MAC/IP
                   *[BGP/170] 1d 08:56:55, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5230
                       to 172.16.23.0 via ge-0/0/2.0, Push 5230
3:192.168.1.3:65500::5220::192.168.1.3/248 IM
                   *[EVPN/170] 2d 13:18:16
                       Indirect
3:192.168.1.3:65500::5230::192.168.1.3/248 IM
                   *[EVPN/170] 2d 13:18:16
                       Indirect
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[EVPN/170] 2d 09:08:16
                       Indirect
3:192.168.1.4:65500::5220::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5230::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5220::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5230::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
4:192.168.1.3:0::090a:192.168.1.3/296 ES
                   *[EVPN/170] 2d 13:18:04
                       Indirect
4:192.168.1.4:0::090a:192.168.1.4/296 ES
                   *[BGP/170] 2d 11:43:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0

default-switch.evpn.0: 22 destinations, 22 routes (16 active, 0 holddown, 6 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[EVPN/170] 2d 13:18:14
                       Indirect
2:192.168.1.4:65500::5220::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 2d 11:43:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5220
                       to 172.16.23.0 via ge-0/0/2.0, Push 5220
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 08:48:19, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 327
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 327
2:192.168.1.5:65500::5220::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5220
                       to 172.16.23.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5220::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5220
                       to 172.16.23.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5230::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:02, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.23.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00::10.200.230.2/304 MAC/IP
                   *[BGP/170] 1d 08:56:55, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0, Push 5230
                       to 172.16.23.0 via ge-0/0/2.0, Push 5230
3:192.168.1.3:65500::5220::192.168.1.3/248 IM
                   *[EVPN/170] 2d 13:18:16
                       Indirect
3:192.168.1.3:65500::5230::192.168.1.3/248 IM
                   *[EVPN/170] 2d 13:18:16
                       Indirect
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[EVPN/170] 2d 13:18:16
                       Indirect
3:192.168.1.4:65500::5220::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5230::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5220::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
3:192.168.1.5:65500::5230::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:39:31, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0

__default_evpn__.evpn.0: 3 destinations, 3 routes (3 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 13:18:03
                       Indirect
4:192.168.1.3:0::090a:192.168.1.3/296 ES
                   *[EVPN/170] 2d 13:18:04
                       Indirect
4:192.168.1.4:0::090a:192.168.1.4/296 ES
                   *[BGP/170] 2d 11:43:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
                       to 172.16.23.0 via ge-0/0/2.0
```

### LEAF4
```
root@LEAF4> show route | no-more

inet.0: 21 destinations, 35 routes (21 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.111.0/24    *[BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.112.0/24    *[BGP/170] 1d 08:40:16, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.113.0/24    *[BGP/170] 1d 08:40:16, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.114.0/24    *[BGP/170] 1d 08:40:16, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.115.0/24    *[BGP/170] 1d 08:40:16, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:16, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.130.0/24    *[BGP/170] 1d 08:56:59, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.131.0/24    *[BGP/170] 1d 08:56:59, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.132.0/24    *[BGP/170] 1d 08:56:59, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.133.0/24    *[BGP/170] 1d 08:56:59, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.134.0/24    *[BGP/170] 1d 08:56:59, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
10.200.135.0/24    *[BGP/170] 1d 08:56:59, localpref 100, from 172.16.24.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
172.16.14.0/31     *[Direct/0] 3d 01:02:33
                    >  via ge-0/0/1.0
172.16.14.1/32     *[Local/0] 3d 01:02:33
                       Local via ge-0/0/1.0
172.16.24.0/31     *[Direct/0] 3d 01:02:33
                    >  via ge-0/0/2.0
172.16.24.1/32     *[Local/0] 3d 01:02:33
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 2d 11:43:51, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 2d 11:43:51, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.24.0 via ge-0/0/2.0
192.168.1.3/32     *[BGP/170] 1d 08:57:39, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:57:39, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
192.168.1.4/32     *[Direct/0] 3d 01:02:33
                    >  via lo0.0
192.168.1.5/32     *[BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:56:59, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe04:0/128
                   *[Local/0] 3d 01:28:23
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:28:34
                       MultiRecv

bgp.evpn.0: 25 destinations, 25 routes (19 active, 0 holddown, 6 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 13:17:49
                       Indirect
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[EVPN/170] 2d 13:18:00
                       Indirect
2:192.168.1.4:65500::5220::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[EVPN/170] 2d 13:17:46
                       Indirect
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[EVPN/170] 08:49:04
                       Indirect
2:192.168.1.5:65500::5220::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5220
                       to 172.16.24.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5220::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5220
                       to 172.16.24.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5230::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00::10.200.230.2/304 MAC/IP
                   *[BGP/170] 1d 08:57:25, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5230
                       to 172.16.24.0 via ge-0/0/2.0, Push 5230
3:192.168.1.3:65500::5220::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5230::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.4:65500::5220::192.168.1.4/248 IM
                   *[EVPN/170] 2d 13:18:04
                       Indirect
3:192.168.1.4:65500::5230::192.168.1.4/248 IM
                   *[EVPN/170] 2d 13:18:03
                       Indirect
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[EVPN/170] 2d 09:08:54
                       Indirect
3:192.168.1.5:65500::5220::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5230::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
4:192.168.1.3:0::090a:192.168.1.3/296 ES
                   *[BGP/170] 2d 11:43:51, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
4:192.168.1.4:0::090a:192.168.1.4/296 ES
                   *[EVPN/170] 2d 13:17:50
                       Indirect

default-switch.evpn.0: 22 destinations, 22 routes (16 active, 0 holddown, 6 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[EVPN/170] 2d 13:18:00
                       Indirect
2:192.168.1.4:65500::5220::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[EVPN/170] 2d 13:17:46
                       Indirect
2:192.168.1.4:65500::5240::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[EVPN/170] 08:49:04
                       Indirect
2:192.168.1.5:65500::5220::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5220
                       to 172.16.24.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5220::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5220
                       to 172.16.24.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5230::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 2d 11:43:46, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.24.0 via ge-0/0/2.0, Push 5230
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00::10.200.230.2/304 MAC/IP
                   *[BGP/170] 1d 08:57:25, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0, Push 5230
                       to 172.16.24.0 via ge-0/0/2.0, Push 5230
3:192.168.1.3:65500::5220::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5230::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.3:65500::5240::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.4:65500::5220::192.168.1.4/248 IM
                   *[EVPN/170] 2d 13:18:04
                       Indirect
3:192.168.1.4:65500::5230::192.168.1.4/248 IM
                   *[EVPN/170] 2d 13:18:03
                       Indirect
3:192.168.1.4:65500::5240::192.168.1.4/248 IM
                   *[EVPN/170] 2d 13:18:03
                       Indirect
3:192.168.1.5:65500::5220::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
3:192.168.1.5:65500::5230::192.168.1.5/248 IM
                   *[BGP/170] 1d 08:57:24, localpref 100, from 192.168.1.5
                      AS path: I, validation-state: unverified
                       to 172.16.14.0 via ge-0/0/1.0
                    >  to 172.16.24.0 via ge-0/0/2.0

__default_evpn__.evpn.0: 3 destinations, 3 routes (3 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 13:17:50
                       Indirect
4:192.168.1.3:0::090a:192.168.1.3/296 ES
                   *[BGP/170] 2d 11:43:52, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.14.0 via ge-0/0/1.0
                       to 172.16.24.0 via ge-0/0/2.0
4:192.168.1.4:0::090a:192.168.1.4/296 ES
                   *[EVPN/170] 2d 13:17:51
                       Indirect
```
### LEAF5
```
root@LEAF5> show route | no-more

inet.0: 27 destinations, 35 routes (27 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.111.0/24    *[BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.112.0/24    *[BGP/170] 1d 08:40:56, localpref 100, from 172.16.25.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.113.0/24    *[BGP/170] 1d 08:40:56, localpref 100, from 172.16.25.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.114.0/24    *[BGP/170] 1d 08:40:56, localpref 100, from 172.16.25.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.115.0/24    *[BGP/170] 1d 08:40:56, localpref 100, from 172.16.25.0
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:40:56, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
10.200.130.0/24    *[Direct/0] 3d 00:51:17
                    >  via ge-0/0/7.130
10.200.130.1/32    *[Local/0] 3d 00:51:17
                       Local via ge-0/0/7.130
10.200.131.0/24    *[Direct/0] 3d 00:51:17
                    >  via ge-0/0/7.131
10.200.131.1/32    *[Local/0] 3d 00:51:17
                       Local via ge-0/0/7.131
10.200.132.0/24    *[Direct/0] 3d 00:51:17
                    >  via ge-0/0/7.132
10.200.132.1/32    *[Local/0] 3d 00:51:17
                       Local via ge-0/0/7.132
10.200.133.0/24    *[Direct/0] 3d 00:51:17
                    >  via ge-0/0/7.133
10.200.133.1/32    *[Local/0] 3d 00:51:17
                       Local via ge-0/0/7.133
10.200.134.0/24    *[Direct/0] 3d 00:51:17
                    >  via ge-0/0/7.134
10.200.134.1/32    *[Local/0] 3d 00:51:17
                       Local via ge-0/0/7.134
10.200.135.0/24    *[Direct/0] 3d 00:51:17
                    >  via ge-0/0/7.135
10.200.135.1/32    *[Local/0] 3d 00:51:17
                       Local via ge-0/0/7.135
172.16.15.0/31     *[Direct/0] 3d 01:02:36
                    >  via ge-0/0/1.0
172.16.15.1/32     *[Local/0] 3d 01:02:36
                       Local via ge-0/0/1.0
172.16.25.0/31     *[Direct/0] 3d 01:02:36
                    >  via ge-0/0/2.0
172.16.25.1/32     *[Local/0] 3d 01:02:36
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 2d 11:44:27, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 2d 11:44:27, localpref 100
                      AS path: 65200 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
192.168.1.3/32     *[BGP/170] 1d 08:52:49, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:58:20, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
192.168.1.4/32     *[BGP/170] 1d 08:52:49, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 08:58:05, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
192.168.1.5/32     *[Direct/0] 3d 01:02:36
                    >  via lo0.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 3d 01:28:52
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 01:29:03
                       MultiRecv

bgp.evpn.0: 16 destinations, 16 routes (16 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
2:192.168.1.4:65500::5220::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5220
                       to 172.16.25.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5220::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:19:20
                       Indirect
2:192.168.1.5:65500::5220::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:18:57
                       Indirect
2:192.168.1.5:65500::5230::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:19:19
                       Indirect
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:18:59
                       Indirect
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00::10.200.230.2/304 MAC/IP
                   *[EVPN/170] 2d 09:05:49
                       Indirect
3:192.168.1.3:65500::5220::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5220
                       to 172.16.25.0 via ge-0/0/2.0, Push 5220
3:192.168.1.3:65500::5230::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5230
3:192.168.1.4:65500::5220::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5220
                       to 172.16.25.0 via ge-0/0/2.0, Push 5220
3:192.168.1.4:65500::5230::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5230
3:192.168.1.5:65500::5220::192.168.1.5/248 IM
                   *[EVPN/170] 3d 00:10:47
                       Indirect
3:192.168.1.5:65500::5230::192.168.1.5/248 IM
                   *[EVPN/170] 3d 00:10:47
                       Indirect

default-switch.evpn.0: 16 destinations, 16 routes (16 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.3:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:0::090a::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
1:192.168.1.4:65500::090a::0/192 AD/EVI
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                       to 172.16.25.0 via ge-0/0/2.0
2:192.168.1.4:65500::5220::2c:6b:f5:65:cc:c0/304 MAC/IP
                   *[BGP/170] 2d 11:44:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5220
                       to 172.16.25.0 via ge-0/0/2.0, Push 5220
2:192.168.1.5:65500::5220::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:19:20
                       Indirect
2:192.168.1.5:65500::5220::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:18:57
                       Indirect
2:192.168.1.5:65500::5230::aa:bb:cc:00:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:19:19
                       Indirect
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 13:18:59
                       Indirect
2:192.168.1.5:65500::5230::aa:bb:cc:80:c0:00::10.200.230.2/304 MAC/IP
                   *[EVPN/170] 2d 09:05:49
                       Indirect
3:192.168.1.3:65500::5220::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5220
                       to 172.16.25.0 via ge-0/0/2.0, Push 5220
3:192.168.1.3:65500::5230::192.168.1.3/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5230
3:192.168.1.4:65500::5220::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0, Push 5220
                       to 172.16.25.0 via ge-0/0/2.0, Push 5220
3:192.168.1.4:65500::5230::192.168.1.4/248 IM
                   *[BGP/170] 1d 08:57:40, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0, Push 5230
                    >  to 172.16.25.0 via ge-0/0/2.0, Push 5230
3:192.168.1.5:65500::5220::192.168.1.5/248 IM
                   *[EVPN/170] 3d 00:10:47
                       Indirect
3:192.168.1.5:65500::5230::192.168.1.5/248 IM
                   *[EVPN/170] 3d 00:10:47
                       Indirect
```
