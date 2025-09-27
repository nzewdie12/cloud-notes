# 16.0
## Client Server Relationship (16.1)
### Parts of a URI
- Web Resources and web services are identified using URI(Uniform Resource Identifier), which is a string whith charcters that identifies a specific network resource
- The two URI specializations are :
  - URN (Uniform Resource Name ) This identifies only the name space of the resource without referece to the protocol. ( Hostname + path and file name )
    - EX. WWW.example.com/author/book.html
  - URL (Uniform Resouce Locator) : This identifies the network locatoin of the specific reseroce on the network + the URN
    - EX. https;// WWW.example.com/author/book.html
  - The parts of the URI
    - Protocol/scheme:  HTTPS or others ( FTP, SFTP, mailto,and NNTP)
    - Hostname: www.example.com
    - Path and file name: /author/book/html
    - Fragment: #page155
   
## Common network applications (16.2)
### Protocols
- DNS (Domain Name System): resolves Internet names to IP addresses
- SSH (Secure Shell): used to provide remote access to servers and networking devices
- SMTP (Simple Mail Transfer Protocol): Sends email messages and attachments from clients to servers, and from servers to other email servers.
- POP (Post Office Protocol): Used by email clients to retrieve email and attachments from a remote server
- IMAP (Internet message access protocol): Used by email clients to retrieve email and attachemnets from remote server
- DHCP (Dynamic Host Configuration Protocol: Used to automatically configure devices with IP addressing and other necessary infomration to enable them to communicate over the internet.
- HTTP (Hyper Text Transfer Protocol): Used by web browsers to request web pages and web servers to treansfer teh files that make up web pages of the World Wide Web
- FTP (File Transfer Protocol): Used for interactive file transfer between systems.

## Domain Name System (DNS) (16.3)
- networks only "know" ip addresses
- Host would ask a DNS server what ip address is assostiated with the website (eg. WWW.Cisco.com) than the DNS server would respond with the ip address
- nslookup + hostname (www.example.com) = ip address of the website

## HTTP and HTML (16.4)
- The client browser uses the IP address and port 80 to request web services. the request is sent to the server using the HTTP ( Hypertext Transfer Protocol)
- The server recives the port 80 request, the server responds to the clinet request and send the web page to the clinet. The conntents of the webpage are encoded using HTML (hypertext markup language). ***HTML*** tells the browser how to format the web page and what grapics and fots to use.
- HTTP is not secure and can easily be intercepted by other users as data is sent over the network.
  - instead use ***HTTPS***, which is sent on ***port 443***

## File Transfer Protocol (FTP) (16.5)
- The FTP proviedes an easy method to transfer files from one computer to another.
- The first connection establisd is for traffic control and the second connection is created to transfer a file
- FTP service uses two diffrent ports to commmunicate between client and server.
- TCP : Port 21 is used to send commands and manage the FTP session, while port 20 is used to transfer the actual file data. In passive mode, a different, dynamically assigned port number is used for data transfer.

## Virtual Terminal (16.6)
- Telnet : Provides a standard method of emulating text-based terminal devices over the data network. Telnet uses software to create a virtual device that provieds the same features of a terminal session with access to the server's CLI (command line interace)
  - Applicaton layer protocol and serviese in the TCP/IP suite.
  - Telnet servers listen for client requests on ***TCP port 23***.
  - A connection using Telnet is called a virtual terminal.
  - *** NOT Secuire***
    - all date exchaged during Telnet sessions is transported as plaintext across the network , not encryptped.
- SSH ( Secure Shell) protocol is the secure alternateive to Telnet.

## Email Clients and Servers (16.7)
### Email Protocols
- SMTP (Simple Mail Transfer Protocol) : Is used by an Email client to send messages to its local email server.
  - if addressed to mailbox on diffrent server, than SMTP is used by the servers
  - ***SMTP requests are sent to port 25***
    

- POP3 ( Post Office Protocol): Similar to a post office, POP servers recives and stores messages addressed to its users. Basiclay email storage unitl user accesses it. Once accessed, they are no longer kept on the server.
  - ***POP3 servers on port 110*** 

  
- IMAP4 (Internet message access protocol): Server recives and stores messages addressed to its users and keeps them, unless delted by user.
  - Similar to POP, but keeps the messages after user access them.
  - ***IMAP4 requests on port 143***

### Internet Phone Calls 
- IP telephony makes use of VoIP (Voice over IP technology). Which converts analog voice signals into digital data
- The voice data is encapsulated into IP packets which carry the phone call thorugh the network
- When software is installed users mush have a unique name, speaker and a mic.
- Calls to other users onteh same service on the internet is simple, but call to regular telephones requere using a gateway to access the PSTN (public switched Telephone Network)












 
