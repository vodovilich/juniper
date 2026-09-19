## assville
```
root@assville> show configuration | display set
set version 24.2R1-S2.5
set system host-name assville
set system root-authentication encrypted-password "$6$qkgiFABC$cw7/.1wXLcFYsri70jZ25YD7Bk0wWcb5FNvJSHXXJ..OUo88llAHbWWMW6J1xK/qd9JyL.vAi3RJDT/ux3DI9/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/0 unit 0 family inet address 192.168.12.11/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 192.168.13.11/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.10.1/24
set interfaces ge-0/0/6 unit 0 family inet address 172.16.21.1/24
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM699CA8F2CE
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM699CA8F2CE
set interfaces lo0 unit 0 family inet address 1.1.1.1/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0001.00
set interfaces lo0 unit 0 family mpls
set policy-options prefix-list DIRECT-TO-BGP 1.1.1.1/32
set policy-options policy-statement A-to-B-POLICY term 1 from route-filter 10.10.10.255/32 exact
set policy-options policy-statement A-to-B-POLICY term 1 then accept
set policy-options policy-statement B-to-A-POLICY term 1 from route-filter 10.20.10.255/32 exact
set policy-options policy-statement B-to-A-POLICY term 1 then accept
set policy-options policy-statement CUST-A_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-A_EXPORT term 01_ACCEPT_BGP then community add CUST-A_RT-FILTER
set policy-options policy-statement CUST-A_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-A_EXPORT term 02_DROP_ANY then reject
set policy-options policy-statement CUST-A_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-A_IMPORT term 01_ACCEPT_BGP from community CUST-A_RT-FILTER
set policy-options policy-statement CUST-A_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-A_IMPORT term 02_DROP_ANY then reject
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP then community add CUST-B_RT-FILTER
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-B_EXPORT term 02_DROP_ANY then reject
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP from community CUST-B_RT-FILTER
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-B_IMPORT term 02_DROP_ANY then reject
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from protocol direct
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from prefix-list DIRECT-TO-BGP
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP then accept
set policy-options policy-statement iBGP-OUT term BGP-ACCEPT from protocol bgp
set policy-options policy-statement iBGP-OUT term BGP-ACCEPT then accept
set policy-options community CUST-A_RT-FILTER members target:65530:1
set policy-options community CUST-B_RT-FILTER members target:65530:2
set routing-instances CUSTOMER-A instance-type vrf
set routing-instances CUSTOMER-A protocols bgp group EXT type external
set routing-instances CUSTOMER-A protocols bgp group EXT advertise-peer-as
set routing-instances CUSTOMER-A protocols bgp group EXT family inet unicast rib-group A-to-B
set routing-instances CUSTOMER-A protocols bgp group EXT neighbor 172.16.10.10 local-address 172.16.10.1
set routing-instances CUSTOMER-A protocols bgp group EXT neighbor 172.16.10.10 family inet unicast
set routing-instances CUSTOMER-A protocols bgp group EXT neighbor 172.16.10.10 peer-as 65601
set routing-instances CUSTOMER-A interface ge-0/0/5.0
set routing-instances CUSTOMER-A route-distinguisher 1.1.1.1:1
set routing-instances CUSTOMER-A vrf-import CUST-A_IMPORT
set routing-instances CUSTOMER-A vrf-export CUST-A_EXPORT
set routing-instances CUSTOMER-B instance-type vrf
set routing-instances CUSTOMER-B protocols bgp group EXT type external
set routing-instances CUSTOMER-B protocols bgp group EXT advertise-peer-as
set routing-instances CUSTOMER-B protocols bgp group EXT family inet unicast rib-group B-to-A
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.21.10 local-address 172.16.21.1
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.21.10 family inet unicast
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.21.10 peer-as 65602
set routing-instances CUSTOMER-B interface ge-0/0/6.0
set routing-instances CUSTOMER-B route-distinguisher 1.1.1.1:2
set routing-instances CUSTOMER-B vrf-import CUST-B_IMPORT
set routing-instances CUSTOMER-B vrf-export CUST-B_EXPORT
set routing-options router-id 1.1.1.1
set routing-options autonomous-system 65530
set routing-options rib-groups A-to-B import-rib CUSTOMER-A.inet.0
set routing-options rib-groups A-to-B import-rib CUSTOMER-B.inet.0
set routing-options rib-groups A-to-B import-policy A-to-B-POLICY
set routing-options rib-groups B-to-A import-rib CUSTOMER-B.inet.0
set routing-options rib-groups B-to-A import-rib CUSTOMER-A.inet.0
set routing-options rib-groups B-to-A import-policy B-to-A-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INT type internal
set protocols bgp group INT local-address 1.1.1.1
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT family route-target
set protocols bgp group INT export iBGP-OUT
set protocols bgp group INT neighbor 3.3.3.3
set protocols bgp group INT neighbor 5.5.5.5
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/1.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface lo0.0
```

