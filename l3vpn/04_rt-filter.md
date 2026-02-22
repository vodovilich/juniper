## Configure
- **Using** `set routing-instances Customer1-VRF vrf-target target:65530:1` **accepts and adverties all prefixes in the VRF**
  - **Including peering PE-CE subnets 192.168.x.0/24**:
 ```
root@PE1> show route table Customer1-VRF.inet.0

Customer1-VRF.inet.0: 5 destinations, 5 routes (5 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.110.0.0/16      *[BGP/170] 11:36:07, MED 0, localpref 100
                      AS path: 65601 I, validation-state: unverified
                    >  to 192.168.11.2 via ge-0/0/1.0
10.120.0.0/16      *[BGP/170] 4d 00:36:49, MED 0, localpref 100, from 11.11.11.11
                      AS path: 65601 I, validation-state: unverified
                    >  to 172.16.11.11 via ge-0/0/0.0, Push 299920, Push 299856(top)
192.168.11.0/24    *[Direct/0] 1w2d 23:43:23
                    >  via ge-0/0/1.0
192.168.11.1/32    *[Local/0] 1w2d 23:43:23
                       Local via ge-0/0/1.0
192.168.22.0/24    *[BGP/170] 4d 00:36:49, localpref 100, from 11.11.11.11
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.11 via ge-0/0/0.0, Push 299920, Push 299856(top)
```

- **RT filtering allows to control import/export**:
```
delete routing-instances Customer1-VRF vrf-target

set policy-options community CUST-A_RT-FILTER members target:65530:1

set policy-options policy-statement CUST-A_EXPORT term 1_ACCEPT_BGP from protocol bgp 
set policy-options policy-statement CUST-A_EXPORT term 1_ACCEPT_BGP then community add CUST-A_RT-FILTER
set policy-options policy-statement CUST-A_EXPORT term 1_ACCEPT_BGP then accept
set policy-options policy-statement CUST-A_EXPORT term 2_DROP_ANY then reject

set policy-options policy-statement CUST-A_IMPORT term 1_ACCEPT_BGP from protocol bgp 
set policy-options policy-statement CUST-A_IMPORT term 1_ACCEPT_BGP from community CUST-A_RT-FILTER
set policy-options policy-statement CUST-A_IMPORT term 1_ACCEPT_BGP then accept
set policy-options policy-statement CUST-A_IMPORT term 2_DROP_ANY then reject

set routing-instance Customer1-VRF vrf-import CUST-A_IMPORT
set routing-instance Customer1-VRF vrf-export CUST-A_EXPORT
```

## Verify

- **Peering subnets disappeared from the route table**:
```
root@PE1> show route table Customer1-VRF.inet.0

Customer1-VRF.inet.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.110.0.0/16      *[BGP/170] 00:32:22, MED 0, localpref 100
                      AS path: 65601 I, validation-state: unverified
                    >  to 192.168.11.2 via ge-0/0/1.0
10.120.0.0/16      *[BGP/170] 00:32:26, MED 0, localpref 100, from 11.11.11.11
                      AS path: 65601 I, validation-state: unverified
                    >  to 172.16.11.11 via ge-0/0/0.0, Push 299920, Push 299856(top)
192.168.11.0/24    *[Direct/0] 1w3d 00:27:43
                    >  via ge-0/0/1.0
192.168.11.1/32    *[Local/0] 1w3d 00:27:43
                       Local via ge-0/0/1.0
```

- **PE devices lost ability to ping each other (src_ip is from peering subnet - not reachable now)**:
```
root@PE1> ping routing-instance Customer1-VRF 10.120.20.10
PING 10.120.20.10 (10.120.20.10): 56 data bytes
^C
--- 10.120.20.10 ping statistics ---
49 packets transmitted, 0 packets received, 100% packet loss
```

- **Customer's sites can interact normally:**
```
CE1-R1# ping 10.120.20.10 source 10.110.20.1
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 10.120.20.10, timeout is 2 seconds:
Packet sent with a source address of 10.110.20.1
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 2/2/3 ms
```

- **Some options to try validate connectivity between PE devices:**
```
root@PE1> ping mpls ldp 2.2.2.2
!!!!!
--- lsping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss

root@PE1> traceroute mpls ldp 2.2.2.2
  Probe options: ttl 64, retries 3, wait 10, paths 16, exp 7, fanout 16
  ttl    Label  Protocol    Address          Previous Hop     Probe Status
    1   299856  LDP         172.16.11.11     (null)           Success
  FEC-Stack-Sent: LDP
  ttl    Label  Protocol    Address          Previous Hop     Probe Status
    2   299840  LDP         172.16.12.22     172.16.11.11     Success
  FEC-Stack-Sent: LDP
  ttl    Label  Protocol    Address          Previous Hop     Probe Status
    3        3  LDP         172.16.22.2      172.16.12.22     Egress
  FEC-Stack-Sent: LDP
  Path 1 via ge-0/0/0.0 destination 127.0.0.64
```
```
root@PE1> ping mpls ldp 2.2.2.2
!!!!!
--- lsping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss
```
<img width="1409" height="937" alt="image" src="https://github.com/user-attachments/assets/3a4aed53-a0e6-4d0c-8596-e496a0f31549" />
