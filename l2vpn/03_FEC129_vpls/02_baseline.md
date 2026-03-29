# FEC129 VPWS
- **BGP autodiscovers PEs**
- **tLDP signals the VPN Labels**
- **SourceIDs are used to identify LSRs**
- Interfaces **encapsulation: vlan-ccc**
- **RoutingInstance config includes:**
  - **Instance-type: l2vpn**
  - **l2vpn-id community in the format of: l2vpn-id:65530:1**
  - **protocols l2vpn > site > [ [interface, targetID], sourceID ]**
- **BGP config includes: family auto-discovery-only**
- **PE1 Customer1.l2vpn.0 and ldp.l2vpn.0 tables:**
<img width="763" height="482" alt="image" src="https://github.com/user-attachments/assets/d89624a1-45eb-4f66-b799-1335a871fc84" />
<img width="707" height="160" alt="image" src="https://github.com/user-attachments/assets/7c154033-1834-4331-a0e9-e14e9b8d38c8" />

- **BGP communities include:**
  - **RT**
  - **L2VPN-ID**
<img width="723" height="770" alt="image" src="https://github.com/user-attachments/assets/ab64ee9e-9570-4981-a150-27fb8ee9a3df" />

- **BGP NLRI includes:**
  - **RD**
  - **PE Addr (identifies Sites)**
- **NLRI from PE2 (Site2, Site4):**
<img width="642" height="717" alt="image" src="https://github.com/user-attachments/assets/59790fab-06ac-42f1-8f92-ce5eeab70890" />

- **NLRI from PE1 (Site1, Site3):**
<img width="715" height="802" alt="image" src="https://github.com/user-attachments/assets/10acc65f-f0c4-4bfd-ae5e-11d61193c48b" />

- **Service labels are signalled via tLDP**
- **Site1-Site2 ServiceLabel is 300192:**
<img width="897" height="245" alt="image" src="https://github.com/user-attachments/assets/5bd0407f-7181-449f-b95b-76486d22b637" />

- **FEC129-VPWS LMM (e.g. from PE2_site2 with 300192):**
  - **FEC type: Generalized PWid FEC Element - type 129**
  - **PW interface parameters specify VLANID**
<img width="695" height="955" alt="image" src="https://github.com/user-attachments/assets/70d808e8-664d-431d-8a91-f231255381d9" />

- **Site3-Site4 ServiceLabel is 300176:**
<img width="908" height="247" alt="image" src="https://github.com/user-attachments/assets/21286773-696d-4fea-adc3-adf9f15b0f54" />

- **FEC129-VPWS LMM from PE2_site4 with 300176:**
  - **PW type: ETHERNET TAGGED MODE**

<img width="747" height="1013" alt="image" src="https://github.com/user-attachments/assets/75a03dd1-ea8a-4d94-b760-18448fa3a72f" />




# FEC129 VPLS
- **Better because of no manual NBR definition**
- **Uses 2 NLRIs (Discovery NLRI, Pseudowire NLRI) and IDs to identify themselves (vozmozhno pizdezh?)**
  - Who runs the same RT - can connect
  <img width="587" height="548" alt="image" src="https://github.com/user-attachments/assets/cb86d171-10f0-4eb7-a7e6-6142b5036d09" />

- **PW type: ETHERNET**
<img width="719" height="729" alt="image" src="https://github.com/user-attachments/assets/e76f4329-24dd-40f0-83f9-55ba7b6af623" />

- **Service Labels assigned per-PE:**
  - **Site1 to Site2: 800001:**
<img width="789" height="204" alt="image" src="https://github.com/user-attachments/assets/490356fd-b563-4dee-ba90-918db08fb11f" />

  - **Site3 to Site4: 800001:**
<img width="781" height="202" alt="image" src="https://github.com/user-attachments/assets/4f8e1ac8-169a-4651-a572-6f6c43a58973" />
