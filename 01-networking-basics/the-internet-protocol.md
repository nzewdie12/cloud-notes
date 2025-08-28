# 8.0
## IPv4
- it must be properly configured and unique within the LAN, for local communicatoin. It must also be properly configured and unique in the world,
for remote communicaiton.
- IPv4 address is assigned to the network interface connectin for a host. Usualy the NIC(network interface card) installed on the device.
- Basicly if it has a NIC it has an IPv4 address, 2 nic = 2 ip addresses
- router interfaces that provide connection to an IP network will also have IPv4 address.
- IPv4 addresses are 32 bits long -> then converted to 4 (8-bit bytes) called octets -> then finaly into decimal values (209.165.200.1)

### IPv4 Networks and Hosts (example IPv4 : 192.168.5.11)
- The LAN :network section [192.168.5] The first three octets;  the host part [.11] the last octet
- This is hierarchical addressing and the routers only need to know how to reah each netowrk, rhtern thean the location each host.
- Muliple logical networks can exist in one physical network. Even if they are all connected only the hosts that share the same network portion
of the IPv4 can communicate (without the use of routing)
### Subnet (ie. SUB Network)
- Subnet mask is used to identify the network on which the host is connected.
- **subnet mask is used to tell how to break up network and host**
 - 192.168.5.11 with a subnet of 255.255.255.0 = Network portion : 192.168.5.0 || Thus devises on same netwokrk can be 192.168.5.1 192.168.5.99 
 - 192.168.5.11 with a subnet of 255.255.0.0 = Network portion : 192.168.0.0|| Thus devises on same netwokrk can be 192.168.5.1 192.168.7.99 
