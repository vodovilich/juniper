## VLAN-Aware EVPN on COREs
- Only import the VXLAN segment on LEAF3, LEAF4
#### LEAF3, LEAF4
```
set protocols evpn vni-options vni 5240 vrf-target export target:65500:5240

set policy-options community RT-VNI-5240 members target:65500:5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 from community RT-VNI-5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 then accept
set switch-options vrf-import FABRIC-IMPORT
```

#### Both COREs
```
set policy-options community RT-FABRIC members target:65500:1
set policy-options policy-statement FABRIC-IMPORT term IMPORT-GLOBAL-RT from community RT-FABRIC
set policy-options policy-statement FABRIC-IMPORT term IMPORT-GLOBAL-RT then accept
!
set policy-options community RT-VNI-5240 members target:65500:5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 from community RT-VNI-5240
set policy-options policy-statement FABRIC-IMPORT term IMPORT-5240 then accept
!
set routing-instances VLAN-AWARE_FABRIC-EVI vtep-source-interface lo0.0
set routing-instances VLAN-AWARE_FABRIC-EVI instance-type virtual-switch
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-import FABRIC-IMPORT
set routing-instances VLAN-AWARE_FABRIC-EVI vrf-target target:65500:5240
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn encapsulation vxlan
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn extended-vni-list all
set routing-instances VLAN-AWARE_FABRIC-EVI protocols evpn multicast-mode ingress-replication
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 vlan-id 240
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 routing-interface irb.240
set routing-instances VLAN-AWARE_FABRIC-EVI bridge-domains BD_240 vxlan vni 5240
```

## L3 VXLAN Virtual GW on COREs - VNI 240
#### CORE6
```
set int irb.240 fam inet addr 10.200.240.252/24 virtual-gateway-address 10.200.240.254
```
#### CORE7
```
set int irb.240 fam inet addr 10.200.240.253/24 virtual-gateway-address 10.200.240.254
```

#### Verification
- MACs on LEAF3
```
root@LEAF3> show ethernet-switching table vlan-id 240

MAC flags (S - static MAC, D - dynamic MAC, L - locally learned, P - Persistent static, C - Control MAC
           SE - statistics enabled, NM - non configured MAC, R - remote PE MAC, O - ovsdb MAC,
           B - Blocked MAC)


Ethernet switching table : 4 entries, 4 learned
Routing instance : default-switch
   Vlan                MAC                 MAC       GBP    Logical                SVLBNH/      Active
   name                address             flags     tag    interface              VENH Index   source
   VLAN_240            00:00:5e:00:01:01   DRP              esi.764                             05:00:00:fe:4c:00:00:14:78:00
   VLAN_240            2c:6b:f5:01:09:f0   DR               vtep.32771                          192.168.1.7
   VLAN_240            2c:6b:f5:65:cc:c0   DL               ae0.0
   VLAN_240            2c:6b:f5:ba:26:f0   DR               vtep.32772                          192.168.1.6
```

- ARPs on COREs
```
root@CORE6> show arp interface irb.240
MAC Address       Address         Name                      Interface               Flags
2c:6b:f5:65:cc:c0 10.200.240.1    10.200.240.1              irb.240 [.local..8]     permanent remote
2c:6b:f5:01:09:f0 10.200.240.253  10.200.240.253            irb.240 [vtep.32769]    permanent remote
00:00:5e:00:01:01 10.200.240.254  10.200.240.254            irb.240                 permanent published gateway


root@CORE7> show arp interface irb.240
MAC Address       Address         Name                      Interface               Flags
2c:6b:f5:65:cc:c0 10.200.240.1    10.200.240.1              irb.240 [.local..8]     permanent remote
2c:6b:f5:ba:26:f0 10.200.240.252  10.200.240.252            irb.240 [vtep.32771]    permanent remote
00:00:5e:00:01:01 10.200.240.254  10.200.240.254            irb.240                 permanent published gateway
```

