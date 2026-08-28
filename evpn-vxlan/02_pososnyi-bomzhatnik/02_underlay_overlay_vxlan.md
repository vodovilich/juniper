- UNDERLAY: EBGP
- OVERLAY: IBGP
  - No RRs => Full Mesh
- 2 Spines, 3 Leaves
- 1 EVI: VLAN-AWARE on Spines
  - RoutingInstanse FABRIC on Spines = GRT on Leaves
- 2 vlans/2 VNIs:
  - vlan100-vni5100
  - vlan101-vni5101
  - FABRIC imports both VNIs NLRIs via VNI communities   
- 4 Servers:
  - S6,S7,S8 - single-homed
  - S9 - dual-homed 
- L3 GW: Virtual Gateway (Redundant L3 VXLAN Gateway)




# UNDERLAY - EBGP


# OVERLAY - IBGP


# ENABLE VXLAN


# GlobalParams


# GlobalParams
