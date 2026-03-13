# Cisco Packet Tracer Lab –Static NAT, Dynamic NAT , PAT Configuration and DHCP-Snooping

## Overview
This project demonstrates the configuration and verification of **Static NAT, Dynamic NAT and Port Address Translation (PAT)and DHCP Snooping** using Cisco routers in a simulated enterprise network environment.

The lab simulates an internal private network where multiple hosts access external networks through NAT translation. Three different NAT techniques are implemented to show their behavior and use cases.

Technologies demonstrated in this project are commonly used in **enterprise networks, ISPs, and corporate infrastructures**.

## Objectives

- Configure **Dynamic NAT** using an IP address pool
- Configure **PAT (NAT Overload)** for multiple hosts using a single public IP
- - Configure **Static NAT** using an IP address 
- Allow internal private network hosts to communicate with external networks
- Verify NAT translations using Cisco IOS commands

---
## Network Topology

### Internal Network
- Network: `192.168.10.0/24`
- Devices:
  - 1 Router (NAT gateway)
  - 1 Layer-2 Switch
  - 3 PCs
  - 2 DHCP Servers for DHCP SNooping Test

### External Network
- Router representing an **ISP / public network**

---

## Scenario 1 – Dynamic NAT

Dynamic NAT maps private IP addresses to a **pool of public IP addresses**.

### Public IP Pool
Dynamic NAT maps private IP addresses to a **pool of public IP addresses**.
### Public IP Pool
200.100.10.2 – 200.100.10.5

### Operation
- Internal hosts from `192.168.10.0/24` request external communication
- Router assigns an available IP from the **public IP pool**
- Each active internal host receives a temporary public address

### Key Features Demonstrated
- NAT pool creation
- Access control list for NAT matching
- Inside / outside interface configuration
- Dynamic translation table verification

---
## Scenario 2 – Port Address Translation (PAT)

PAT allows **multiple internal devices to share a single public IP address** using different port numbers.

### Public IP Used 
200.100.10.3

### Operation
- All internal hosts translate to the same public IP
- Unique **TCP/UDP port numbers** differentiate each session
- Enables efficient usage of public IP addresses

### Key Features Demonstrated
- NAT overload configuration
- Interface-based translation
- Multiple host communication through a single public IP

---

## Configuration Concepts Used

- Dynamic NAT
- PAT (NAT Overload)
- Access Control Lists (ACL)
- Inside / Outside Interface Roles
- NAT Translation Tables
- Cisco IOS NAT Verification Commands

---

## Verification Commands

Example commands used to verify configuration:

```bash
show ip nat translations
show ip nat statistics
show running-config

**Files Included**

NAT_DHCP_SNooping.png
PAT.png
Static_Nat.png
Dybamic_NAT.png

topology-pat.png



**Skills Demonstrated**

Cisco Router Configuration

Network Address Translation (NAT)

Enterprise Network Design Concepts

Packet Tracer Network Simulation

Troubleshooting Network Connectivity














