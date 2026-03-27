# FEC129 VPWS
- BGP autodiscovers PEs;
- LDP signals the VPN
- SourceIDs are used to identify LSRs
- Interfaces encapsulation: vlan-ccc
- RoutingInstance gets:
  - Instance-type: l2vpn
  - l2vpn-id community in the format of: l2vpn-id:65530:1
  - protocols l2vpn > site > [ [interface, targetID], sourceID ]
- BGP > family auto-discovery-only

- ldp.l2vpn.0 table on PE1:
```
ldp.l2vpn.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

2.2.2.2:CtrlWord:4:65530:1:0.0.0.2:0.0.0.1/176
                   *[LDP/9] 00:17:38
                       Discard
2.2.2.2:CtrlWord:4:65530:1:0.0.0.4:0.0.0.3/176
                   *[LDP/9] 00:17:38
                       Discard
```
# FEC129 VPLS
