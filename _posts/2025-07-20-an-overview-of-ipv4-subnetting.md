---
title: An overview of IPv4 subnetting
date: 2025-07-20 10:00 PM
categories: [Miscellaneous]
tags: [subnetting]
---

In this post, I'm going to go over the basics of IPv4 subnetting. Subnetting is a complex topic that takes time and practice to learn, and sometimes it helps to see it taught from a different perspective. My hope is that this post will help you gain a better understanding of subnetting and potentially give you that "Aha!" moment. I'm also assuming that if you're reading this post, you already have a basic understanding of IPv4 and concepts such as binary and subnet masks. So, I'll only provide a brief overview of the basics before going over subnetting. 

## IPv4 Address
An IPv4 address is a 32-bit address, written in decimal format, that is used to uniquely identify a device on a network. It is separated into 4 8-bit sections called "octets," with each octet containing a number ranging from 0 to 255. Each bit in an octet has a corresponding decimal value and is either a 0 or 1, which corresponds to being off or on. In binary, the value of every bit is calculated using a power of 2, and the bit only has value if it is on. For example, in the table below, the value of the leftmost bit would be calculated as 2<sup>7</sup> = 128.

**8 bit octet chart**

| ----------    | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Power of 2    | 2<sup>7</sup> | 2<sup>6</sup> | 2<sup>5</sup> | 2<sup>4</sup> | 2<sup>3</sup> | 2<sup>2</sup> | 2<sup>1</sup> | 2<sup>0</sup> |
| bit Value     | 128           | 64            | 32            | 16            | 8             | 4             | 2             | 1             |

**Example IPv4 Address:** `192.168.1.0`

|           | 1st octet | 2nd octet | 3rd octet | 4th octet |
| -------   | --------- | --------- | --------- | --------- |
| Decimal   | 192       | 168       | 1         | 0         |
| Binary    | 11000000  | 10101000  | 00000001  | 00000000  |
|           | 8 bits    | 8 bits    | 8 bits    | 8 bits    |

## Subnet Mask
The subnet mask is a 32-bit address that is used to identify the network and host portions of an IP address. In the example below, we have the IP address `192.168.1.0` with a subnet mask of `255.255.255.0`. This means that the first 3 octets (or 24 bits) represent the network portion of the address, while the last octet (or 8 bits) represents the host portion. So, to calculate our number of hosts, we take 2 to the power of 8, which is our number of host bits, and that gives us 2<sup>8</sup> = 256. We then subtract 2 addresses for our network and broadcast address, which gives us 254 usable hosts ranging from `192.168.1.1` to `192.168.1.254`.

|               | Network  | Network  | Network  | Host     |
| ------------- | -------- | -------- | -------- | -------- |
| IP Address    | 192      | 168      | 1        | 0        |
| Subnet Mask   | 255      | 255      | 255      | 0        |
| Subnet Binary | 11111111 | 11111111 | 11111111 | 00000000 |

## Public IPv4 Address Ranges
This table provides an overview of the public IPv4 address ranges.

| Class            | Range   | Default Subnet Mask | # of Networks | # of Hosts |
| ---------------- | ------- | ------------------- | ------------- | ---------- |
| A                | 1-126   | 255.0.0.0           | 126           | 16,777,214 |
| B                | 128-191 | 255.255.0.0         | 16,384        | 65,534     |
| C                | 192-223 | 255.255.255.0       | 2,097,152     | 254        |
| D (Multicast)    | 224-239 |                     |               |            |
| E (Experimental) | 240-255 |                     |               |            |

## Private IPv4 Addresses RFC 1918
This table provides an overview of the private IPv4 address ranges as defined by RFC 1918. These address ranges are reserved for use in private networks and are not routable on the public internet.

| Class | Range                       | CIDR Prefix (Subnet Mask)    |
| ----- | --------------------------- | ---------------------------- |
| A     | 10.0.0.0-10.255.255.255     | 10.0.0.0/8 (255.0.0.0)       |
| B     | 172.16.0.0-172.31.255.255   | 172.16.0.0/12 (255.240.0.0)  |
| C     | 192.168.0.0-192.168.255.255 | 192.168.0.0/16 (255.255.0.0) |

