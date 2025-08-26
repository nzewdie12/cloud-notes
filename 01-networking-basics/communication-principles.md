# 5.0
- Media Access Control : Mac Address

### Protocol Charicteristic 
####: Protocols are the rules that govern network communications including the message format, message size, timing and encapsulation.
- Message format : message formats depend ont eh type of messge and the channel that it used
- Message size
- timing
- Encoding: messages sent across the network are first convertid into bits by the sending host, each bit is then encoded into a pattern of
sounds, light waves or electriccal pulseses. The destination host then decodes it
- Encapsulaton: each message trasmitted on a network must include a header that sontains addressing infomration that identifies the source
and destination host. it also might include other inomration to delever to the correct appilaton on the destination host.
- Message pattern : response to reciving the message.

### TCP/IP Model Layers (Protocol Model)
- Application : Represents Data to the user, plus encoding and dialog control.
  - HTTP, DNS , FTP
- Transport : Supports Communiaton between various devices across diverse networks
  - TCP, UDP
- Internet : Determines the best path through the network. Internet Protocol (IP) is used by routers to forward messages.
  - IPV4, IPV6
- Network Access : Controls the hardware devices and meda that make up the network.
  - Ethernet, WI-FI

### OSI Model Layer (Reference Model)
7. Applicaton : The application layer contains protocols used for process-topreocess ommunications
6. Presentation : The presentatoin layer provieds for common representation of the data transferred between application layer services.
5. Session : The session layer provied services to presentaion layer to organize its dialogue and to manage data exchange
4. Transport: The transport layer defines services to segment, transfer, and reassembel the data for individual communications beween the end devices.
3. Network : This layer provied services to exhange the individual pieces of data over the network betweeen identified end devices.
2. Data Link : This layer protocols describe methods for exchanging data frames between devices over a common media.
1. Physical : This layer protocols describe the mechanical electrical ... means to activeate, maintain and de-activeate physical connections for a bit transmission to and from a netwokr device.   


- The TCP/IP application layer includes several protocols that provide specific functionality to a variety of end user applications. The OSI model Layers 5, 6, and 7 are used as references for application software developers and vendors to produce applications that operate on networks.
- Both the TCP/IP and OSI models are commonly used when referring to protocols at various layers. Because the OSI model separates the data link layer from the physical layer, it is commonly used when referring to these lower layers.
