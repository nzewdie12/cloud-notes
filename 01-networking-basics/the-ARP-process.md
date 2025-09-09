# 13.0
## Mac and IP (13.1)
- There are 2 primary addresses assigned to a device on an Ethernet LAN:
  - Physical adddress( The Mac address) - used for NIC-to-NIC communication on same ethernet network
    - Layer 2 physical addresses are used to deliver the data link frame with the encapulated IP packet from one NIC to another. 
  - Logical address(the IP address)
    - Layer 3 logical address contains the actual IP packet
- When the destination IP address (IPv4 or IPv6) is on a remote network, ***the destination MAC address will be the address of the default gateway( the router interface)***.
- When a host sends a packet to a remote host, it will encapsulates the IPv4 packet in a data link frame and send it to the router.
  - The destination address will be the remote host's IP address and the routers Mac address. It will also have the hosts source IP and Mac Address.
  - When it gets to the router, it de-encapulates the layer 2 info, and then (if it is going to a diffrent router) it will encapsulate the packet in a new data link frame with its own ( the router's ***interface***) source MAC address and the next routers Destination MAC address ***interface***.
- The frame is specific to the data link technology that is associated with that link, such as Ethernet.
  - ***Data Link frame include : Destination MAC | Source MAC | Source IPv4 | Destination IPv4***

### ARP (13.2.5)
- The ARP(for IPv4) can be thought as the proccess to associate the MAC addresses on each link along the path. For IPv6 this is called the ICMPv6 Neighbor Discovery (ND).
  - The sending host can use an IPv4 protocol called ARP(address resolution protocol) to discover the MAC address of any host on the same local network.
- ARP uses a three step process to discover and store the MAC address of a host on the ***local network*** when only the IPvr address of the host is known:
  -  ***ARP Request*** The sending host creates and sends a frame addressed to a broadcast MAC ( FF:FF:FF:FF:FF:FF) and the inteded host's IPv4 address.
  -  ***ARP Reply*** each host on the network will recive the broadcast frame and check if they are the inteded host for the message. If they are the inteded host, they will send thier MAC address back to the origianl host
  -  The original host will then store the MAC and IPv4 address info in a table called ***ARP Table***.
 
- 