## CIDR
CIDR, or Classless Inter-Domain Routing, is a standard that allows for a more efficient method of IP address allocation compared to the old classful-based system. With the old classful-based system, each IPv4 address class had a fixed number of network and host bits and a predetermined subnet mask. That method was very inefficient and led to a lot of wasted IP addresses. With CIDR, you can assign a subnet mask or prefix based on your individual needs, reducing the number of wasted IP addresses.

The way CIDR works is that you have an IP address followed by a slash and a number, which corresponds to the prefix length, or number of network bits. For example, `192.168.1.0/24` represents a prefix length of /24, meaning that the first 24 bits are associated with the network portion. Below is a table showing the CIDR prefix lengths along with the associated decimal subnet mask and number of network and host bits.

| CIDR | Subnet Mask     | Network Bits | Host Bits |
| ---- | --------------- | ------------ | --------- |
| /1   | 128.0.0.0       | 1            | 31        |
| /2   | 192.0.0.0       | 2            | 30        |
| /3   | 224.0.0.0       | 3            | 29        |
| /4   | 240.0.0.0       | 4            | 28        |
| /5   | 248.0.0.0       | 5            | 27        |
| /6   | 252.0.0.0       | 6            | 26        |
| /7   | 254.0.0.0       | 7            | 25        |
| /8   | 255.0.0.0       | 8            | 24        |
| /9   | 255.128.0.0     | 9            | 23        |
| /10  | 255.192.0.0     | 10           | 22        |
| /11  | 255.224.0.0     | 11           | 21        |
| /12  | 255.240.0.0     | 12           | 20        |
| /13  | 255.248.0.0     | 13           | 19        |
| /14  | 255.252.0.0     | 14           | 18        |
| /15  | 255.254.0.0     | 15           | 17        |
| /16  | 255.255.0.0     | 16           | 16        |
| /17  | 255.255.128.0   | 17           | 15        |
| /18  | 255.255.192.0   | 18           | 14        |
| /19  | 255.255.224.0   | 19           | 13        |
| /20  | 255.255.240.0   | 20           | 12        |
| /21  | 255.255.248.0   | 21           | 11        |
| /22  | 255.255.252.0   | 22           | 10        |
| /23  | 255.255.254.0   | 23           | 9         |
| /24  | 255.255.255.0   | 24           | 8         |
| /25  | 255.255.255.128 | 25           | 7         |
| /26  | 255.255.255.192 | 26           | 6         |
| /27  | 255.255.255.224 | 27           | 5         |
| /28  | 255.255.255.240 | 28           | 4         |
| /29  | 255.255.255.248 | 29           | 3         |
| /30  | 255.255.255.252 | 30           | 2         |
| /31  | 255.255.255.254 | 31           | 1         |
| /32  | 255.255.255.255 | 32           | 0         |

## Subnetting
In this section, I'm going to cover two different approaches to subnetting, known as FLSM (Fixed Length Subnet Mask) and VLSM (Variable Length Subnet Mask). Subnetting is simply the process of taking a larger network and breaking it into several smaller ones. This also provides many benefits, such as improved network performance, easier management, and better security, just to name a few.

With subnetting, what you're doing is borrowing host bits to create the desired number of networks. You can calculate the number of networks using the formula **2<sup>n</sup>**, where n equals the number of borrowed host bits. To calculate the number of usable hosts, you use the formula **2<sup>n</sup>-2**, where n is the number of host bits. Another important aspect is the bit values, which are used to determine the block size. Below, I have included tables of the formulas and block sizes for reference. 

**Subnetting Formulas**

|                    | Formula         | Explanation                            |
| ------------------ | --------------- | -------------------------------------- | 
| Number of Networks | 2<sup>n</sup>   | Where n = number of borrowed host bits | 
| Number of Hosts    | 2<sup>n</sup>-2 | Where n = number of host bits          |

**Block Size**

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

### FLSM
FLSM (Fixed Length Subnet Mask) is a subnetting method in which all subnets use the same subnet mask and have the same number of hosts.

**Example**

