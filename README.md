# 🚀 Enterprise MPLS L3VPN & Security Infrastructure (GNS3 Lab)

## 📌 Project Description

This project demonstrates the implementation of a complete Enterprise MPLS Layer 3 VPN (L3VPN) and Security Infrastructure using GNS3, VMware and Cisco technologies.

The environment simulates a real-world Service Provider backbone delivering secure connectivity between multiple customer sites (HQ and Branches) with high availability, redundancy, segmentation, monitoring and centralized security services.

---

# 🧠 Core Technologies Implemented

## 🔹 MPLS Backbone

* MPLS (LDP)
* MP-BGP VPNv4
* VRF Segmentation
* OSPF Multi-Area Routing
* PE / P Architecture

## 🔹 Switching & High Availability

* VLAN Segmentation
* Inter-VLAN Routing
* HSRP Redundancy
* EtherChannel Aggregation
* DHCP Services

## 🔹 Security Infrastructure

* Cisco ASA Firewalls
* Active/Standby Failover
* DMZ Architecture
* ACL Security Policies
* Secure Administrative Access

## 🔹 Enterprise Services

* WWW Server
* DNS Server
* SMTP Mail Server
* Ubuntu DMZ Server

## 🔹 Monitoring & AAA

* Zabbix Monitoring Server
* SNMPv3 Secure Monitoring
* FreeRADIUS AAA Authentication

## 🔹 Intrusion Prevention

* IPS / Threat Detection Integration

---

# 🌐 Architecture Overview

## 🔸 Provider Backbone

Routers:

* P1
* P2
* PE1
* PE2

Features:

* OSPF Area 0
* MPLS forwarding
* LDP label distribution
* MP-BGP VPNv4 route exchange

---

# 🔐 VPN Layer

## VRF Configuration

VRF:

```text
VPN_CYBER
```

Route Distinguisher:

```text
100:3
```

Route Target:

```text
100:3
```

BGP Autonomous System:

```text
AS 100
```

---

# 🏢 Headquarters (Siège)

## VLANs

* VLAN 10 → 172.16.210.0/24
* VLAN 15 → 172.16.215.0/24
* VLAN 20 → 172.16.220.0/24

## Features

* Inter-VLAN Routing
* HSRP Redundancy
* EtherChannel
* DHCP Services
* AAA Authentication
* SNMPv3 Monitoring

---

# 🌍 Branch1

## Networks

* VLAN 201 → 172.16.201.0/24
* VLAN 202 → 172.16.202.0/24

## Features

* Router-on-a-Stick
* DHCP
* OSPF with PE router

---

# 🌍 Branch2

## Networks

* VLAN 203 → 172.16.203.0/24
* VLAN 204 → 172.16.204.0/24

---

# 🛡️ Security & DMZ Architecture

## ASA Failover

The infrastructure includes two Cisco ASA Firewalls configured in:

```text
Active / Standby Failover
```

Features:

* Stateful Failover
* Redundant Security Gateway
* DMZ Protection
* Traffic Filtering
* Secure Segmentation

---

# 🌐 DMZ Zone

## DMZ Network

```text
172.16.255.0/25
```

## Hosted Services

* WWW
* DNS
* SMTP

The DMZ is connected redundantly to both ASA firewalls to ensure high availability and service continuity.

---

# 📊 Monitoring Infrastructure

## Zabbix

* SNMPv3 secure monitoring
* Device supervision
* Traffic & health monitoring
* Alerting capabilities

---

# 🔑 AAA Infrastructure

## FreeRADIUS

Implemented centralized authentication for administrative access and secure device management.

---

# 🧪 VERIFICATION RESULTS

## MPLS & BGP

```cisco
show ip bgp vpnv4 all summary
```

✔ VPNv4 sessions established successfully

---

## OSPF

```cisco
show ip ospf neighbor
```

✔ All neighbors in FULL state

---

## MPLS LDP

```cisco
show mpls ldp neighbor
```

✔ MPLS core operational

---

## HSRP

```cisco
show standby brief
```

✔ Gateway redundancy operational

---

## EtherChannel

```cisco
show etherchannel summary
```

✔ Link aggregation operational

---

## ASA Failover

```cisco
show failover
```

✔ Active/Standby synchronization operational

---

# 🧪 End-to-End Validation

✔ HQ ↔ Branch1 Connectivity
✔ HQ ↔ Branch2 Connectivity
✔ MPLS VPN Reachability
✔ DMZ Services Reachability
✔ Redundancy Validation
✔ Failover Validation
✔ Monitoring & AAA Functional

---

# ⚠️ Troubleshooting & Real-World Fixes

During the project, several complex infrastructure issues were identified and resolved:

* OSPF adjacency stuck in EXSTART
* MPLS route propagation issues
* VRF route redistribution problems
* VLAN / trunk inconsistencies
* HSRP synchronization issues
* VMware / GNS3 adapter conflicts
* ASA failover synchronization problems
* DMZ Layer2 connectivity debugging
* SNMPv3 & AAA integration troubleshooting

---

# 🛠️ Technologies Used

* MPLS (LDP)
* MP-BGP VPNv4
* OSPF
* VRF (L3VPN)
* VLANs (802.1Q)
* HSRP
* EtherChannel
* Cisco ASA
* ACLs
* DMZ
* SNMPv3
* Zabbix
* FreeRADIUS
* IPS
* DHCP
* GNS3
* VMware
* Ubuntu Server

---

# 🎯 Skills Demonstrated

* Enterprise Network Design
* MPLS L3VPN Deployment
* Advanced Routing & Switching
* High Availability Architectures
* Enterprise Security Integration
* Firewall Redundancy
* DMZ Implementation
* Monitoring & AAA Deployment
* Infrastructure Troubleshooting
* Network Security Engineering

---

# 👨‍💻 Author

Neder Ghanmi
