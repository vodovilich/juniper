## VLAN-Aware EVPN on SPINEs
- **RoutingInstance VLAN-AWARE_FABRIC-EVI on Spines = Global on Leaves**
### Configuration
- **To auto-generate a unique RD per configured Routing-Instance:**
```
route-distinguisher-id $ROUTERID 
```
#### SPINE1
```
set routing-options route-distinguisher-id 192.168.1.1
```
#### SPINE2
```
set routing-options route-distinguisher-id 192.168.1.2
```
#### Both SPINEs
```
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:1
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
!
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vlan-id 100
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 vxlan vni 5100
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list 5100
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5100 vrf-target target:65500:5100
!
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vlan-id 101
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 vxlan vni 5101
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list 5101
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn vni-options vni 5101 vrf-target target:65500:5101
```
### Verification
- **View local and remote VTEPs**
```
root@SPINE2> show l2-learning vxlan-tunnel-end-point source
Logical System Name       Id  SVTEP-IP         IFL   L3-Idx    SVTEP-Mode    ELP-SVTEP-IP
<default>                 0   192.168.1.2      lo0.0    0
    L2-RTT                   Bridge Domain              VNID     Translation-VNID    MC-Group-IP    Interface
    VLAN-AWARE_FABRIC-EVI    BD_100+100                 5100                         0.0.0.0             vtep.32768
```
```
root@SPINE2> show l2-learning vxlan-tunnel-end-point remote
Logical System Name       Id  SVTEP-IP         IFL   L3-Idx    SVTEP-Mode    ELP-SVTEP-IP
<default>                 0   192.168.1.2      lo0.0    0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 192.168.1.3      VLAN-AWARE_FABRIC-EVI    347       vtep.32771   594     RNVE
    VNID          MC-Group-IP
    5100          0.0.0.0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 192.168.1.4      VLAN-AWARE_FABRIC-EVI    346       vtep.32770   593     RNVE
    VNID          MC-Group-IP
    5100          0.0.0.0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 192.168.1.5      VLAN-AWARE_FABRIC-EVI    337       vtep.32769   592     RNVE
    VNID          MC-Group-IP
    5100          0.0.0.0
```
- **View neighbors**
  - Since Spines do not advertise anything yet - the are not in any list of neighbors on either Leaves or Spines
