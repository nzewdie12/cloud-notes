# 7.0
## Encapsilation
- if data is represented as a letter, than the envelope is the frame. This proccess is called ** Encapsialtoin **
  - Encapsualtion is the process of prepending protocol information with information from another protocol. 
- Ethernet frame looks as follows:
  - Preamble  -> start frame delimiter -> Destination MAC address -> Source MAC address -> Length/Type -> DATA ( IP Packet)-> Frame check Sequence (check if everything is correct)
 
### Ethernet protocol operates at layer 2, the data link layer of the OSI Model.
---
## MAC Address Tables
- If mac address is not filled, the switch will fill the address by sending data to all ports to find the destination MAC (except the incoming port). This will be done as data is being moved thorught the switch.
- ### Initially it will add entriest to their MAC address tabel based the source MAC address
- Ethernet Hubs are Considered obsolete because they broadcast all traffic to every connected device, leading to significant network congestion, reduced bandwidth, and increased collision risks. In contrast, network switches are intelligent devices that learn MAC addresses and direct data only to the intended recipient.


### To maintain the MAC Address table, the switch uses the source MAC address of teh incoming packets and the port that the packets enter.
