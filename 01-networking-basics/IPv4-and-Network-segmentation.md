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

### Private addresses and prefix 
- 10.0.0.0/8
- 172.16.0.0/12: 172.16.0.0 - 172.31.255.255
- 192.168.0.0/16
## Routing to the internet 9.2.2
- Most internal networks, from large enterprises to home networks, use private IPv4 addresses for internal devices (hosts and routers).
- ***Pirvate addresses are not gloabally routable***
- NAT(network address Translation) : is used to translate IPv4 private to a public adress. This is usually done on the router that connects to the ISP network.

## Special Use IPv4 Addresses (9.2.4)
- there are certian addresses, such as the netwokr address and broadcast address, that cannot be assigned to hosts.
- Loopback addresses: (127.0.0.0/8 [more commonly 127.0.0.1]) is used by a host to direct traffic to itself. It can be used to ping your own device.
- Link-local addresses (169.254.0.0/16) : are more commonly known as the Automatic private IP addressing (APIPA or Auto-IP) addresses. There are used by windows client to self-configre in the event that the client cannot obtain an IP addressing thorough methods. Can be used for peer-to-peer connection

***xxx.xxx.xxx.0 = network address , xxx.xxx.xxx.255 = broadcast address***
## Legacy Classful Addressing
- Class A (0.0.0.0/8 to 127.0.0.0/8) Designed to support extremely large networks with more that 16 millini host addresses
  - during 1981 : class A acounted for 50% of the IPv4 netwokrs 
- Class B (128.0.0.0/16 to 191.255.0.0/16) Designed to support the needs of moderate to large size networks with up to aproximately 65,000 host addresses
- Class C (192.0.0.0/24 to 223.255.255.0/24) Designed to support small netwokrs with a maximum of 254 hosts.
- Class D Mulitcast block 224 - 239
- Class E experamental block 240 - 255
- Classless addressing was introduced in mid 1990's to more efficently allocate the limited IPv4 address spaces

## Assignment of IP Addresses
- IANA(Internet assigned numbers authority) manages and allocates IP addresses to the RIR (Reginal Internet Registries). RIR are responsible for allocating IP address to ISPs who provide IPv4 address blocks to organizatoins and smaller ISPs. Organizations can also get their addresses directly from an RIR
### RIRs
- AfriNIC : Africa
- APNIC : Asia/Pacific
- ARIN : North America (not mexico)
- LACNIC : Latin America and some Carribean islands
- RIPE : Europe, The Middle East, and Central Asia.