## ballsackcity
```
root@ballsackcity> show configuration | display set
set version 24.2R1-S2.5
set system host-name ballsackcity
set system root-authentication encrypted-password "$6$RpQoNhpc$i6rcTf41/DvvIy2IwqIbKnLympl0wUbjNfpM9dnR8hvrIdDhUWU5gvaIrR8plT7iQHFkroNCxyZqeh/kNTSPS."
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/0 unit 0 family inet address 192.168.12.22/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 192.168.24.22/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/2 unit 0 family inet address 192.168.23.22/24
set interfaces ge-0/0/2 unit 0 family iso
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM699CA906E9
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM699CA906E9
set interfaces lo0 unit 0 family inet address 2.2.2.2/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0002.00
set interfaces lo0 unit 0 family mpls
set policy-options prefix-list DIRECT-TO-BGP 2.2.2.2/32
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from protocol direct
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from prefix-list DIRECT-TO-BGP
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP then accept
set policy-options policy-statement iBGP-OUT term ACCEPT-BGP from protocol bgp
set policy-options policy-statement iBGP-OUT term ACCEPT-BGP then accept
set routing-options router-id 2.2.2.2
set routing-options autonomous-system 65530
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INT type internal
set protocols bgp group INT local-address 2.2.2.2
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT family route-target
set protocols bgp group INT export iBGP-OUT
set protocols bgp group INT neighbor 3.3.3.3
set protocols bgp group INT neighbor 5.5.5.5
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/1.0
set protocols isis interface ge-0/0/2.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface lo0.0

```

## cumshottown_rr
```
root@cumshottown_rr> show configuration | display set
set version 24.2R1-S2.5
set system host-name cumshottown_rr
set system root-authentication encrypted-password "$6$xSDalggH$lDqvxiuLYtwP.nRgYAQ0ObNn8eb7Kye1rSJFysxSBG2oBNKJCqDKcc/6vRbny/IpYn79ae4fgugLBGGgMtIS8/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/0 unit 0 family inet address 192.168.35.33/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 192.168.13.33/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/2 unit 0 family inet address 192.168.23.33/24
set interfaces ge-0/0/2 unit 0 family iso
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.23.1/24
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM699CA90D99
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM699CA90D99
set interfaces lo0 unit 0 family inet address 3.3.3.3/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0003.00
set interfaces lo0 unit 0 family mpls
set policy-options prefix-list DIRECT-TO-BGP 3.3.3.3/32
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP then community add CUST-B_RT-FILTER
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-B_EXPORT term 02_DROP_ANY then reject
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP from community CUST-B_RT-FILTER
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-B_IMPORT term 02_DROP_ANY then reject
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from protocol direct
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from prefix-list DIRECT-TO-BGP
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP then accept
set policy-options policy-statement iBGP-OUT term BGP-ACCEPT from protocol bgp
set policy-options policy-statement iBGP-OUT term BGP-ACCEPT then accept
set policy-options community CUST-B_RT-FILTER members target:65530:2
set routing-instances CUSTOMER-B instance-type vrf
set routing-instances CUSTOMER-B protocols bgp group EXT type external
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.23.10 local-address 172.16.23.1
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.23.10 advertise-peer-as
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.23.10 family inet unicast
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.23.10 peer-as 65602
set routing-instances CUSTOMER-B interface ge-0/0/5.0
set routing-instances CUSTOMER-B route-distinguisher 3.3.3.3:2
set routing-instances CUSTOMER-B vrf-import CUST-B_IMPORT
set routing-instances CUSTOMER-B vrf-export CUST-B_EXPORT
set routing-options router-id 3.3.3.3
set routing-options autonomous-system 65530
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INT type internal
set protocols bgp group INT local-address 3.3.3.3
set protocols bgp group INT advertise-inactive
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT family route-target
set protocols bgp group INT export iBGP-OUT
set protocols bgp group INT cluster 3.3.3.3
set protocols bgp group INT neighbor 1.1.1.1
set protocols bgp group INT neighbor 2.2.2.2
set protocols bgp group INT neighbor 4.4.4.4
set protocols bgp group INT neighbor 5.5.5.5
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/1.0
set protocols isis interface ge-0/0/2.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface lo0.0

```

