# 17
## Troubleshooting Commands (17.1)
### Software utility programs

#### ipconfig(MAC: ifconfig) : Displays IP configuration information
  - just ipconfig: Displays basic config info: ***IP address, subnetmask, default gateway***
  - ipconfig /all: displays additional info: MAC Address, IP of the default gateway, and the DNS servers. If DHCP is enabled, the DHCP server address, lease info
  - ipconfig /release: will release the current DHCP bindings, and ipconfig /renew: will request fresh configuration information from the DHCP server.
#### ping: Tests connections to other IP hosts
- When a ping is sent to an IP address, a packet known as an echo request is sent across the network to the IP destination. If the host receives it, it sends an echo reply; if not, the request will time out.
  - If ping is sent to a domain name ( google.com) it is first sent to dns server then the ip address. if ping to ip address succedes but not the domain name, then problem with DNS.
  - a ping may fail even though network connectivity is fine, if there is a firewall on hte sending or reciving device.
  
#### netstat: Displays network connections

#### tracert(MAC: traceroute): Displays the route taken to the destination

#### nslookup: Directly queries the name server for information on a destination domain
