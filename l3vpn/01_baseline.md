## LDP (Transport) Label Signaling
- **Hello**
  - UDP from int_ip to mcst-224.0.0.2
  - Contains Loopback IP in TransportAddress field
- **Initialization**
  - TCP loopback_to_loopback
  - Label Advertise e.g. DownstreamUnsolicited 
  - LoopDetection e.g. disabled
- **Keepalive**
  - TCP loopback_to_loopback
- **Address Message**
  - TCP loopback_to_loopback
  - List of IPs on the sender_LSR
- **Label Mapping Message**
  - LSRs signal ImplicitNull 3 Labels for FEC equals to their loopbacks
  - LSR_B adds routing record for FEC=LSR_A with no label (because of PHP)
  - LSR_B generates a new label for FEC=LSR_A 
  - LSR_B sends LMM with the new label to its NBRs
    - Including LSR_A

```
49320 is decimal  299808
49340 is decimal  299840
49350 is decimal  299856
49340 is decimal  299840
49350 is decimal  299856
49360 is decimal  299872
49380 is decimal  299904
493a0 is decimal  299936
493b0 is decimal  299952
49380 is decimal  299904
49350 is decimal  299856
49360 is decimal  299872
```
<img width="663" height="203" alt="image" src="https://github.com/user-attachments/assets/b8ede3ee-8f39-4e6c-bcaf-8b9f7908df85" />
<img width="721" height="70" alt="image" src="https://github.com/user-attachments/assets/e586cad8-ef42-4c94-864f-168b704a033e" />
<img width="1539" height="1166" alt="image" src="https://github.com/user-attachments/assets/91a472b0-0bf7-43e3-87eb-f44db60c2f2c" />




## MP-BGP (Service) label signaling
- **Capabilities for MP-BGP exchanged in OPEN messages:**
<img width="457" height="665" alt="image" src="https://github.com/user-attachments/assets/45b80ed9-522e-438a-a262-8a875fbee0a2" />
<br>
<br>

- **RTs are transferred via ExtCommunities**
<img width="1260" height="524" alt="image" src="https://github.com/user-attachments/assets/836bf1cd-73dd-4653-bf5b-c09724fe7a6c" />
<br>
<br>

- **CE sends prefixes to PE**
  - No communities:
<img width="738" height="428" alt="image" src="https://github.com/user-attachments/assets/c8d68b9b-e740-49e3-8831-146bbde88d43" />
<br>
<br>

- **PE propagates CE routes to core:**
  - Extended Communities signal:
    - Service Label (assigned by the PE as an Egress LSR)
    - RT 
<img width="642" height="525" alt="image" src="https://github.com/user-attachments/assets/9adca1f2-d83a-418b-b353-516a35b88b40" />
<br>
<br>

- **Service Labels are signalled via MP_REACH_NLRI attributes:**
<img width="796" height="410" alt="image" src="https://github.com/user-attachments/assets/7c6449e1-60d5-4e5c-beb7-74a4ae23cfe3" />
<br>
<br>

- **PE to CE prefixes do contain ExtCommunities (is it excessive?):**
<img width="791" height="523" alt="image" src="https://github.com/user-attachments/assets/d706ab8d-504a-42d0-8221-5e444971fdf9" />
<br>
<br>

- **Replies to CE1 will contain CE1-generated service_label:**
<img width="642" height="230" alt="image" src="https://github.com/user-attachments/assets/8547dd3f-8005-4f88-a1be-8cee875b8bc3" />

- **Requests from CE1 to CE2 will contain:**
  - **service_label:**
    - PE2-generated 
  - **transport_label:**
    - P1-generated
<img width="752" height="166" alt="image" src="https://github.com/user-attachments/assets/7d285845-f2db-4fd0-956a-ab1e5b6cd844" />








