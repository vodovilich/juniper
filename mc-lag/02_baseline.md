
<img width="675" height="855" alt="01_mclag_scheme" src="https://github.com/user-attachments/assets/2aaff67f-2cbc-4f61-a4c8-28a989f22587" />
- Gateways - on Spines
- MC-AE - configured for downstream
  - For upstream - usual LAG
- Backup liveness detection in the lab shows UP even if a remote IP is not configured on the peer, lol

# LEAF ICL - Inter Chassis Link
### LEAF3
```
set vlans DATA100 vlan-id 100
set vlans DATA100 l3-interface irb.100
set switch-options service-id 1 

set chassis aggregated-devices ethernet device-count 5
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp periodic fast
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members DATA100
set interfaces irb unit 100 family inet address 192.168.100.3/24

set protocols iccp local-ip-addr 192.168.100.3
set protocols iccp authentication-key MD5KEY
set protocols iccp peer 192.168.100.4 redundancy-group-id-list 34
set protocols iccp peer 192.168.100.4 liveness-detection minimum-interval 1000
set protocols iccp peer 192.168.100.4 liveness-detection multiplier 3
set protocols iccp peer 192.168.100.4 backup-liveness-detection backup-peer-ip 4.4.4.4
```
### LEAF4
```
set vlans DATA100 vlan-id 100
set vlans DATA100 l3-interface irb.100
set switch-options service-id 1

set chassis aggregated-devices ethernet device-count 5
set interfaces ge-0/0/9 ether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp periodic fast
set interfaces ae0 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae0 unit 0 family ethernet-switching vlan members DATA100
set interfaces irb unit 100 family inet address 192.168.100.4/24

set protocols iccp local-ip-addr 192.168.100.4
set protocols iccp authentication-key MD5KEY
set protocols iccp peer 192.168.100.3 redundancy-group-id-list 34
set protocols iccp peer 192.168.100.3 liveness-detection minimum-interval 1000
set protocols iccp peer 192.168.100.3 liveness-detection multiplier 3
set protocols iccp peer 192.168.100.3 backup-liveness-detection backup-peer-ip 3.3.3.3
```
### Verify
```
root@LEAF3> show iccp

Redundancy Group Information for peer 192.168.100.4
  TCP Connection       : Established
  Liveliness Detection : Up
  Backup liveness peer status: Up
  Redundancy Group ID          Status
    34                          Up

Client Application: l2ald_iccpd_client
  Redundancy Group IDs Joined: 34

Client Application: mclag_cfgchkd
  Redundancy Group IDs Joined: 0 34

Client Application: lacpd
  Redundancy Group IDs Joined: 34
```
# Server-facing MC-AE
- **Three items must match on both chassis:**
  - mc-ae redundancy-group
    - `ae1 agg mc-ae redundancy-group X` must match with one defined at `protocols iccp peer redundancy-group-id-list X`
  - mc-ae mode [ active-active | active-standby ]
  - mc-ae mc-ae-id
    - LabGuide assigns **mc-ae-id per-MC-AE** interface
 
- **Two items must not match on both chassis:**
  - mc-ae chassis-id (0 .. 1)
  - mc-ae status-control [ active | standby ]
- **LACP parameters added:**
  - lacp admin-key 
    - Must match on both chassis
    - LabGuide assigns **same admin-key for multiple MC-AE** interfaces
  - system-id - logical MAC used on both chassis
    - Must match on both chassis
    - LabGuide assigns **system-id per-MC-AE** interface

### LEAF3
```
set vlans CUST10 vlan-id 10
set vlans CUST11 vlan-id 11
set vlans CUST12 vlan-id 12

set interfaces ge-0/0/0 ether-options 802.3ad ae1
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp periodic fast
set interfaces ae1 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae1 unit 0 family ethernet-switching vlan members 10-12

set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:01
set interfaces ae1 aggregated-ether-options lacp admin-key 1
set interfaces ae1 aggregated-ether-options mc-ae mc-ae-id 1
set interfaces ae1 aggregated-ether-options mc-ae redundancy-group 34
set interfaces ae1 aggregated-ether-options mc-ae chassis-id 0
set interfaces ae1 aggregated-ether-options mc-ae mode active-active
set interfaces ae1 aggregated-ether-options mc-ae status-control active

set multi-chassis multi-chassis-protection 192.168.100.4 interface ae0
```
### LEAF4
```
set vlans CUST10 vlan-id 10
set vlans CUST11 vlan-id 11
set vlans CUST12 vlan-id 12

set interfaces ge-0/0/0 ether-options 802.3ad ae1

set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp periodic fast
set interfaces ae1 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae1 unit 0 family ethernet-switching vlan members 10-12

set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:01
set interfaces ae1 aggregated-ether-options lacp admin-key 1
set interfaces ae1 aggregated-ether-options mc-ae mc-ae-id 1
set interfaces ae1 aggregated-ether-options mc-ae redundancy-group 34
set interfaces ae1 aggregated-ether-options mc-ae chassis-id 1
set interfaces ae1 aggregated-ether-options mc-ae mode active-active
set interfaces ae1 aggregated-ether-options mc-ae status-control standby

set multi-chassis multi-chassis-protection 192.168.100.3 interface ae0
```
### Verify
```
root@LEAF3> show interfaces mc-ae
 Member Link                  : ae1
 Current State Machine's State: mcae active state
 Configuration Error Status   : No Error
 Local Status                 : active
 Local State                  : up
 Peer Status                  : active
 Peer State                   : up
     Logical Interface        : ae1.0
     Topology Type            : bridge
     Local State              : up
     Peer State               : up
     Peer Ip/MCP/State        : 192.168.100.4 ae0.0 up
```
# Spine-facing AE (not MC-AE)
### LEAF3/LEAF4
```
set interfaces ge-0/0/1 ether-options 802.3ad ae2
set interfaces ge-0/0/2 ether-options 802.3ad ae2

set interfaces ae2 aggregated-ether-options lacp active
set interfaces ae2 aggregated-ether-options lacp periodic fast
set interfaces ae2 unit 0 family ethernet-switching interface-mode trunk
set interfaces ae2 unit 0 family ethernet-switching vlan members 10-12
```

