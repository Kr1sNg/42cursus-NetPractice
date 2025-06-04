# NetPractice 🕸️

the Internet and the Networking 🕸️


---

Exercise 6
A1:
IP       : 11010000 11000110 00101111 11100011 : xxx.xxx.xxx.227
/25 Mask : 11111111 11111111 11111111 10000000 : 255.255.255.128
Bitwise &: 11010000 11000110 00101111 10000000 : xxx.xxx.xxx.128 (network ad)
Network address: xxx.xxx.xxx.128
Broadcast address: xxx.xxx.xxx.255
Usable IP min : xxx.xxx.xxx.129
Usable IP max : xxx.xxx.xxx.254 (126 hosts)

R2:
IP       : 11010000 11000110 11100000 00001100 : xxx.xxx.xxx.12
/28 Mask : 11111111 11111111 11000000 11110000 : 255.255.255.240
Bitwise &: 11010000 11000110 11000000 00000000 : xxx.xxx.xxx.0 (network ad)
Network address: xxx.xxx.xxx.0
Broadcast address: xxx.xxx.xxx.15
Usable IP min : xxx.xxx.xxx.1
Usable IP max : xxx.xxx.xxx.14 (14 hosts)
Exercise 7:
This level introduces the concept of overlaps. The range of IP addresses of a network must not overlap the range of IP addresses of a separate network. Networks are separated by routers.
Between Client A and Router R1

R11
IP       : 11010000 11000110 00101111 00000001 : xxx.xxx.xxx.1
/28 Mask : 11111111 11111111 11111111 11110000 : 255.255.255.240
Bitwise &: 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0 (network ad)
Network address: xxx.xxx.xxx.0
Broadcast address: xxx.xxx.xxx.15
Usable IP min : xxx.xxx.xxx.1
Usable IP max : xxx.xxx.xxx.14 (14 hosts)
=> A1: xxx.xxx.xxx.2 /28
Between Router R1 and Router R2.

R12
IP       : 11010000 11000110 00101111 11111110 : xxx.xxx.xxx.254
/30 Mask : 11111111 11111111 11111111 11111100 : 255.255.255.252
Bitwise &: 11010000 11000110 00101111 11111100 : xxx.xxx.xxx.252 (network ad)
Network address: xxx.xxx.xxx.252
Broadcast address: xxx.xxx.xxx.255
Usable IP min : xxx.xxx.xxx.253
Usable IP max : xxx.xxx.xxx.254 (2 hosts)
=> R21: xxx.xxx.xxx.253 /30
Between Router R2 and Client C.

R22
IP       : 11010000 11000110 00101111 00010001 : xxx.xxx.xxx.17
/28 Mask : 11111111 11111111 11111111 11110000 : 255.255.255.240
Bitwise &: 11010000 11000110 00101111 00010000 : xxx.xxx.xxx.16 (network ad)
Network address: xxx.xxx.xxx.16
Broadcast address: xxx.xxx.xxx.31
Usable IP min : xxx.xxx.xxx.17
Usable IP max : xxx.xxx.xxx.30 (14 hosts)
=> C1: xxx.xxx.xxx.30 /28
Exercise 8
Between Internet - R1

Internet Destination
IP       : 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0
/26 Mask : 11111111 11111111 11111111 11000000 : 255.255.255.192
Bitwise &: 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0 (network ad)
Network address: xxx.xxx.xxx.0
Broadcast address: xxx.xxx.xxx.63
Usable IP min : xxx.xxx.xxx.1
Usable IP max : xxx.xxx.xxx.62 (62 hosts)
Internet Destination is 141.93.85.0/26 => R2, C, D should be in the range of Destination addresses to receive data from the internet
Between R1 - R2

R13
IP       : 11010000 11000110 00101111 00111110 : xxx.xxx.xxx.62
/30 Mask : 11111111 11111111 11111111 11111100 : 255.255.255.252
Bitwise &: 11010000 11000110 00101111 00111100 : xxx.xxx.xxx.60 (network ad)
Network address: xxx.xxx.xxx.60
Broadcast address: xxx.xxx.xxx.63
Usable IP min : xxx.xxx.xxx.61
Usable IP max : xxx.xxx.xxx.62 (2 hosts)
Between R2 - C and Between R2 - D