```
root@SPINE2> show evpn instance VLAN-AWARE_FABRIC-EVI
                            Intfs       IRB intfs         MH      MAC addresses
Instance                    Total   Up  Total   Up  Nbrs  ESIs    Local  Remote
VLAN-AWARE_FABRIC-EVI           1    1      0    0     3     1        0       5

```
```
root@SPINE2> show evpn instance VLAN-AWARE_FABRIC-EVI extensive
Instance: VLAN-AWARE_FABRIC-EVI
  Route Distinguisher: 192.168.1.2:8
  Encapsulation type: VXLAN
  Duplicate MAC detection threshold: 5
  Duplicate MAC detection window: 180
  MAC database status                     Local  Remote
    MAC advertisements:                       0       5
    MAC+IP advertisements:                    0       2
    Default gateway MAC advertisements:       0       0
  Number of local interfaces: 1 (1 up)
    Interface name  ESI                            Mode             Status     AC-Role
    .local..8       00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
  Number of IRB interfaces: 0 (0 up)
  Number of protect interfaces: 0
  Number of bridge domains: 1
    VLAN  Domain-ID Intfs/up   IRB-intf  Mode            MAC-sync v4-SG-sync v6-SG-sync
    100   5100         0  0              Extended        Enabled  Disabled   Disabled
  Number of neighbors: 3
    Address               MAC    MAC+IP        AD        IM        ES Leaf-label DCI-Peer Flow-label DT2U-SID           DT2M-SID
    192.168.1.3             3         1         0         1         0                           NO
    192.168.1.4             1         1         2         1         0                           NO
    192.168.1.5             1         0         2         1         0                           NO
  Number of ethernet segments: 1
    ESI: 00:00:00:00:00:00:00:00:00:11
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.5      5100       0               all-active
        192.168.1.4      5100       0               all-active
  Router-ID: 192.168.1.2
  Source VTEP interface IP: 192.168.1.2
  SMET Forwarding: Disabled
  RIB Table-ID: 184549385, Kernel Table-ID: 8, Kernel Table-Generation: 3
  EVPN instance flags: 0x100000014800
  RTT Update Timestamp: Aug 25 11:41:53.629 2026
  L2ALD state change Timestamp: Aug 25 11:41:53.544 2026
  Core-Isolation change TS: Aug 25 11:42:03.870 2026, Core-Isolated: N
  Last Core-Isolation Change Reason: evpn-peer-transition
```
```
root@LEAF4> show ethernet-switching vxlan-tunnel-end-point remote
Logical System Name       Id  SVTEP-IP         IFL   L3-Idx    SVTEP-Mode    ELP-SVTEP-IP
<default>                 0   192.168.1.4      lo0.0    0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 192.168.1.3      default-switch           355       vtep.32770   599     RNVE
    VNID          MC-Group-IP
    5100          0.0.0.0
 RVTEP-IP         L2-RTT                   IFL-Idx   Interface    NH-Id   RVTEP-Mode  ELP-IP        Flags
 192.168.1.5      default-switch           354       vtep.32769   597     RNVE
    VNID          MC-Group-IP
    5100          0.0.0.0
```
- **View MAC addresses on Spines:**
```
root@SPINE2> show l2-learning vxlan-tunnel-end-point remote mac-table
MAC flags (S -static MAC, D -dynamic MAC, L -locally learned, C -Control MAC
           SE -Statistics enabled, NM -Non configured MAC, R -Remote PE MAC, P -Pinned MAC)

Logical system   : <default>
Routing instance : VLAN-AWARE_FABRIC-EVI
 Bridging domain : BD_100+100, VLAN : 100, VNID : 5100
   MAC                 MAC      Logical          Remote VTEP
   address             flags    interface        IP address
   aa:bb:cc:80:90:00   DR       esi.595          192.168.1.5
   aa:bb:cc:80:80:00   DR       vtep.32770       192.168.1.4
   aa:bb:cc:00:60:00   DR       vtep.32771       192.168.1.3
   aa:bb:cc:80:60:00   DR       vtep.32771       192.168.1.3
   aa:bb:cc:80:70:00   DR       vtep.32771       192.168.1.3
```

### Autocreated policies
- **4 policies related to the created RoutingInstance:**
```
root@SPINE2> show policy
Configured policies:
LOAD-BALANCE
LOOPBACK-TO-BGP
__evpn-export-VLAN-AWARE_FABRIC-EVI-bd-override-5100-internal__
__evpn-import-autoderive-VLAN-AWARE_FABRIC-EVI-internal__
__vrf-export-VLAN-AWARE_FABRIC-EVI-internal__
__vrf-import-VLAN-AWARE_FABRIC-EVI-internal__
__vrf-import-__default_evpn__-internal__
```
- **__vrf-import-VRFNAME-internal__ **
  - **Accepts routes with RT of this RoutingInstance **
```
root@SPINE2> show policy __vrf-import-VLAN-AWARE_FABRIC-EVI-internal__
Policy __vrf-import-VLAN-AWARE_FABRIC-EVI-internal__:  [CHANGED/RESOLVED/]
    Term unnamed:
        from community __vrf-community-VLAN-AWARE_FABRIC-EVI-common-internal__ [target:65500:1 ]
        then accept
    Term unnamed:
        then reject
```

- **__vrf-export-VRFNAME-internal__**
  - Marks announced routes with RT of this RoutingInstance
```
root@SPINE2> show policy __vrf-export-VLAN-AWARE_FABRIC-EVI-internal__
Policy __vrf-export-VLAN-AWARE_FABRIC-EVI-internal__:  [CHANGED/RESOLVED/]
    Term unnamed:
        then community + __vrf-community-VLAN-AWARE_FABRIC-EVI-common-internal__ [target:65500:1 ] accept
```
- **__evpn-import-autoderive-VRFNAME-internal__**
  - **Accepts routes with RT of this RoutingInstance**
  - **Accepts routes with RT of this VNI**
