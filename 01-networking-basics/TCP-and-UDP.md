# 15.0
## TCP and UDP (Transport Layer Protocols)
- both contain source and destination numbers
- Both use port numbers

### UDP ( User Datagram protocol)
- Mainly used for streaming and listing to things ( entertainment or live videos). Anything that requires minimul transmision delay
- Packets lost are not retrasmiteted , Not worryied if some packets lost
- no acknoledgments, and no sequence numbers
- "best effort" delivery system

### TCP ( Transport Control Protocol)
- Mechanisms with the fewest number of packets are lost, and lost packets are retransmitted
- each packet seqments has a sequence numbers on top of source and destination numbers
- constint communication is being held beteen the two end points ( source and destinatnion)
- has an acknowledgment of receipt of the packets

***Some applicatoins may use both TCP and USP***
- for example DNS uses UDP when clients send requeses to a DNS server, but uses TCP when two DNS servers are communicating with each other. 
## Transport Layer Port Numbers
- common port numbers for servers
  - HTTP (Web): 80
  - FTP: 21
  - Mail: 25
  - HTTPS(web secure) : 443
  - SSH(Secure shell): 22
- Port numbers allow servers to perform many different services ( web, ftp, mail) on one device
- Prot numbers allow hosts to use many different services at the same time 
- Requests and responses contain Destination port numbers and source port numbers
- When a message is recived by a server, port numbers are neccessary for teh servet ot be ab le to dertimein ewhich service is being requested by the client.
- Ports are assigned and managed by the ICANN ( Internet corporation for assigned names and numebrs.
- Ports are brokedn in to 3 categories
  -  Well-known ports - destination ports that are associated with common network applications : 1 -> 1023
  -  Registered ports -  Can be used as both source and dstination ports, and can eb used by organization to register specific applicaotin such as IM(instant message) applicatoins 1024 -> 49151
  -  Private ports - manily used as source ports ( clinet ), can be used by any application
## Socket Pairs 
- Sourse and destination ports are placed within segments.  Thes egmants are encapsulated within an IP packet. the IP packets contains the IP address of the source and destinatoin.
- ***The combination of the sourse IP address and source port number, or the same thing but for destinatoin , is kown as a socket***
  - A client socket might look like this 192.168.1.5:1099 ( where 1099 is the sourse port number)
  - A  web server socket might look like 192.168.1.7:80 ( 80 port number)
  - A socket pair would then be : 192.168.1.5:1099, 192.168.1.7:80 
- Source(clinet) Port numebrs are often dynamically genrated

***netstat command is used in terminal(command) to list he protocols in use, the local address and port numbers, the foreign address and port numebrs and the connectoins state***
