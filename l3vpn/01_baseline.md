## LDP (Transport) Label Signaling
- Hello
  - UDP from int_ip to mcst-224.0.0.2
  - Contains Loopback IP in TransportAddress field
- Initialization
  - TCP loopback_to_loopback
  - Label Advertise e.g. DownstreamUnsolicited 
  - LoopDetection e.g. disabled
- Keepalive
  - TCP loopback_to_loopback
- Address Message
  - TCP loopback_to_loopback
  - List of IPs on the sender_LSR
- Label Mapping Message
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
