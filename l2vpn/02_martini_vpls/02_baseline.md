## LDP-signalled VPWS
- CE-facing (sub)interfaces **encapsulation - vlan-ccc**
- **Protocol enabled - l2circuit**
- **VRF routing-instance config- removed**
- **Manual NBR specification**
- **l2circuit.0 route table**
<img width="507" height="137" alt="image" src="https://github.com/user-attachments/assets/255af77a-0533-482a-a93a-86cacaffa8a0" />

- **Service Labels are signalled via tLDP:**
  - Unicast LMMs  

```
root@PE1> show route table mpls | last 2
ge-0/0/1.601       *[L2CKT/7] 09:06:21, metric2 1
                    >  to 172.16.11.11 via ge-0/0/0.0, Push 299872, Push 299888(top) Offset: 252
```
<img width="1074" height="273" alt="image" src="https://github.com/user-attachments/assets/594ca54f-d9ab-4653-9b80-462686348b97" />

### PE1_LDP_VPWS_config
```
set interfaces ge-0/0/1 vlan-tagging
set interfaces ge-0/0/1 encapsulation vlan-ccc
set interfaces ge-0/0/1 unit 601 description Cust1_Site1
set interfaces ge-0/0/1 unit 601 encapsulation vlan-ccc
set interfaces ge-0/0/1 unit 601 vlan-id 601
set protocols l2circuit neighbor 2.2.2.2 interface ge-0/0/1.601 virtual-circuit-id 12
```


## LDP-signalled VPLS
- CE-facing (sub)interfaces **encapsulation - vlan-vpls**
- **Protocol enabled - RoutingInstance > vpls**
- **Manual NBR specification**
- l2circuit.0 route table

- **PE mpls table:**
```
root@PE2> show route table mpls

mpls.0: 13 destinations, 13 routes (13 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 2w2d 11:38:54, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 2w2d 11:38:54, metric 1
                       to table mpls.0
1                  *[MPLS/0] 2w2d 11:38:54, metric 1
                       Receive
2                  *[MPLS/0] 2w2d 11:38:54, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 2w2d 11:38:54, metric 1
                       to table mpls.0
13                 *[MPLS/0] 2w2d 11:38:54, metric 1
                       Receive
300016             *[LDP/9] 01:05:44, metric 1
                    >  to 172.16.22.22 via ge-0/0/0.0, Pop
300016(S=0)        *[LDP/9] 01:05:44, metric 1
                    >  to 172.16.22.22 via ge-0/0/0.0, Pop
300032             *[LDP/9] 01:05:44, metric 1
                    >  to 172.16.22.22 via ge-0/0/0.0, Swap 299776
300048             *[LDP/9] 01:05:44, metric 1
                    >  to 172.16.22.22 via ge-0/0/0.0, Swap 299840
300064             *[LDP/9] 01:05:44, metric 1
                    >  to 172.16.22.22 via ge-0/0/0.0, Swap 299856
800000             *[VPLS/7] 01:05:33
                    >  via vt-0/0/0.1048833, Pop
vt-0/0/0.1048833   *[VPLS/7] 01:05:33, metric2 1
                    >  to 172.16.22.22 via ge-0/0/0.0, Push 800000, Push 299856(top)
```
- VPLS VRF **MAC table:**
```
root@PE2> show vpls mac-table

MAC flags       (S -static MAC, D -dynamic MAC, L -locally learned, C -Control MAC
    O -OVSDB MAC, SE -Statistics enabled, NM -Non configured MAC, R -Remote PE MAC, P -Pinned MAC)

Routing instance : Customer1
 Bridging domain : __Customer1__, VLAN : NA
   MAC                 MAC      GBP     Logical          NH     MAC         active
   address             flags    Tag     interface        Index  property    source
   aa:bb:cc:00:60:00   D                vt-0/0/0.1048833
   aa:bb:cc:00:70:00   D                ge-0/0/1.601
   aa:bb:cc:00:80:00   D                vt-0/0/0.1048833
   aa:bb:cc:00:90:00   D                ge-0/0/2.601

```
- **VPLS connections:**
```
root@PE2> show vpls connections
Instance: Customer1
Edge protection: Not-Primary
  LDP-VPLS State
  VPLS-id: 100
  Mesh-group connections: __ves__
    Neighbor                  Type  St     Time last up          # Up trans
    1.1.1.1(vpls-id 100)      rmt   Up     Mar 26 08:21:50 2026           1
      Remote PE: 1.1.1.1, Negotiated control-word: No
      Incoming label: 800000, Outgoing label: 800000
      Negotiated PW status TLV: No
      Local interface: vt-0/0/0.1048833, Status: Up, Encapsulation: ETHERNET
        Description: Intf - vpls Customer1 neighbor 1.1.1.1 vpls-id 100
      Flow Label Transmit: No, Flow Label Receive: No
```
- **Service Labels are signalled via tLDP**:
  - **FEC type: PWid FEC Element - type128 (instead of prefix FEC - type 2)**
<img width="613" height="508" alt="image" src="https://github.com/user-attachments/assets/bfff4ff7-a9eb-4cc2-86e3-ca5f2a3a32bb" />