As an example, let's say I start with the network `192.168.1.0/24` and need to create 2 subnets with 100 usable hosts in each subnet. Since we are starting with a /24, we have 24 network bits and 8 host bits. So, to create 2 subnets, we would have to borrow 1 host bit, which would give us 2<sup>1</sup> = 2 subnets. That would leave us with 7 host bits, giving us 2<sup>7</sup>-2 = 126 usable hosts per subnet, which would meet our need for 100 usable hosts per subnet. Our new prefix length for our subnets would be a /25, and our block size would be 128.

|                   | Subnet 1       | Subnet 2         |
| ----------------- | -------------- | ---------------- |
| Network Address   | 192.168.1.0/25 | 192.168.1.128/25 |
| First Usable Host | 192.168.1.1    | 192.168.1.129    |
| Last Usable Host  | 192.168.1.126  | 192.168.1.254    |
| Broadcast Address | 192.168.1.127  | 192.168.1.255    |

### VLSM
VLSM (Variable Length Subnet Mask) is a more efficient subnetting method that allows the creation of subnets of varying sizes using different subnet masks. VLSM is a little more complicated than FLSM, but it still follows the same general principles of subnetting.

**Example**

As an example, let's say I have a starting network of `192.168.1.0/24` and need to create 4 subnets with the host requirements of subnet 1 = 105, subnet 2 = 55, subnet 3 = 25, and subnet 4 = 10. With VLSM, we're going to assign our subnets based on host requirements, starting from the largest subnet to the smallest. We would start with the largest subnet, subnet 1, and assign it a prefix length of /25, which has a block size of 128, to meet our host requirement. That would give subnet 1 a network address of `192.168.1.0/25`, a usable host range of `192.168.1.1` through `192.168.1.126`, and a broadcast address of `192.168.1.127`.

Next, we would move on to subnet 2 and assign it a network address of `192.168.1.128`, which is 1 address higher than subnet 1's broadcast address. To meet subnet 2's host requirement, we would assign it a /26 prefix with a block size of 64. We would then repeat the same steps and assign subnet 3 a /27 prefix and subnet 4 a /28 prefix. Below, I have included a table outlining each subnet, as well as a table showing the CIDR prefix lengths and corresponding block sizes for reference.

|                   | Subnet 1       | Subnet 2         | Subnet 3         | Subnet 4         |
| ----------------- | -------------- | ---------------- | ---------------- | ---------------- |
| Number of Hosts   | 105            | 55               | 25               | 10               |
| Network Address   | 192.168.1.0/25 | 192.168.1.128/26 | 192.168.1.192/27 | 192.168.1.224/28 |
| First Usable Host | 192.168.1.1    | 192.168.1.129    | 192.168.1.193    | 192.168.1.225    |
| Last Usable Host  | 192.168.1.126  | 192.168.1.190    | 192.168.1.222    | 192.168.1.238    |
| Broadcast Address | 192.168.1.127  | 192.168.1.191    | 192.168.1.223    | 192.168.1.239    |

**CIDR / Block Size**

| CIDR       | /25 | /26 | /27 | /28 | /29 | /30 | /31 | /32 |
| Block Size | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |

## Subnetting Cheat Sheet
Below is a subnetting cheat sheet chart that can help you quickly identify the CIDR prefix length, decimal subnet mask, and the number of networks and addresses.

| CIDR |     |     |     | Subnet Mask | Networks | Addresses |
| ---- |     |     |     | ----------- | -------- | --------- |
| /1   | /9  | /17 | /25 | 128         | 2        | 128       |
| /2   | /10 | /18 | /26 | 192         | 4        | 64        |
| /3   | /11 | /19 | /27 | 224         | 8        | 32        |
| /4   | /12 | /20 | /28 | 240         | 16       | 16        |
| /5   | /13 | /21 | /29 | 248         | 32       | 8         |
| /6   | /14 | /22 | /30 | 252         | 64       | 4         |
| /7   | /15 | /23 | /31 | 254         | 128      | 2         |
| /8   | /16 | /24 | /32 | 255         | 256      | 1         |

## Conclusion

I hope this post helped you gain a better understanding of subnetting. Subnetting is a complex topic, and it's ok if you don't understand it the first time around. For me, it took reviewing the concept several times from different resources before it finally clicked. So, if you're struggling with subnetting, keep practicing and don't give up. Eventually, you'll have that "Aha!" moment when it clicks. Thanks for reading, and best of luck with subnetting!