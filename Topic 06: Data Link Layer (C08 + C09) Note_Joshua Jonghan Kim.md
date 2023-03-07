# Topic 06: Data Link Layer (C08 + C09) Note_Joshua Jonghan Kim
Delivery of messages between directly connected adjacent nodes
wireless, fiber, copper has different protocol, so each requires different headers

—-DLL(Wifi)----
dest MAC = R1 //changes into R2 or R3 or destination or etc.
—-Network Layer----
destination IP : 1.2.3.4
—-Transport Layer----
dest app = web server
—-message----
“Hello World”

Network Layer
Logical Link Control //DLL
Media Access Control //DLL
Physical Layer

LLC
1. receives IP packet from network layers
2. chooses which outbound connection to use
3. Atlach the matching DLL header before sending to MAC

MAC address(6 bytes)
globally unique identifier for a network card

IEEE

3bytes OUI, 3bytes NIC
7c:A2:04 is for INTEL.
Each device of INTEL has a different NIC.




A –-wifi— R1 —cable— R2 —cable— R3 —wifi— D
4 hops
header is changed at each hop. wifi or ethernet or … and MAC also changes.

A—ㄱ
B——S1—cable— R1 —cable— R2 —cable— R3 —wifi— D
C—
How many DLL hops?
just 4! Switch is just a cable!

What is the job of HUB and Switch?
act as a n-dimensional cable.
Hub has a collision problem, but the switch has no such problems.
Switch : a passive device that acts as n-dimensional cable. to allow multiple connected devices to form a local area network.

Switch Device Discovery Algorithm
1. Upon receiving a new frame, record the Src MAC Address and the incoming port# to the FIB(forwarding information base).

Switch has a memory and it has a 3-column table. (MAC, Port#, Expiration)
MAC Port# Expiration
A	P1	3/1/2024
C	P2 	3/12024

2. Check FIB for Destination MAC 
if found 
forward it on the matching port#
else : revert to hub mode: Flood Message on ALL Other(not through input port) ports. (one MAC has only one Port#, but one Port# can has multiple MACs.)
When A->D, it reverts to hub mode.

Ethernet Header Format

CRC: Cyclic redundancy check

FCS : Frame Check Sequence
= data integrity algorithm which uses CRC32

Ethernet: data frame

Wifi:
-management frame
-control frame
-data frame

Management Frame
assists in connecting and disconnecting devices
-beacon : SSID, transfer rate, encryption
-Probes : automatically connect next time
-Authentication: credentials
-Association: 

Control: Assists in the delivery of messages and are necessary due to the half duplex nature of Wi-Fi
-ACKs: reply when receive
-Block-ACKS: reply for multiple input
-RTS/CTS: to avoid collision in wireless environment

