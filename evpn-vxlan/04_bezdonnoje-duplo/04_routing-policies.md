## Routing Policies
### DRAIN policy - Steer traffic when applied
- Create a policy called DRAIN on both SPINEs
  - **Do not apply** the policy but ensure that it can be applied to all BGP groups using only a single configuration command: `# set apply-groups DRAIN-GLOBAL-GROUP`
  - The policy should ensure that, **when applied, the local_SPINE becomes less likely to receive traffic** compared to other remote_SPINE
#### Both SPINEs
```
set policy-options policy-statement DRAIN term 1 then as-path-prepend "65200 65200"
set groups DRAIN-GLOBAL-GROUP protocols bgp group <*> export DRAIN
```
#### Verification
- Before
```
root@LEAF3# run show route 192.168.1.6
192.168.1.6/32     *[BGP/170] 1d 02:28:14, localpref 100                  //MULTIPATH HERE
                      AS path: 65200 65100 I, validation-state: unverified
                       to 172.16.13.0 via ge-0/0/1.0
                    >  to 172.16.23.0 via ge-0/0/2.0
                    [BGP/170] 1d 02:28:14, localpref 100
                      AS path: 65200 65100 I, validation-state: unverified
                    >  to 172.16.13.0 via ge-0/0/1.0
```
- Apply
```
root@SPINE1# set apply-groups DRAIN-GLOBAL-GROUP
[edit]
root@SPINE1# show | compare
[edit]
+ apply-groups DRAIN-GLOBAL-GROUP;
[edit]
root@SPINE1# show protocols bgp | display inheritance
group CORE-SPINE {
    hold-time 9;
    ##
    ## 'DRAIN' was inherited from group 'DRAIN-GLOBAL-GROUP'
    ##
    export [ LOOPBACK-to-BGP DRAIN ];
    peer-as 65100;
    neighbor 172.16.16.0;
    neighbor 172.16.17.0;
}
group SPINE-LEAF {
    hold-time 9;
    advertise-peer-as;
    ##
    ## 'DRAIN' was inherited from group 'DRAIN-GLOBAL-GROUP'
    ##
    export [ LOOPBACK-to-BGP DRAIN ];
    peer-as 65300;
    neighbor 172.16.13.1;
    neighbor 172.16.14.1;
    neighbor 172.16.15.1;
}

```
- After
```
root@LEAF5> show route 192.168.1.7
192.168.1.7/32     *[BGP/170] 1d 02:38:21, localpref 100                  //NO MULTIPATH HERE
                      AS path: 65200 65100 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 00:00:07, localpref 100
                      AS path: 65200 65200 65200 65100 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
```

### StandardCommy per-LEAF
- Ensure that COREs can use standard communities to differentiate between the routes that were received from the LEAVEs when using show commands
#### LEAF3
```
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options policy-stat LOOPBACK-to-BGP term LOOPBACK_0 then community add  LEAF3 
set policy-options policy-stat DIRECT-to-BGP term ge-0/0/8_ALL-GWs then community add  LEAF3 
```
#### LEAF4
```
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options policy-stat LOOPBACK-to-BGP term LOOPBACK_0 then community add  LEAF4
```
#### LEAF5
```
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
set policy-options policy-stat LOOPBACK-to-BGP term LOOPBACK_0  then community add  LEAF5
set policy-options policy-stat DIRECT-to-BGP term ge-0/0/7_ALL-GWs then community add  LEAF5
```
#### Both COREs
```
set policy-options community LEAF3 members 65500:3
set policy-options community LEAF4 members 65500:4
set policy-options community LEAF5 members 65500:5
```
#### Verificiation:
```
root@CORE6> show route community-name LEAF3

inet.0: 28 destinations, 43 routes (28 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.110.0/24    *[BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.111.0/24    *[BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.112.0/24    *[BGP/170] 1d 07:34:08, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.113.0/24    *[BGP/170] 1d 07:34:08, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.114.0/24    *[BGP/170] 1d 07:34:08, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
10.200.115.0/24    *[BGP/170] 1d 07:34:08, localpref 100, from 172.16.26.1
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
                       to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:34:08, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0
192.168.1.3/32     *[BGP/170] 1d 07:51:31, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                       to 172.16.16.1 via ge-0/0/1.0
                    >  to 172.16.26.1 via ge-0/0/2.0
                    [BGP/170] 1d 07:51:31, localpref 100
                      AS path: 65200 65300 I, validation-state: unverified
                    >  to 172.16.16.1 via ge-0/0/1.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)

bgp.evpn.0: 21 destinations, 21 routes (21 active, 0 holddown, 0 hidden)

VLAN-AWARE_FABRIC-EVI.evpn.0: 20 destinations, 20 routes (20 active, 0 holddown, 0 hidden)

__default_evpn__.evpn.0: 1 destinations, 1 routes (1 active, 0 holddown, 0 hidden)
```
### LEAF5-to-CORE7 Path Tuning via SPINE1
- **LEAF5 should send traffic towards CORE7 via SPINE1** and use SPINE2 as backup
  - **LEAF5** must have a **policy applied at the BGP group** level
- **LEAF5** should continue to **load share towards CORE6, SPINE1 and SPINE2**
  - Before - LEAF5 is multipathing traffic to CORE7 via both SPINEs
```
root@LEAF5> show route 192.168.1.7
192.168.1.7/32     *[BGP/170] 1d 01:55:40, localpref 100, from 172.16.15.0
                      AS path: 65200 65100 I, validation-state: unverified
                       to 172.16.15.0 via ge-0/0/1.0
                    >  to 172.16.25.0 via ge-0/0/2.0
                    [BGP/170] 1d 01:55:40, localpref 100
                      AS path: 65200 65100 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
```
#### LEAF5
```
set policy-opt policy-stat CORE7-via-SPINE1 term 1 from route-filter 192.168.1.7/32 exact
set policy-opt policy-stat CORE7-via-SPINE1 term 1 from next-hop 172.16.15.0
set policy-opt policy-stat CORE7-via-SPINE1 term 1 then local-preference 110
set protocols bgp group SPINE-LEAF import CORE7-via-SPINE1
```
#### Verify
- After - LEAF5 is sending traffic to CORE7 via SPINE1
```
root@LEAF5> show route 192.168.1.7
192.168.1.7/32     *[BGP/170] 00:00:01, localpref 110                    //LP is 110 here
                      AS path: 65200 65100 I, validation-state: unverified
                    >  to 172.16.15.0 via ge-0/0/1.0
                    [BGP/170] 00:00:01, localpref 100
                      AS path: 65200 65100 I, validation-state: unverified
                    >  to 172.16.25.0 via ge-0/0/2.0
```

### Export into BGP any IRB on COREs
- Ensure IP connectivity between the servers with a layer 3 gateway on LEAF3/LEAF5 and servers in VNI 5240
#### Both COREs
```
set policy-options prefix-list IRB-ANY-PL apply-path "interfaces irb unit<*> family inet address<*>"
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB from protocol direct
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB from prefix-list IRB-ANY-PL
set policy-options policy-statement DIRECT-to-BGP term ANY-IRB then accept
set protocols bgp group CORE-SPINE export DIRECT-to-BGP
```
- Verification
```
root@LEAF3> ping 10.200.240.253 source  10.200.110.1
PING 10.200.240.253 (10.200.240.253): 56 data bytes
64 bytes from 10.200.240.253: icmp_seq=0 ttl=63 time=2.398 ms
64 bytes from 10.200.240.253: icmp_seq=1 ttl=63 time=2.374 ms
```
