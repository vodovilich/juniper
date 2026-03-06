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


## HEAD


## HEAD 
