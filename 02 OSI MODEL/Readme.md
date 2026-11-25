# Day 2 — OSI Model Lab

## Overview

This lab focuses on understanding the OSI Model and analyzing network traffic using Cisco Packet Tracer Simulation Mode.

## Objectives

- Analyze network traffic using Simulation Mode
- Identify OSI layers involved in network communication
- Inspect ICMP packet details
- Observe how a switch receives and forwards Ethernet frames
- Release and renew PC1's IP address using DHCP
- Observe DHCP events in the Simulation Event List
- Verify connectivity using ping

## Network Topology

The topology includes:

- 1 Server — SRV1
- 1 PC — PC1
- 2 Cisco 2960 switches — SW1 and SW2
- 2 Cisco ISR4331 routers — R1 and R2

## IP Addressing

### LAN Network — 192.168.1.0/24

| Device | Interface | IP Address |
|---|---|---|
| SRV1 | Fa0 | 192.168.1.100 |
| R1 | Gi0/0/0 | 192.168.1.1 |
| PC1 | Fa0 | DHCP |

### Router-to-Router Network — 10.0.0.0/24

| Device | Interface | IP Address |
|---|---|---|
| R1 | Gi0/0/1 | 10.0.0.1 |
| R2 | Gi0/0/0 | 10.0.0.2 |

## Lab Activities

### 1. ICMP Traffic Analysis

Generated ICMP traffic from PC1 to SRV1 and observed packet movement through the network in Simulation Mode.

### 2. Inbound PDU Details at SW2

Inspected the inbound PDU and observed the ICMP Echo Request.

- Source IP: 192.168.1.2
- Destination IP: 192.168.1.100
- ICMP Type: Echo Request

### 3. OSI Model at SW2

Observed SW2 receiving an Ethernet frame on FastEthernet0/1 and forwarding it through FastEthernet0/2 toward SW1.

### 4. DHCP Release and Renew

Used the following commands on PC1:

```text
ipconfig /release
ipconfig /renew
```

Observed DHCP traffic in Simulation Mode.

### 5. Connectivity Verification

Tested connectivity between PC1 and SRV1 using:

```text
ping 192.168.1.100
```

The final ping test completed successfully with 4 packets sent, 4 received, and 0% packet loss.

## Screenshots

The Screenshots folder contains the following lab evidence:

1. Network Topology
2. ICMP Simulation Events
3. ICMP Inbound PDU Details at SW2
4. OSI Model at SW2
5. DHCP Release and Renew
6. DHCP Simulation Events
7. Successful Ping Test
8. PC1 IP Configuration

## Tools Used

- Cisco Packet Tracer
- Cisco ISR4331 Routers
- Cisco 2960 Switches

## Lab File

`02-OSI-Model-Lab.pkt`

This lab is part of my CCNA Networking Labs learning series.
