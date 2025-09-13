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
   
## Common network applications
### Protocols
- DNS (Domain Name System): resolves Internet names to IP addresses
- SSH (Secure Shell): used to provide remote access to servers and networking devices
- SMTP (Simple Mail Transfer Protocol): Sends email messages and attachments from clients to servers, and from servers to other email servers.
- POP (Post Office Protocol): Used by email clients to retrieve email and attachments from a remote server
- IMAP (Internet message access protocol): Used by email clients to retrieve email and attachemnets from remote server
- DHCP (Dynamic Host Configuration Protocol: Used to automatically configure devices with IP addressing and other necessary infomration to enable them to communicate over the internet.
- HTTP (Hyper Text Transfer Protocol): Used by web browsers to request web pages and web servers to treansfer teh files that make up web pages of the World Wide Web
- FTP (File Transfer Protocol): Used for interactive file transfer between systems.
