# Lab 03: Network Devices and Inter-LAN Routing

## Overview
This lab demonstrates how network devices connect computers and how a router enables communication between two different LANs using Cisco Packet Tracer.

## Devices Used
- 1 Cisco 1941 Router
- 2 Cisco 2960 Switches
- 4 PCs

## Network Addressing

### LAN 1
Network: `192.168.1.0/24`  
Default Gateway: `192.168.1.1`

| PC | IP Address |
|---|---|
| PC1 | 192.168.1.10 |
| PC2 | 192.168.1.2 |

### LAN 2
Network: `192.168.2.0/24`  
Default Gateway: `192.168.2.1`

| PC | IP Address |
|---|---|
| PC3 | 192.168.2.10 |
| PC4 | 192.168.2.2 |

Subnet mask for all PCs: `255.255.255.0`

## Router Configuration
- GigabitEthernet0/0: `192.168.1.1/24`
- GigabitEthernet0/1: `192.168.2.1/24`
- Enabled router interfaces using `no shutdown`

## Practical Tasks
- Built a topology with two LANs.
- Configured static IPv4 addresses on all PCs.
- Configured router interfaces.
- Verified interface status using `show ip interface brief`.
- Tested connectivity within the LAN.
- Tested communication between LANs using ICMP ping.

## Verification
Successful ping tests were performed:
- PC1 to its gateway: `192.168.1.1`
- PC1 to PC3: `192.168.2.10`

Both tests completed with 0% packet loss.

## Key Learnings
- Switches connect devices within a LAN.
- Routers connect different IP networks.
- Default gateways are required to reach remote networks.
- Router interfaces must be configured and enabled.

## Status
Completed

## Next Lab
Lab 04 – Network Interfaces and Cables
