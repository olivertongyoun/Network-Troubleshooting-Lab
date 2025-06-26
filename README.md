# 🧪 Network Troubleshooting Lab (Packet Tracer)

## 📘 Overview

This project simulates an enterprise-level network using Cisco Packet Tracer to explore real-world issues including:
- Routing loops
- Misconfigured IPs and subnets
- Faulty Access Control Lists (ACLs)

The goal is to understand how to identify, isolate, and fix these common networking problems through CLI configuration and testing.

---

## 🗺️ Network Topology

![Network Diagram](https://i.imgur.com/lYwhcx1.png)


- **Routing protocol:** RIP v2 or OSPF
- **IP addressing:** Manual (no DHCP)
- **ACLs:** Simulate denied traffic or restricted services

---

## 🧩 IP Addressing Scheme

| Device     | Interface       | IP Address       | Subnet Mask       |
|------------|------------------|------------------|-------------------|
| PC1        | FastEthernet0    | 192.168.10.10    | 255.255.255.0     |
| PC2        | FastEthernet0    | 192.168.20.10    | 255.255.255.0     |
| Router1    | G0/0             | 192.168.10.1     | 255.255.255.0     |
| Router1    | G0/1             | 10.10.10.1       | 255.255.255.0     |
| Router2    | G0/0             | 192.168.20.1     | 255.255.255.0     |
| Router2    | G0/1             | 10.10.10.2       | 255.255.255.0     |

---

## 🔧 Simulated Troubleshooting Scenarios

1. **Routing Loop**
   - Misconfigured RIP routing updates between routers
   - Fix by implementing `no auto-summary` and correct `network` statements

2. **IP Address Errors**
   - Incorrect IP/subnet mask on PC2 or Router2
   - Fix by verifying address plans with `ipconfig` and `show ip interface brief`

3. **ACL Misconfiguration**
   - Apply ACL to Router2 that blocks ICMP from PC1
   - Diagnose with `ping`, `traceroute`, and ACL removal or fix

---

## 🧠 What I Learned

- Diagnosing Layer 3 routing issues using CLI tools
- Analyzing ACL rules and how they impact traffic flow
- Best practices for subnetting and static IP planning
- How to visually and logically isolate errors in a multi-router setup

---

## 🧪 Sample Testing Commands

Router1# show ip route
Router2# show access-lists
PC1> ping 192.168.20.10
