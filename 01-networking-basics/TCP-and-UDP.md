# 15.0
## TCP and UDP (Transport Layer Protocols)
- both contain source and destination numbers

### UDP ( User Datagram protocol)
- Packets lost are not retrasmiteted , Not worryied if some packets lost
- no acknoledgments, and no sequence numbers
- "best effort" delivery system

### TCP ( Transport Control Protocol)
- mechaniseum the fewist numbers of packets are lost , and lost one are retransmited
- each packet seqments has a sequence numbers on top of source and destination numbers
- constint communication is being held beteen the two end points ( source and destinatnion)
- has an acknowledgment of receipt of the packets
