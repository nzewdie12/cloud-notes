# 10.0 
## The Need for IPv6 (10.1.1)
-  Increasing internet population, a limited IPv4 address space, issues with NAT and the IoT, have led to the transition to IPv6.
-  IPv6 has 128-bit address space, providing 340 undecillion possible addresses compared to IPv4 with 4.3 billion.
### The 3 IPv4 to IPv6 migration techneques:
- Dual Stack(known as Native IPv6)***prefered***: Devices run both IPv4 and IPv6 protocol stacks simultaneously.
- Tunneling is a method of transporting an IPv6 packet over IPv4 network. The IPv6 packet is encapsulated inside an IPv4 packet.
- Translation: NAT64(Network Address Translation 64 allows IPv6-enabled devices to comunicate with IPv4-enabled devices using a translation technique similar to NAt for IPv4.
  - IPv6 packet to IPv4 packet and vise-versa

## IPv6 addressing
- IPv6 addresses are represented using hexadecimal numbers
  - base 16 (16 digits) Known as ***Hextets***: 0123456789ABCDEF
- Each 4 bits is represented by a single hexadecimal digit.

### Preferred Format:
- IPv6 address is written: " x : x : x : x : x : x : x : x "
- x = 1 hextet = 4 hexadecimls (0bd8) = 16 bits
- example : "  fe80 : 0000 : 0000 : 0000 : c012 : 9aff : fe9a : 19ac "

### Reducing notation of IPv6 addresses
- Rule 1 : Omit Leading Zeros
  - 01ab = 1ab
  - 00ab = ab
  - 0a00 = a00
- Rule 2: Double Colon (::)
  - A double colon(::) can replace any single, contiguous string of one or more hextet's of 0's.
    -  "fe80 : 0000 : 0000 : 0000 : c012 : 9aff : fe9a : 19ac " =>  "fe80 :: c012 : 9aff : fe9a : 19ac "
    -  "fe80 : 0000 : c012 : 9aff : fe9a : 0000 : 0000 : 0000 "  =>  fe80 : 0000 : c012 : 9aff : fe9a ::
      - ***double colon (::) can only be used once***
 
