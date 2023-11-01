---
id: hbufmzqr4by8dm4rxrglecq
title: Internetworking
desc: ''
updated: 1698861137292
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

