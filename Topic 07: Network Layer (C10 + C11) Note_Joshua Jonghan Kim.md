IP Address: provides us a way to identify networks and devices connected to these networks.

MAC Address Limitations : no organizational system

# IPv4 (32 bits)

0-255.0-255.0-255.0-255
ex) 6.4.240.111

2^32 = 2.1 billion (not many)

IPv4 : USA
IPv6 : Everywhere else
most IPv4 are reserved to US.
IPv4 Address Exhaustion Problem

# History  
# classful IPv4 Addressing (not used nowadays)

https://venus.cs.qc.cuny.edu/~rlaw/cs355/lectures/07-network-layer/images/class.png

Class A: (1 octet for network, 3 octets for host)
2^24 = 16M devices
first octet in the range 0-126

Class B: (2 octet for network 2 octets for host)
2^16 = 65k devices
first octet in the range 128-191

Class C: (3 octet for network, 1 octet for host)
2^8 = 254 hosts
first octet in the range 192-223

# CIDR - Classless Interdomain Routing (used today)
8.5.0.0/16 (/16 = subnet identifier (subnet mask))
= 00001000.00000101.00000000.00000000
= 16 bits are for network portion (00001000.00000101)

I want to change the IP address!

16.4.0.0/15
= 00010000.00000100.00000000.00000000
= 15 bits for network (00010000.0000010)
the rest is for host.

__In this case, decimal notation is not good anymore.
See, 16.4.255.10 and 16.5.11.2 are for same network!__