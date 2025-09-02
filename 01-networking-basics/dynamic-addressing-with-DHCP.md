# 11.0
## Static and Dynamic Addressing (11.1)
### static IPv4 addresses must be manually configured.
  - at minimum it needs to include: IP address, Subnet mask, Default gateway - this identifies the networking device the host uses to access the internet (usualy the router).
  - Useful for printers, servers, and other devices that need to be accessible to clients on the network.  It is good if you need the address not to change.
  - Can provide increased control on network resources, but it can be time-consuming to set up and vulnerable to user error. These addresses are not normaly reused.

### Dynamic IPv4 address assignment
  - IPv4 can be automatically assigned with DHCP (Dynamic Host Configuration Protocol).
  - Generally preferred method for large networks.
  - no address is permanently assigned, rather it gets a asigned and once that host leaves the network , it can be reused.
  - preferred addressing for mobile users.

### DHCP Servers
  -  DHCP Servers assigns an IPv4 address to the host.
  -  Most medium to large networks, have the DHCP server as a locoal dedicated PC-based server
  -  Home netwokrs have the DHCP server located at the ISP.
  -  Your home router acts as both a DHCP Client and server
    - Client: Gets a public IPv4 address from the ISP
    - Server: Gives private IPv4 addresses to the host in the local network.
## DHCPv4 Configuration  
- A client that needs an IPv4 address will broadcast a DHCP Discover message. The DHCP server will than resond with a DHCP Offer, suggesting an IPv4 address
The Host than sends a DHCP Request asking to use that IPv4 Address, then the server responds with a DHCP Acknowledgment.
- DHCP Discover message has a  Destination IP as ( 255.255.255.255)