```
root@SPINE2> show policy __evpn-import-autoderive-VLAN-AWARE_FABRIC-EVI-internal__
Policy __evpn-import-autoderive-VLAN-AWARE_FABRIC-EVI-internal__:  [CHANGED/RESOLVED/EVPN_VXLAN_AUTO/]
    Term VLAN-AWARE_FABRIC-EVI-bd-override-5100:
        from community __evpn-community-VLAN-AWARE_FABRIC-EVI-bd-override-5100-export-internal__ [target:65500:5100 ]
        then accept
    Term unnamed:
        from community __vrf-community-VLAN-AWARE_FABRIC-EVI-common-internal__ [target:65500:1 ]
        then accept
    Term unnamed:
        then reject
```
- **__evpn-export-VRFNAME-bd-override-5100-internal__**
  - **Marks announced routes with RT of this VNI**
```
root@SPINE2> show policy __evpn-export-VLAN-AWARE_FABRIC-EVI-bd-override-5100-internal__
Policy __evpn-export-VLAN-AWARE_FABRIC-EVI-bd-override-5100-internal__:  [CHANGED/RESOLVED/EVPN_VXLAN_AUTO/]
    Term unnamed:
        then community + __evpn-community-VLAN-AWARE_FABRIC-EVI-bd-override-5100-export-internal__ [target:65500:5100 ] accept
```
- d
- d

## Virtual GW  (Redundant Layer 3 VXLAN Gateway)
### Configuration
#### SPINE1
```
set interfaces irb.100 fam inet addr 10.200.100.252/24 virtual-gateway-address 10.200.100.254
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 routing-interface irb.100

set interfaces irb.101 fam inet addr 10.200.101.252/24 virtual-gateway-address 10.200.101.254
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
```
#### SPINE2
```
set interfaces irb.100 fam inet addr 10.200.100.253/24 virtual-gateway-address 10.200.100.254
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-100 routing-interface irb.100

set interfaces irb.101 fam inet addr 10.200.101.253/24 virtual-gateway-address 10.200.101.254
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD-101 routing-interface irb.101
```
### Verification
- show evpn instance $EVI_NAME extensive
```
root@SPINE1> show evpn instance VLAN-AWARE_FABRIC-EVI extensive
Instance: VLAN-AWARE_FABRIC-EVI
  Route Distinguisher: 192.168.1.1:8
  Encapsulation type: VXLAN
  Duplicate MAC detection threshold: 5
  Duplicate MAC detection window: 180
  MAC database status                     Local  Remote
    MAC advertisements:                       1       6
    MAC+IP advertisements:                    2       1
    Default gateway MAC advertisements:       2       0
  Number of local interfaces: 1 (1 up)
    Interface name  ESI                            Mode             Status     AC-Role
    .local..8       00:00:00:00:00:00:00:00:00:00  single-homed     Up         Root
  Number of IRB interfaces: 1 (1 up)
    Interface name  VLAN   VNI    Status  L3 context
    irb.100                5100    Up     master
  Number of protect interfaces: 0
  Number of bridge domains: 1
    VLAN  Domain-ID Intfs/up   IRB-intf  Mode            MAC-sync v4-SG-sync v6-SG-sync
    100   5100         0  0    irb.100   Extended        Enabled  Disabled   Disabled
  Number of neighbors: 3
    Address               MAC    MAC+IP        AD        IM        ES Leaf-label DCI-Peer Flow-label DT2U-SID           DT2M-SID
    192.168.1.3             3         0         0         1         0                           NO
    192.168.1.4             2         1         2         1         0                           NO
    192.168.1.5             1         1         2         1         0                           NO
  Number of ethernet segments: 2
    ESI: 00:00:00:00:00:00:00:00:00:11
      Status: Resolved
      State-Bitfield: 0x1
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of remote PEs connected: 2
        Remote-PE        MAC-label  Aliasing-label  Mode
        192.168.1.4      5100       0               all-active
        192.168.1.5      5100       0               all-active
    ESI: 05:00:00:fd:e9:00:00:13:ec:00
      State-Bitfield: 0x43
      ESI Refcount: 1
      ESI Num Macs: 1, ESI Num SGDBs: 0
      Number of Local interfaces: 1
      Local interface: irb.100, Status: Up/Forwarding
  Router-ID: 192.168.1.1
  Source VTEP interface IP: 192.168.1.1
  SMET Forwarding: Disabled
  RIB Table-ID: 184549385, Kernel Table-ID: 8, Kernel Table-Generation: 3
  EVPN instance flags: 0x100001814800
  RTT Update Timestamp: Aug 25 11:39:24.431 2026
  L2ALD state change Timestamp: Aug 25 11:39:24.310 2026
  Core-Isolation change TS: Aug 25 11:39:34.444 2026, Core-Isolated: N
  Last Core-Isolation Change Reason: evpn-peer-transition
```
- **SPINEs start advertising Type2 MAC/IP routes for real and virtual IRB IPs**
  - Virtual-gateway is always bound to the same MAC address - **00:00:5e:00:01 :01**
  - Autogenerated RD: 192.168.1.1:8