# Spine ICL
- vMX vs vQFX syntax:
  - Assign physical interfaces to vMX LAG using `gigether-options` rather than `ether-options`
  - Configure the trunk between the vMX routers with the `family bridge` and the `vlan-id-list` instead of  `family ethernet-switching` and `vlan members`
### SPINE1
```
set chassis aggregated-devices ethernet device-count 5
set bridge-domains bd-101 vlan-id 101


set interfaces ge-0/0/8 gigether-options 802.3ad ae0
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp periodic fast
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list 101

set interfaces irb unit 101 family inet address 192.168.101.1/30
set bridge-domains bd-101 routing-interface irb.101

set protocols iccp local-ip-addr 192.168.101.1
set protocols iccp authentication-key MD5KEY
set protocols iccp peer 192.168.101.2 redundancy-group-id-list 12
set protocols iccp peer 192.168.101.2 backup-liveness-detection backup-peer-ip 2.2.2.2
set protocols iccp peer 192.168.101.2 liveness-detection minimum-interval 1000
set protocols iccp peer 192.168.101.2 liveness-detection multiplier 3
set multi-chassis multi-chassis-protection 192.168.101.2 interface ae0
```
### SPINE2
```
set chassis aggregated-devices ethernet device-count 5
set bridge-domains bd-101 vlan-id 101

set interfaces ge-0/0/8 gigether-options 802.3ad ae0
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp periodic fast
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list 101

set interfaces irb unit 101 family inet address 192.168.101.2/30
set bridge-domains bd-101 routing-interface irb.101

set protocols iccp local-ip-addr 192.168.101.2
set protocols iccp authentication-key MD5KEY
set protocols iccp peer 192.168.101.1 redundancy-group-id-list 12
set protocols iccp peer 192.168.101.1 backup-liveness-detection backup-peer-ip 1.1.1.1
set protocols iccp peer 192.168.101.1 liveness-detection minimum-interval 1000
set protocols iccp peer 192.168.101.1 liveness-detection multiplier 3
set multi-chassis multi-chassis-protection 192.168.101.1 interface ae0
```