## dickville
```
root@dickville> show configuration | display set
set version 24.2R1-S2.5
set system host-name dickville
set system root-authentication encrypted-password "$6$Jrg3VtC3$g0pdh3Co9LmGe2pZZe7CuSWzX5JnTqcFewNmHMatsKQyl45OppvOY/mxrHFVlAKVY5yFS0Pbv2uxceGTagQns/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 192.168.24.44/24
set interfaces ge-0/0/1 unit 0 family iso
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/2 unit 0 family inet address 192.168.45.44/24
set interfaces ge-0/0/2 unit 0 family iso
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.22.1/24
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM699CA917B9
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM699CA917B9
set interfaces lo0 unit 0 family inet address 4.4.4.4/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0004.00
set interfaces lo0 unit 0 family mpls
set policy-options prefix-list DIRECT-TO-BGP 4.4.4.4/32
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP then community add CUST-B_RT-FILTER
set policy-options policy-statement CUST-B_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-B_EXPORT term 02_DROP_ANY then reject
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP from community CUST-B_RT-FILTER
set policy-options policy-statement CUST-B_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-B_IMPORT term 02_DROP_ANY then reject
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from protocol direct
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from prefix-list DIRECT-TO-BGP
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP then accept
set policy-options policy-statement iBGP-OUT term ACCEPT-BGP from protocol bgp
set policy-options policy-statement iBGP-OUT term ACCEPT-BGP then accept
set policy-options community CUST-B_RT-FILTER members target:65530:2
set routing-instances CUSTOMER-B instance-type vrf
set routing-instances CUSTOMER-B protocols bgp group EXT type external
set routing-instances CUSTOMER-B protocols bgp group EXT advertise-peer-as
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.22.10 local-address 172.16.22.1
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.22.10 family inet unicast
set routing-instances CUSTOMER-B protocols bgp group EXT neighbor 172.16.22.10 peer-as 65602
set routing-instances CUSTOMER-B interface ge-0/0/5.0
set routing-instances CUSTOMER-B route-distinguisher 4.4.4.4:2
set routing-instances CUSTOMER-B vrf-import CUST-B_IMPORT
set routing-instances CUSTOMER-B vrf-export CUST-B_EXPORT
set routing-options router-id 4.4.4.4
set routing-options autonomous-system 65530
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INT type internal
set protocols bgp group INT local-address 4.4.4.4
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT family route-target
set protocols bgp group INT export iBGP-OUT
set protocols bgp group INT neighbor 3.3.3.3
set protocols bgp group INT neighbor 5.5.5.5
set protocols isis interface ge-0/0/1.0
set protocols isis interface ge-0/0/2.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface lo0.0

```

## ejaculaburg_rr
```
root@ejaculaburg_rr> show configuration |display set
set version 24.2R1-S2.5
set system host-name ejaculaburg_rr
set system root-authentication encrypted-password "$6$xoCNydsH$EdthvNihaZFOb5j/3T805HF7lFdCGkqRQk2YjwQwRNpxthGseaXoGUV2yXb6puZpNpRnZJKBNEp2CFTyD30/o/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/0 unit 0 family inet address 192.168.35.55/24
set interfaces ge-0/0/0 unit 0 family iso
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/2 unit 0 family inet address 192.168.45.55/24
set interfaces ge-0/0/2 unit 0 family iso
set interfaces ge-0/0/2 unit 0 family mpls
set interfaces ge-0/0/3 unit 0 family inet address 192.168.15.55/24
set interfaces ge-0/0/3 unit 0 family iso
set interfaces ge-0/0/3 unit 0 family mpls
set interfaces ge-0/0/5 unit 0 family inet address 172.16.11.1/24
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM699CA91931
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM699CA91931
set interfaces lo0 unit 0 family inet address 5.5.5.5/32
set interfaces lo0 unit 0 family iso address 49.0000.0000.0000.0005.00
set interfaces lo0 unit 0 family mpls
set policy-options prefix-list DIRECT-TO-BGP 5.5.5.5/32
set policy-options policy-statement CUST-A_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-A_EXPORT term 01_ACCEPT_BGP then community add CUST-A_RT-FILTER
set policy-options policy-statement CUST-A_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-A_EXPORT term 02_DROP-ANY then reject
set policy-options policy-statement CUST-A_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement CUST-A_IMPORT term 01_ACCEPT_BGP from community CUST-A_RT-FILTER
set policy-options policy-statement CUST-A_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement CUST-A_IMPORT term 02_DROP_ANY then reject
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from protocol direct
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP from prefix-list DIRECT-TO-BGP
set policy-options policy-statement iBGP-OUT term DIRECT-TO-BGP then accept
set policy-options policy-statement iBGP-OUT term ACCEPT-BGP from protocol bgp
set policy-options policy-statement iBGP-OUT term ACCEPT-BGP then accept
set policy-options community CUST-A_RT-FILTER members target:65530:1
set routing-instances CUSTOMER-A instance-type vrf
set routing-instances CUSTOMER-A protocols bgp group EXT type external
set routing-instances CUSTOMER-A protocols bgp group EXT advertise-peer-as
set routing-instances CUSTOMER-A protocols bgp group EXT neighbor 172.16.11.10 local-address 172.16.11.1
set routing-instances CUSTOMER-A protocols bgp group EXT neighbor 172.16.11.10 family inet unicast
set routing-instances CUSTOMER-A protocols bgp group EXT neighbor 172.16.11.10 peer-as 65601
set routing-instances CUSTOMER-A interface ge-0/0/5.0
set routing-instances CUSTOMER-A route-distinguisher 5.5.5.5:1
set routing-instances CUSTOMER-A vrf-import CUST-A_IMPORT
set routing-instances CUSTOMER-A vrf-export CUST-A_EXPORT
set routing-instances CUSTOMER-A vrf-table-label
set routing-options router-id 5.5.5.5
set routing-options autonomous-system 65530
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group INT type internal
set protocols bgp group INT local-address 5.5.5.5
set protocols bgp group INT advertise-inactive
set protocols bgp group INT family inet unicast
set protocols bgp group INT family inet-vpn unicast
set protocols bgp group INT family route-target
set protocols bgp group INT export iBGP-OUT
set protocols bgp group INT cluster 5.5.5.5
set protocols bgp group INT neighbor 1.1.1.1
set protocols bgp group INT neighbor 2.2.2.2
set protocols bgp group INT neighbor 3.3.3.3
set protocols bgp group INT neighbor 4.4.4.4
set protocols isis interface ge-0/0/0.0
set protocols isis interface ge-0/0/2.0
set protocols isis interface ge-0/0/3.0
set protocols isis interface lo0.0
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/2.0
set protocols ldp interface ge-0/0/3.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/0.0
set protocols mpls interface ge-0/0/2.0
set protocols mpls interface lo0.0
set protocols mpls interface ge-0/0/3.0

```

