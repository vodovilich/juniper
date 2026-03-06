## ballsackcity baseline:
- **2 RRs, 2 Clusters**
- **No Multihomed CEs**
- **Type1 RDs**


## keep all
- bgp.l3vpn table by default created on:
  - PEs
  - RRs (can be a P router)
- ballsackcity - P router, no VRFs configured, no bgp.l2vpn table:
  - No routes displayed as received:
    - Despite 3.3.3.3 does send l3vpn NLRI
```
root@ballsackcity> show bgp summary
Threading mode: BGP I/O
Default eBGP mode: advertise - accept, receive - accept
Groups: 1 Peers: 2 Down peers: 0
Table          Tot Paths  Act Paths Suppressed    History Damp State    Pending
inet.0
                       8          0          0          0          0          0
bgp.l3vpn.0
                       0          0          0          0          0          0
Peer                     AS      InPkt     OutPkt    OutQ   Flaps Last Up/Dwn State|#Active/Received/Accepted/Damped...
3.3.3.3               65530        109         92       0       3       39:43 Establ
  inet.0: 0/4/4/0
  bgp.l3vpn.0: 0/0/0/0
5.5.5.5               65530        170        160       0       2     1:11:27 Establ
  inet.0: 0/4/4/0
  bgp.l3vpn.0: 0/0/0/0


root@ballsackcity> show route receive-protocol bgp 3.3.3.3 all | match bgp
root@ballsackcity>

```
  - Table exists, but empty (probably)

```
root@ballsackcity> show route table bgp.l3vpn.0

root@ballsackcity> show route table bgp.l33vpn.0
error: No routing tables matching specification.

```
- Changed by the *keep all* BGP configuration option:
```
[edit]
root@ballsackcity# set protocols bgp group INT keep ?
Possible completions:
  all                  Retain all routes
  none                 Retain no routes
[edit]
root@ballsackcity# set protocols bgp group INT keep all

```
- Output changed
```
root@ballsackcity> show bgp summary
Threading mode: BGP I/O
Default eBGP mode: advertise - accept, receive - accept
Groups: 1 Peers: 2 Down peers: 0
Table          Tot Paths  Act Paths Suppressed    History Damp State    Pending
inet.0
                       8          0          0          0          0          0
bgp.l3vpn.0
                      10          5          0          0          0          0
Peer                     AS      InPkt     OutPkt    OutQ   Flaps Last Up/Dwn State|#Active/Received/Accepted/Damped...
3.3.3.3               65530        134        111       0       3       47:25 Establ
  inet.0: 0/4/4/0
  bgp.l3vpn.0: 4/5/5/0
5.5.5.5               65530        196        180       0       2     1:19:09 Establ
  inet.0: 0/4/4/0
  bgp.l3vpn.0: 1/5/5/0

```

```
root@ballsackcity> show route receive-protocol bgp 3.3.3.3 all | match bgp
bgp.l3vpn.0: 5 destinations, 10 routes (5 active, 0 holddown, 0 hidden)

root@ballsackcity>
```
```
root@ballsackcity> show route table bgp.l3vpn.0

bgp.l3vpn.0: 5 destinations, 10 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1.1.1.1:1:10.10.10.255/32
                   *[BGP/170] 00:02:35, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65601 I, validation-state: unverified
                    >  to 192.168.12.11 via ge-0/0/0.0, Push 299856
                    [BGP/170] 00:02:35, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65601 I, validation-state: unverified
                    >  to 192.168.12.11 via ge-0/0/0.0, Push 299856
1.1.1.1:2:10.20.10.0/24
                   *[BGP/170] 00:02:35, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.12.11 via ge-0/0/0.0, Push 299888
                    [BGP/170] 00:02:35, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.12.11 via ge-0/0/0.0, Push 299888
3.3.3.3:2:10.20.30.0/24
                   *[BGP/170] 00:02:35, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.23.33 via ge-0/0/2.0, Push 299840
                    [BGP/170] 00:02:35, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.23.33 via ge-0/0/2.0, Push 299840
4.4.4.4:2:10.20.20.0/24
                   *[BGP/170] 00:02:35, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.24.44 via ge-0/0/1.0, Push 299856
                    [BGP/170] 00:02:35, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.24.44 via ge-0/0/1.0, Push 299856
5.5.5.5:1:10.10.20.255/32
                   *[BGP/170] 00:02:35, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65601 I, validation-state: unverified
                       to 192.168.24.44 via ge-0/0/1.0, Push 299840, Push 299824(top)
                    >  to 192.168.23.33 via ge-0/0/2.0, Push 299840, Push 299824(top)
                    [BGP/170] 00:02:35, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65601 I, validation-state: unverified
                       to 192.168.24.44 via ge-0/0/1.0, Push 299840, Push 299824(top)
                    >  to 192.168.23.33 via ge-0/0/2.0, Push 299840, Push 299824(top)
```
- By default **only BEST BGP paths are stored:**
  - *keep all* - keeps non-best routes
    - Useful when RD **Type 0** makes **prefixes from different PEs look the same:**
    - e.g. Multihomed CE
    - e.g. RRs are in same Cluster  
