## BGP Configuration
- Enable BGP full-mesh between PEs
- Authenticate all BGP sessions using the password 'BGPSECRET'
- The BGP session should allow for the exchange of MPLS L3 VPN addresses only.
- Use autonomous system 65500

#### All PEs
```
set routing-options autonomous-system 65500
set protocols bgp group IBGP-CORE type internal
set protocols bgp group IBGP-CORE family inet-vpn unicast
set protocols bgp group IBGP-CORE authentication-key BGPSECRET
```
#### PE1
```
set protocols bgp group IBGP-CORE local-address 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### PE2
```
set protocols bgp group IBGP-CORE local-address 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### PE3
```
set protocols bgp group IBGP-CORE local-address 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### PE4
```
set protocols bgp group IBGP-CORE local-address 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### P5
```
set protocols bgp group IBGP-CORE local-address 192.168.1.5
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.6
```
#### P6
``` 
set protocols bgp group IBGP-CORE local-address 192.168.1.6
set protocols bgp group IBGP-CORE neighbor 192.168.1.1
set protocols bgp group IBGP-CORE neighbor 192.168.1.2
set protocols bgp group IBGP-CORE neighbor 192.168.1.3
set protocols bgp group IBGP-CORE neighbor 192.168.1.4
set protocols bgp group IBGP-CORE neighbor 192.168.1.5
```