R22
IP       : 11010000 11000110 00101111 00000001 : xxx.xxx.xxx.1
/28 Mask : 11111111 11111111 11111111 11110000 : 255.255.255.240
Bitwise &: 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0 (network ad)
Network address: xxx.xxx.xxx.0
Broadcast address: xxx.xxx.xxx.15
Usable IP min : xxx.xxx.xxx.1
Usable IP max : xxx.xxx.xxx.14 (14 hosts)

R23
IP       : 11010000 11000110 00101111 00010001 : xxx.xxx.xxx.17
/28 Mask : 11111111 11111111 11111111 11110000 : 255.255.255.240
Bitwise &: 11010000 11000110 00101111 00010000 : xxx.xxx.xxx.16 (network ad)
Network address: xxx.xxx.xxx.16
Broadcast address: xxx.xxx.xxx.31
Usable IP min : xxx.xxx.xxx.17
Usable IP max : xxx.xxx.xxx.30 (14 hosts)
Exercise 9
Goal 2: host D - host C
R23
IP       : 11010000 11000110 10011011 00000001 : xxx.xxx.155.223
/18 Mask : 11111111 11111111 11000000 00000000 : 255.255.192.0
Bitwise &: 11010000 11000110 10000000 00000000 : xxx.xxx.128.0 (network ad)
Network address: xxx.xxx.128.0
Broadcast address: xxx.xxx.191.255
Usable IP min : xxx.xxx.128.1
Usable IP max : xxx.xxx.191.254 (16,382 hosts)

R22
IP       : 11010000 11000110 11000000 00000001 : xxx.xxx.192.1
/18 Mask : 11111111 11111111 11000000 00000000 : 255.255.192.0
Bitwise &: 11010000 11000110 11000000 00000000 : xxx.xxx.192.0 (network ad)
Network address: xxx.xxx.192.0
Broadcast address: xxx.xxx.255.255
Usable IP min : xxx.xxx.192.1
Usable IP max : xxx.xxx.255.254 (16,382 hosts)
Goal 6: host D - internet
R13
IP       : 11010000 11000110 00101111 11111110 : xxx.xxx.xxx.254
/30 Mask : 11111111 11111111 11111111 11111100 : 255.255.255.252
Bitwise &: 11010000 11000110 00101111 11111100 : xxx.xxx.xxx.252 (network ad)
Network address: xxx.xxx.xxx.252
Broadcast address: xxx.xxx.xxx.255
Usable IP min : xxx.xxx.xxx.253
Usable IP max : xxx.xxx.xxx.254 (2 hosts)
Goal 3: host A - internet
A1:
IP       : 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0
/25 Mask : 11111111 11111111 11111111 10000000 : 255.255.255.128
Bitwise &: 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0 (network ad)
Network address: xxx.xxx.xxx.0
Broadcast address: xxx.xxx.xxx.127
Usable IP min : xxx.xxx.xxx.1
Usable IP max : xxx.xxx.xxx.126 (126 hosts)
Exercise 10
S1:
IP       : 11010000 11000110 00101111 00000010 : xxx.xxx.xxx.2
/25 Mask : 11111111 11111111 11111111 10000000 : 255.255.255.128
Bitwise &: 11010000 11000110 00101111 00000000 : xxx.xxx.xxx.0 (network ad)
Network address: xxx.xxx.xxx.0
Broadcast address: xxx.xxx.xxx.127
Usable IP min : xxx.xxx.xxx.1
Usable IP max : xxx.xxx.xxx.126 (126 hosts)

H41
IP       : 11010000 11000110 00101111 10000000 : xxx.xxx.xxx.131
/26 Mask : 11111111 11111111 11111111 11000000 : 255.255.255.192
Bitwise &: 11010000 11000110 00101111 10000000 : xxx.xxx.xxx.128 (network ad)
Network address: xxx.xxx.xxx.128
Broadcast address: xxx.xxx.xxx.191
Usable IP min : xxx.xxx.xxx.129
Usable IP max : xxx.xxx.xxx.190 (62 hosts)

R22
IP       : 11010000 11000110 00101111 11000000 : xxx.xxx.xxx.192
/27 Mask : 11111111 11111111 11111111 11100000 : 255.255.255.224
Bitwise &: 11010000 11000110 00101111 11000000 : xxx.xxx.xxx.192 (network ad)
Network address: xxx.xxx.xxx.192
Broadcast address: xxx.xxx.xxx.223
Usable IP min : xxx.xxx.xxx.193
Usable IP max : xxx.xxx.xxx.222 (30 hosts)Reference

---