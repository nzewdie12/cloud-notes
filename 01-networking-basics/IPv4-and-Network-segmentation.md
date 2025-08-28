# 9.0
## Unicast 
- one-to-one communication: one device sending a message to one other device.
## Broadcast
- one-to-all communication : one device sendin a message to all other devices.
- Directed broadcast is sent on all hosts on a speciic network. Basically targeting specific subnets.
  - 172.16.4.0/24 - > to all in the  172.16.4.255 hosts.
- limited broadcast is basicly sent to everyone
  - by default, routers do not forward broadcasts. 255.255.255.255
## Mulitcast
- one-to-group communicatoin: one devices sending a message to a multicast group
- IPv4 reserved the 224.0.0.0 to 239.255.255.255 addresses as multicast range.
- The hosts that recive the multicast packets are called multicast clients. Each multicast group is represented by a single IPv4 multicast destination address

---
## Types of IPv4 addresses
- public IPv4 adresses are addresses which are gloabally routed and between ISP routers.
- Their are blocks of addresses called private addresses that are used by most organizatoin to assign IPv4 addresses to internal hosts.
- 