## CE_A-1
```
hostname CE_A-1
interface Loopback0
 ip address 10.10.10.255 255.255.255.255
!
interface Ethernet0/0
 ip address 172.16.10.10 255.255.255.0
!
router bgp 65601
 bgp log-neighbor-changes
 network 10.10.10.255 mask 255.255.255.255
 redistribute connected
 neighbor 172.16.10.1 remote-as 65530
 neighbor 172.16.10.1 allowas-in
!
no ip http server
no ip http secure-server
ip route 10.10.10.255 255.255.255.255 Null0 name BLACKHOLE
```

## CE_A-2
```
hostname CE_A-2
!
interface Loopback0
 ip address 10.10.20.255 255.255.255.255
!
interface Loopback20
 ip address 10.20.20.255 255.255.255.255
!
interface Ethernet0/0
 ip address 172.16.11.10 255.255.255.0
!
router bgp 65601
 bgp log-neighbor-changes
 network 10.10.20.0 mask 255.255.255.0
 network 10.20.20.0 mask 255.255.255.0
 neighbor 172.16.11.1 remote-as 65530
 neighbor 172.16.11.1 allowas-in
!
ip route 10.10.20.0 255.255.255.0 Null0 name BLACKHOLE
ip route 10.20.20.0 255.255.255.0 Null0 name BLACKHOLE_OVERLAPPING
```

## CE_B-1
```
hostname CE-B_1
!
interface Loopback0
 ip address 10.20.10.255 255.255.255.255
!
interface Ethernet0/0
 ip address 172.16.21.10 255.255.255.0
!
router bgp 65602
 bgp log-neighbor-changes
 network 10.20.10.0 mask 255.255.255.0
 neighbor 172.16.21.1 remote-as 65530
 neighbor 172.16.21.1 allowas-in
!
ip route 10.20.10.0 255.255.255.0 Null0 name BLACKHOLE
```

## CE_B-2
```
hostname CE-B_2
!
interface Loopback0
 ip address 10.20.20.255 255.255.255.255
!
interface Ethernet0/0
 ip address 172.16.22.10 255.255.255.0
!
router bgp 65602
 bgp log-neighbor-changes
 network 10.20.20.0 mask 255.255.255.0
 neighbor 172.16.22.1 remote-as 65530
 neighbor 172.16.22.1 allowas-in
!
ip route 10.20.20.0 255.255.255.0 Null0 name BLACKHOLE
```

## CE_B-3
```
hostname CE-B_3
!
interface Loopback0
 ip address 10.20.30.255 255.255.255.255
!
interface Ethernet0/0
 ip address 172.16.23.10 255.255.255.0
!
router bgp 65602
 bgp log-neighbor-changes
 network 10.20.30.0 mask 255.255.255.0
 neighbor 172.16.23.1 remote-as 65530
 neighbor 172.16.23.1 allowas-in
!
ip forward-protocol nd
!
!
no ip http server
no ip http secure-server
ip route 10.20.30.0 255.255.255.0 Null0 name BLACKHOLE

```