*PE1 → RD 100:1 → 10.20.20.0/24*  
*PE2 → RD 100:1 → 10.20.20.0/24*

## Route Target address family
- By default RR reflects all L3VPN routes to PEs:
  - **RDs contain all customers’ ArbitraryNumbers:**
```
root@cumshottown_rr> show route advertising-protocol bgp 4.4.4.4 table bgp.l3vpn.0

bgp.l3vpn.0: 6 destinations, 9 routes (6 active, 0 holddown, 0 hidden)
  Prefix                  Nexthop              MED     Lclpref    AS path
  1.1.1.1:1:10.10.10.255/32
*                         1.1.1.1              0       100        65601 I
  1.1.1.1:2:10.20.10.0/24
*                         1.1.1.1              0       100        65602 I
  3.3.3.3:2:10.20.30.0/24
*                         Self                 0       100        65602 I
  5.5.5.5:1:10.10.20.0/24
*                         5.5.5.5              0       100        65601 I
  5.5.5.5:1:10.20.20.0/24
*                         5.5.5.5              0       100        65601 I
```
- Enabling route-target family - RRs reflect only requested RTs to PEs
```
root@cumshottown_rr> show route table bgp.rtarget.0

bgp.rtarget.0: 2 destinations, 3 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0:0:0/0
                   *[RTarget/5] 00:05:16
                      Type Default
                       Local
65530:65530:2/96
                   *[RTarget/5] 00:05:18
                      Type Default
                       Local
                    [BGP/170] 00:05:16, localpref 100, from 4.4.4.4
                      AS path: I, validation-state: unverified
                    >  to 192.168.35.55 via ge-0/0/0.0, Push 299776
                       to 192.168.23.22 via ge-0/0/2.0, Push 299808
```
<img width="792" height="537" alt="image" src="https://github.com/user-attachments/assets/06adbebd-3482-451b-b625-a2ad37ba76be" />

- **RDs contain only attached customers’ ArbitraryNumbers:**  
```
root@cumshottown_rr> show route advertising-protocol bgp 4.4.4.4 table bgp.l3vpn.0

bgp.l3vpn.0: 6 destinations, 9 routes (6 active, 0 holddown, 0 hidden)
  Prefix                  Nexthop              MED     Lclpref    AS path
  1.1.1.1:2:10.20.10.0/24
*                         1.1.1.1              0       100        65602 I
  3.3.3.3:2:10.20.30.0/24
*                         Self                 0       100        65602 I
```

## vrf-tabel-label 
- Left - before, Right - after vrf-tabel-label:
  - Labels can be same by themselves but due to a coincidence:
<img width="1417" height="400" alt="image" src="https://github.com/user-attachments/assets/12d69200-1728-4ec5-ac19-9484b676e8bd" />

## Route leak between VRF
- Create import policies policies:
```
set policy-options policy-statement A-to-B-POLICY term 1 from route-filter 10.10.10.255/32 exact
set policy-options policy-statement A-to-B-POLICY term 1 then accept
```

- Create RIB groups for importing:
```
root@assville> show configuration routing-options rib-groups
A-to-B {
    import-rib [ CUSTOMER-A.inet.0 CUSTOMER-B.inet.0 ];
    import-policy A-to-B-POLICY;
}

```

- Apply RIB groups in BGP inet family unicast inside VRFs:
```
set routing-instances CUSTOMER-A protocols bgp group EXT family inet unicast rib-group A-to-B
```

- Verify table CUSTOMER-B contains prefix 10.10.10.255/32 from CUSTOMER-A:
```
root@assville> show route table CUSTOMER-B 10.0.0.0/8

CUSTOMER-B.inet.0: 7 destinations, 9 routes (7 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.10.10.255/32    *[BGP/170] 21:41:42, MED 0, localpref 100
                      AS path: 65601 I, validation-state: unverified
                    >  to 172.16.10.10 via ge-0/0/5.0
10.20.10.0/24      *[BGP/170] 1w1d 21:59:11, MED 0, localpref 100
                      AS path: 65602 I, validation-state: unverified
                    >  to 172.16.21.10 via ge-0/0/6.0
10.20.20.0/24      *[BGP/170] 22:52:46, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.12.22 via ge-0/0/0.0, Push 299872, Push 299808(top)
                    [BGP/170] 22:51:00, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.12.22 via ge-0/0/0.0, Push 299872, Push 299808(top)
10.20.30.0/24      *[BGP/170] 22:52:46, MED 0, localpref 100, from 3.3.3.3
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.13.33 via ge-0/0/1.0, Push 299888
                    [BGP/170] 22:51:00, MED 0, localpref 100, from 5.5.5.5
                      AS path: 65602 I, validation-state: unverified
                    >  to 192.168.13.33 via ge-0/0/1.0, Push 299888

```
