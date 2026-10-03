# BALLSACKCITY 
- 2 single-homed servers 
- 1 dual-homed server 
## VLAN-AWARE EVI definition
- **VLAN-AWARE-EVI-RT=65500:65002**
- **L2 services** - three L2-domain:
  - vlan11,12,13
    - vlan11 | No per-L2Domain-RT
    - vlan12 | No per-L2Domain-RT
    - vlan13 | No per-L2Domain-RT
- **L3 services**
  - vlan11 | Virtual GW on IRB.11 - VIP=192.168.2.254 
  - vlan12 | Virtual GW on IRB.12 - VIP=192.168.2.254
  - vlan13 | Anycast (IP+MAC) GW on IRB.13 - 192.168.2.255
- **L3VPN**
  - L3VPN-12 | Interface IRB.12 | RT=65500:12 
  - L3VPN-13 | Interface IRB.13 | RT=65500:13 


#### PE3,PE4
```
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE instance-type virtual-switch
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE vrf-target target:65500:65002
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE protocols evpn extended-vlan-list 11-13
!
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-11 vlan-id 11
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-11 routing-interface irb.11
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-12 vlan-id 12
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-12 routing-interface irb.12
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-13 vlan-id 13
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE bridge-domains BD-13 routing-interface irb.13
!
set routing-instances L3VPN-12 instance-type vrf
set routing-instances L3VPN-12 interface irb.12
set routing-instances L3VPN-12 vrf-target target:65500:12
set routing-instances L3VPN-12 vrf-table-label
!
set routing-instances L3VPN-13 instance-type vrf
set routing-instances L3VPN-13 interface irb.13
set routing-instances L3VPN-13 vrf-target target:65500:13
set routing-instances L3VPN-13 vrf-table-label
```
#### PE3
```
set interfaces irb.11 family inet address 192.168.2.253/24 virtual-gateway-address 192.168.2.254
set interfaces irb.12 family inet address 192.168.2.253/24 virtual-gateway-address 192.168.2.254
set interfaces irb.13 family inet address 192.168.2.254/24
set interfaces irb.13 mac aa:aa:aa:aa:aa:aa
```
#### PE4
```
set interfaces irb.11 family inet address 192.168.2.252/24 virtual-gateway-address 192.168.2.254
set interfaces irb.12 family inet address 192.168.2.252/24 virtual-gateway-address 192.168.2.254
set interfaces irb.13 family inet address 192.168.2.254/24
set interfaces irb.13 mac aa:aa:aa:aa:aa:aa
```

### SINGLE-HOMED customer-facing
#### PE3,PE4
```
set interfaces ge-0/0/8 flexible-vlan-tagging
set interfaces ge-0/0/8 encapsulation flexible-ethernet-services
set interfaces ge-0/0/8.0 family bridge interface-mode trunk
set interfaces ge-0/0/8.0 family bridge vlan-id-list 11-13
!
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE interface ge-0/0/8.0
```
### DUAL-HOMED customer-facing
#### PE3, PE4
```
set interfaces ge-0/0/7 gigether-options 802.3ad ae0
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 unit 0 family bridge interface-mode trunk
set interfaces ae0 unit 0 family bridge vlan-id-list [ 11 12 13 ]
!
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:34
set interfaces ae0 esi 00:02:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
!
set routing-instances BALLSACKCITY-EVPN-VLAN-AWARE interface ae0.0
```


## VLAN-BASED EVI definition
- **VLAN-BASED-EVI-RT=65500:200**
- **L2 services** - one L2-domain:
  - vlan200
- **L3 services**
  - vlan200 |  Virtual GW on IRB.200 - VIP=192.168.200.254 
- **L3VPN**
  - L3VPN-100200 | Interface IRB.200 | RT=65500:100200 
### DUAL-HOMED customer-facing
#### PE3,PE4
```
set interfaces ae0 unit 200 encapsulation vlan-bridge
set interfaces ae0 unit 200 vlan-id 200
!
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED instance-type evpn
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED protocols evpn
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED vlan-id 200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED routing-interface irb.200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED interface ae0.200
set routing-instances BALLSACKCITY-EVPN-VLAN-BASED vrf-target target:65500:100200
!
set routing-instances L3VPN-100200 instance-type vrf
set routing-instances L3VPN-100200 interface irb.200
set routing-instances L3VPN-100200 vrf-target target:65500:100200
set routing-instances L3VPN-100200 vrf-table-label
```
#### PE1
```
set interfaces irb unit 200 family inet address 192.168.200.253/24 virtual-gateway-address 192.168.200.254
```
#### PE2
```
set interfaces irb unit 200 family inet address 192.168.200.252/24 virtual-gateway-address 192.168.200.254
```
