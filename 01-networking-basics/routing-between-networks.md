# 14.0
## need for routing
- to contain broadcasts ( into separate broadcast domains)
- for security reasons
- flexibility to move physical locations
- Routing is a process to determine the best path to a destination.
- Logical Grouping ( admin vs. HR vs. finance)
## Routers 
- ***A router is a network device that connects multiple layer 3, IP networks.***
- at the distributin layer of the network, routers direct traffic and preform other funtions critical to efficent network operations
- Routers, like switches, are ablte to decode and read teh messages tha are sent to them.
  - unlike switches, mehc make theier forwared decises based on teh Layer 2 Mac address, reouters forwarding decsions based ont the Layer 3 IP address.
- Step by step process
  - host will forwared a message the is going to a remote host to the local router -> the router recives and de-encapsualtese the ethernat frame
  then reades teh destiantion ip address. It then re-encapsulates the packet back in a new data frame, and forwared the frame on to its destination.

###
- if Host knows (because of its subnet mask) that the destination host is on the same network, it does not need to go to the router. 
- if it is not on the same network, it will set the destination MAC address to the default gatway ( or if it doesnt have that it will set an ARP request).
- then once it gets the MAC address of the interface ( each router has mulitple interfaces [ NIC's]).
-  Then the router will send the packet based on the routing table which tells the router which interface is connected to which subnet .
-  Then it will encapsulate the ethernet frame with the interface as the source MAC and the dest MAC as the intended destination.



### ARP Table - Routing Table
- Each host has an ARP table to catigorize a mac address with an IP address
- Each Router has a routing address that assosiattes each interface (port on router) with an ip subnet ( 192.168.1.0/24)
  - entries on a routing table can be made dynamically , by updating info as it recives it from the routers. It can  also be manualy entered.
  - A router will drop a message if it can not deterime where to send it to , unless a static default route was set up by a netwok admin.
    - a static default route is the interface through which the router forward a packet containing an unkown destination IP network address.This default route usually connects to another router that can forward the packet towareds its final destination network.

 ### LAN
 - LAN (Local Area Networks) refers to a local network, or a group of interconnected local networks ***under the same administrative control***
   - LAN typacally use Ethernet or wireless protocols, and they support high data rates.
   - Term Intranet refer to a private LAN that belongs to an organization.
  


## Practice test wrong answer :
 Q :A host needs to reach another host on a remote network, but the ARP cache has no mapping entries. To what destination address will the host send an ARP request?

A : the broadcast MAC address

Explanation: ARP requests are sent when a host does not have an IP to MAC mapping for a destination in the ARP cache. ARP requests are sent to the Ethernet broadcast of FF:FF:FF:FF:FF:FF. In this example because the address of the remote host is unknown, an ARP request is sent to the Ethernet broadcast to resolve the MAC address of the default gateway that is used to reach the remote host.