```
root@SPINE1> show route advertising-protocol bgp 192.168.1.5 | match "^  2.*"
  2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
  2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
  2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
  2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
  2:192.168.1.1:8::5100::00:00:5e:00:01:01/304 MAC/IP
  2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0/304 MAC/IP
  2:192.168.1.1:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
  2:192.168.1.1:8::5100::2c:6b:f5:3e:e0:f0::10.200.100.252/304 MAC/IP
```
- **SPINE1 BD-100 MAC table:**
```
root@SPINE1> show bridge mac-ip-table
MAC IP flags  (S - Static, K - Kernel,
Routing instance : VLAN-AWARE_FABRIC-EVI
Bridging domain : BD-100
   IP                           MAC                  Flags              GBP    Logical            Active
   address                      address                                 Tag    Interface          source
   10.200.100.254               00:00:5e:00:01:01    S,K                       irb.100
   10.200.100.252               2c:6b:f5:3e:e0:f0    S,K                       irb.100
```
- **SPINE1 ARP table on SPINE1:**
```
root@SPINE1> show arp
MAC Address       Address         Name                      Interface               Flags
aa:bb:cc:80:60:00 10.200.100.1    10.200.100.1              irb.100 [vtep.32771]    permanent remote
aa:bb:cc:80:70:00 10.200.100.2    10.200.100.2              irb.100 [vtep.32771]    permanent remote
aa:bb:cc:80:80:00 10.200.100.3    10.200.100.3              irb.100 [vtep.32769]    permanent remote
aa:bb:cc:80:90:00 10.200.100.4    10.200.100.4              irb.100 [.local..8]     permanent remote
00:00:5e:00:01:01 10.200.100.254  10.200.100.254            irb.100                 permanent published gateway
02:00:00:00:00:10 128.0.0.16      fpc0                      em1.0                   none
50:00:00:03:00:02 172.16.13.1     172.16.13.1               ge-0/0/3.0              none
50:00:00:04:00:02 172.16.14.1     172.16.14.1               ge-0/0/4.0              none
50:00:00:05:00:02 172.16.15.1     172.16.15.1               ge-0/0/5.0              none
```
- **Spine configured with  route-distinguisher-id only:**
  - Sends **Type1 per-ESs** with autogenerated RD **192.168.1.2:0**
  - Sends **Type2 MAC/IPs** with autogenerated RD **192.168.1.2:8**
```
root@SPINE2> show route advertising-protocol bgp 192.168.1.5 | match 192.168.1.2
  1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
  2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
  2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
  2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
  2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
  3:192.168.1.2:8::5100::192.168.1.2/248 IM
  2:192.168.1.2:8::5100::00:00:5e:00:01:01/304 MAC/IP
  2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0/304 MAC/IP
  2:192.168.1.2:8::5100::00:00:5e:00:01:01::10.200.100.254/304 MAC/IP
  2:192.168.1.2:8::5100::2c:6b:f5:b9:da:f0::10.200.100.253/304 MAC/IP
  3:192.168.1.2:8::5100::192.168.1.2/248 IM
  1:192.168.1.2:0::050000fdea000013ec00::FFFF:FFFF/192 AD/ESI
```

