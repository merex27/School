---
id: hbufmzqr4by8dm4rxrglecq
title: Internetworking
desc: ''
updated: 1700068489415
created: 1695822925384
---

## [Notes by Nick](https://drive.google.com/drive/folders/1dK7et2KKT6VIE0k5FNf3iU33vphMX413)

## Week 0
[Introduction PDF](/Internetworking/Week%200%20-%20Introduction.pdf)

## Week 1
[DHCP and DNS PDF](/Internetworking/Week%201%20-%20DHCP%20and%20DNS.pdf)

## Week 2
[IP Addressing Lecture](/Internetworking/Week%201%20-%20IP%20Addressing.pdf)

### IP - Internet protocol
* Connectionless (delivering datagrams)
* best effort
* unreliable (no guarantee of delivery)

### How it work!
(When sending)  
Ip encapsulates data from transport layer to datagrams, prepare header and apply routing algorithm.

(When receiving)  
Checks validity if datagrams, read headers, checks for forwarding(if no[...]if yes[...])

### IP Address (IPv4)
* 32 bit string split between network ID and host ID
* 4 octets
* dotted notation
* each byte from 0 to 255

Network ID can be 8,16 or 24 bits (depending on class) rest of bits are for host IDs.

Class A - NNNN.HHHH.HHHH.HHHH  
Class B - NNNN.NNNN.HHHH.HHHH  
Class C - NNNN.NNNN.NNNN.HHHH  
Class D - multicast  
Class E - experimental use

Default masks:  
Class A - 255.0.0.0 (/8)  
Class B - 255.255.0.0 (/16)  
Class C - 255.255.255.0 (/24)  

127.0.0.1 - Loopback/Localhost

Network address - first address of host part  
Broadcast - last address of host part

[IP Addressing Labs](/Internetworking/Week%202%20-%20IP%20Addressing%20Labs.pdf)

[Answers](/Internetworking/Week%202%20-%20IP%20Addressing%20Labs%20Answers.pdf)

## Week 3 and 4

[IP Addresses and Subnets PDF](/Internetworking/Week%203%20-%20IP%20Addresses%20and%20Subnets.pdf)

[Subnetting vs Supernetting Labs](/Internetworking/Week%203%20-%20Subnetting%20vs%20Supernetting%20Labs.pdf)

## Week 4

[VLSM PDF](/Internetworking/Week%204%20-%20Subnets%20VLSM.pdf)

[VLSM Labs PDF](/Internetworking/Week%204%20-%20VLSM%20Labs.pdf)

## Week 5

[Supernetting PDF](/Internetworking/Week%205%20-%20Supernetting.pdf)

## Week 6

[Routing PDF](/Internetworking/Week%206%20-%20Routing.pdf)

**Routing** - the act of forwarding a packet from one router to another router towards the destination host.

**Gateway** - router that connects two networks

Static routing - manually configured routing table by network admin, not scalable, not viable for large networks

Anatomy of a routing table entry:
* Code - what process discovered the route
* Network and mask - destination network and mask
* AD/Metric - administrative distance and metric
* Next hop - IP address of next hop
* Interface - exit interface

Routers supporting different protocols can be used in the same network.

**Convergence** - when all routers have the same routing table

**Routing loop** - when a packet is forwarded between two routers in a circular fashion, it occurs when there is a problem with the routing table (slow convergence, incorrect metric, incorrect AD).

Metric:
* Hop count - number of routers between source and destination
* Path length - sum of the link speeds between source and destination
* Bandwidth - the bandwidth of the slowest link between source and destination
* Delay - the sum of the delays between source and destination
* Load - the load on the slowest link between source and destination
* Reliability - the reliability of the slowest link between source and destination (based on bit error rates)

## Week 7

[RIP PDF](/Internetworking/Week%207%20-%20RIP.pdf)

[RIP Labs](/Internetworking/Week%207%20-%20RIP%20Labs.pdf)