# Leaf-facing MC-AE
### SPINE1
```
set bridge-domains bd-10 vlan-id 10
set bridge-domains bd-11 vlan-id 11
set bridge-domains bd-12 vlan-id 12
set switch-options service-id 1

set interfaces ge-0/0/3 gigether-options 802.3ad ae2
set interfaces ae2 aggregated-ether-options lacp active
set interfaces ae2 aggregated-ether-options lacp periodic fast
set interfaces ae2 unit 0 family bridge interface-mode trunk
set interfaces ae2 unit 0 family bridge vlan-id-list 10-12

set interfaces ae2 aggregated-ether-options lacp system-id 00:00:00:00:12:03
set interfaces ae2 aggregated-ether-options lacp admin-key 1
set interfaces ae2 aggregated-ether-options mc-ae mc-ae-id 1
set interfaces ae2 aggregated-ether-options mc-ae redundancy-group 12
set interfaces ae2 aggregated-ether-options mc-ae chassis-id 0
set interfaces ae2 aggregated-ether-options mc-ae mode active-active
set interfaces ae2 aggregated-ether-options mc-ae status-control active
```
```
set interfaces ge-0/0/4 gigether-options 802.3ad ae3
set interfaces ae3 aggregated-ether-options lacp active
set interfaces ae3 aggregated-ether-options lacp periodic fast
set interfaces ae3 unit 0 family bridge interface-mode trunk
set interfaces ae3 unit 0 family bridge vlan-id-list 10-12

set interfaces ae3 aggregated-ether-options lacp system-id 00:00:00:00:12:04
set interfaces ae3 aggregated-ether-options lacp admin-key 1
set interfaces ae3 aggregated-ether-options mc-ae mc-ae-id 2
set interfaces ae3 aggregated-ether-options mc-ae redundancy-group 12
set interfaces ae3 aggregated-ether-options mc-ae chassis-id 0
set interfaces ae3 aggregated-ether-options mc-ae mode active-active
set interfaces ae3 aggregated-ether-options mc-ae status-control active
```
### SPINE2
```
set bridge-domains bd-10 vlan-id 10
set bridge-domains bd-11 vlan-id 11
set bridge-domains bd-12 vlan-id 12
set switch-options service-id 1

set interfaces ge-0/0/3 gigether-options 802.3ad ae2
set interfaces ae2 aggregated-ether-options lacp active
set interfaces ae2 aggregated-ether-options lacp periodic fast
set interfaces ae2 unit 0 family bridge interface-mode trunk
set interfaces ae2 unit 0 family bridge vlan-id-list 10-12

set interfaces ae2 aggregated-ether-options lacp system-id 00:00:00:00:12:03
set interfaces ae2 aggregated-ether-options lacp admin-key 1
set interfaces ae2 aggregated-ether-options mc-ae mc-ae-id 1
set interfaces ae2 aggregated-ether-options mc-ae redundancy-group 12
set interfaces ae2 aggregated-ether-options mc-ae chassis-id 1
set interfaces ae2 aggregated-ether-options mc-ae mode active-active
set interfaces ae2 aggregated-ether-options mc-ae status-control standby
```
```
set interfaces ge-0/0/4 gigether-options 802.3ad ae3
set interfaces ae3 aggregated-ether-options lacp active
set interfaces ae3 aggregated-ether-options lacp periodic fast
set interfaces ae3 unit 0 family bridge interface-mode trunk
set interfaces ae3 unit 0 family bridge vlan-id-list 10-12

set interfaces ae3 aggregated-ether-options lacp system-id 00:00:00:00:12:04
set interfaces ae3 aggregated-ether-options lacp admin-key 1
set interfaces ae3 aggregated-ether-options mc-ae mc-ae-id 2
set interfaces ae3 aggregated-ether-options mc-ae redundancy-group 12
set interfaces ae3 aggregated-ether-options mc-ae chassis-id 1
set interfaces ae3 aggregated-ether-options mc-ae mode active-active
set interfaces ae3 aggregated-ether-options mc-ae status-control standby
```

# MC-LAG Gateway

### SPINE1
- Add customer VLANS to ICL:
```
SPINE1# set interfaces ae0 unit 0 family bridge vlan-id-list 10-12
```
- VLANs 10,11: VRRP
  - `accept-data` - enables Master router to accept packets destined to the virtual router
```
set int irb unit 10 fam inet address 192.168.10.11/24 vrrp-group 10 virtual-address 192.168.10.1
set int irb unit 10 fam inet address 192.168.10.11/24 vrrp-group 10 priority 150
set int irb unit 10 fam inet address 192.168.10.11/24 vrrp-group 10 accept-data
set int irb unit 10 fam inet address 192.168.10.11/24 vrrp-group 10 authentication-type md5
set int irb unit 10 fam inet address 192.168.10.11/24 vrrp-group 10 authentication-key MD5KEY
set bridge-domains bd-10 routing-interface irb.10

set int irb unit 11 fam inet address 192.168.11.11/24 vrrp-group 11 virtual-address 192.168.11.1
set int irb unit 11 fam inet address 192.168.11.11/24 vrrp-group 11 accept-data
set int irb unit 11 fam inet address 192.168.11.11/24 vrrp-group 11 authentication-type md5
set int irb unit 11 fam inet address 192.168.11.11/24 vrrp-group 11 authentication-key MD5KEY
set bridge-domains bd-11 routing-interface irb.11
```
- VLANs 12: anycast GW:
```
set interfaces irb unit 12 family inet address 192.168.12.1/24
set interfaces irb unit 12 mac 00:00:00:00:00:12
set bridge-domains bd-12 routing-interface irb.12
```
### SPINE2
```
set interfaces ae0 unit 0 family bridge vlan-id-list 10-12

set int irb unit 10 fam inet address 192.168.10.22/24 vrrp-group 10 virtual-address 192.168.10.1
set int irb unit 10 fam inet address 192.168.10.22/24 vrrp-group 10 accept-data
set int irb unit 10 fam inet address 192.168.10.22/24 vrrp-group 10 authentication-type md5
set int irb unit 10 fam inet address 192.168.10.22/24 vrrp-group 10 authentication-key MD5KEY
set bridge-domains bd-10 routing-interface irb.10

set int irb unit 11 fam inet address 192.168.11.22/24 vrrp-group 11 virtual-address 192.168.11.1
set int irb unit 11 fam inet address 192.168.11.22/24 vrrp-group 11 priority 150
set int irb unit 11 fam inet address 192.168.11.22/24 vrrp-group 11 accept-data
set int irb unit 11 fam inet address 192.168.11.22/24 vrrp-group 11 authentication-type md5
set int irb unit 11 fam inet address 192.168.11.22/24 vrrp-group 11 authentication-key MD5KEY
set bridge-domains bd-11 routing-interface irb.11

set interfaces irb unit 12 family inet address 192.168.12.1/24
set interfaces irb unit 12 mac 00:00:00:00:00:12
set bridge-domains bd-12 routing-interface irb.12
```
