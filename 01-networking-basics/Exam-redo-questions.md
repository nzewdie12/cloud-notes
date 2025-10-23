# Checkpoint Exam: Protocols for specific Tasks
- Which action is performed by a client when establishing communication with a server via the use of UDP at the transport layer?
 - The client randomly selects a source port number.
  - Explanation: Because a session does not have to be established for UDP, the client selects a random source port to begin a connection. The random port number selected is inserted into the source port field of the UDP header.
# Course Final Exam
- ARP request
- Multicasting
- DHCP config
- TCP/ip vs OSI Model
- Powerline netwoking
- Wireless RF band 

### Review Q&A
- Question: What will a Cisco LAN switch do if it receives an incoming frame and the destination MAC address is not listed in the MAC address table?
  - A : Forward the frame out all ports except the port where the frame is received.
  - Explanation: A LAN switch populates the MAC address table based on source MAC addresses. When a switch receives an incoming frame with a destination MAC address that is not listed in the MAC address table, the switch forwards the frame out all ports except for the ingress port of the frame. When the destination device responds, the switch adds the source MAC address and the port on which it was received to the MAC address table.

- Question: What layer is responsible for routing messages through an internetwork in the TCP/IP model?
  - A: internet
  - Explanation: The TCP/IP model consists of four layers: application, transport, internet, and network access. Of these four layers, it is the internet layer that is responsible for routing messages. The session layer is not part of the TCP/IP model but is rather part of the OSI model.

- Question: At which layer of the OSI model would a logical address be added during encapsulation?
  - A: network layer
  - Explanation: Logical addresses, also known as IP addresses, are added at the network layer. Physical addresses are edded at the data link layer. Port addresses are added at the transport layer. No addresses are added at the physical layer.

- Question: A company uses DHCP servers to dynamically assign IPv4 addresses to employee workstations. The address lease duration is set as 5 days. An employee returns to the office after an absence of one week. When the employee boots the workstation, it sends a message to obtain an IP address. Which Layer 2 and Layer 3 destination addresses will the message contain?
  - A: FF-FF-FF-FF-FF-FF and 255.255.255.255
  - Explanation: When the lease of a dynamically assigned IPv4 address has expired, a workstation will send a DHCPDISCOVER message to start the process of obtaining a valid IP address. Because the workstation does not know the addresses of DHCP servers, it sends the message via broadcast, with destination addresses of FF-FF-FF-FF-FF-FF and 255.255.255.255.

- Question: A newly purchased client laptop has just connected to the local area network. The local area network is using a wireless router that is providing dynamic addressing as shown. Which IP address does the laptop use as a destination address when requesting a dynamically assigned address?
  - A: 255.255.255.255
  - Explanation: When a new client device is installed on a network that uses dynamic IP addressing, the client will send out a DHCP request message with the destination IPv4 address of 255.255.255.255.

- Question:What are two characteristics of multicast transmission? (Choose two.)
  - A : 1)  Multicast transmission can be used by routers to exchange routing information.
       2)  A single packet can be sent to a group of hosts.
  - Explanation: Broadcast messages consist of single packets that are sent to all hosts on a network segment. These types of messages are used to request IPv4 addresses, and map upper layer addresses to lower layer addresses. A multicast transmission is a single packet sent to a group of hosts and is used by routing protocols, such as OSPF and RIPv2, to exchange routes. The address range 224.0.0.0 to 224.0.0.255 is reserved for link-local addresses to reach multicast groups on a local network.

- Questoin: What type of route is indicated by the code C in an IPv4 routing table on a Cisco router?
  - A: directly connected route
  - Explanation: Some of the IPv4 routing table codes include the following:
      C – directly connected
      S – static
      D – EIGRP
      "* " – candidate default

- Question: Host H2 sends a unicast message to host H6.  Which destination IP address is contained in the header of the packet when it reaches host H6?
  - A: the IP address assigned to the network adapter on host H6
  - Explanation: When host H2 sends the packet to host H6, the source IP address is the address assigned to the network adapter on host H2. The destination address of the packet is the IP address assigned to the network adapter on host H6. The source and destination IP addresses do not change as the packet is forwarded through the routers. When the packet arrives at H6 the destination address of the packet is the address assigned to the network adapter on H6.

- Queston: When analog voice signals are converted for use on a computer network, in what format are they encapsulated?
  - A: IP packets
  - Explanation: When Voice over iP (VoIP) is being used, analog voice signals are translated into digital data in the form of IP packets. This translation allows the phone call to be carried through a computer network.

---------------
PT 2.

- Port number 53 for DNS

-  Question: Which statement describes the use of powerline networking technology?
  - A : A device connects to an existing home LAN using an adapter and an existing electrical outlet.
  - Explanation: Powerline networking adds the ability to connect a device to the network using an adapter wherever there is an electrical outlet.​ The network uses existing electrical wiring to send data. It is not a replacement for physical cabling, but it can add functionality in places where wireless access points cannot be used or cannot reach devices.​

- Q : how many bits in IPv4 address
  - A : 32
  - Expl: 4 octetns of binary digits, each contains 8 bits ( 4 x 8 = 32)
  ***128 bits in IPv6***
- Q : Which two TCP header fields are used to confirm receipt of data?
  - A : The two TCP header fields used to confirm receipt of data are the Sequence Number and the Acknowledgment Number
  - Expl: The Sequence Number keeps track of the order of data bytes sent, while the Acknowledgment Number is sent back by the receiver to indicate the next expected sequence number, confirming that all data up to that point has been successfully received.
-  













  

   
