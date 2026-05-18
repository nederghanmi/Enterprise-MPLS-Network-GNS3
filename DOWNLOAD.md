# 📦 Full GNS3 Project Download

Due to GitHub file size limitations, the complete GNS3 lab environment is hosted externally.

## 🔗 Download Link

👉 https://drive.google.com/file/d/1XsA-WRe6veUy8EwdyIgEGmyu6-M79uBk/view?usp=sharing

---

# 📁 Included Content

The archive contains:

* Full GNS3 project (.gns3)
* Complete router, switch and firewall configurations
* MPLS L3VPN backbone topology
* ASA Active/Standby Failover setup
* DMZ infrastructure
* Zabbix monitoring environment
* AAA / FreeRADIUS integration
* Verification and testing outputs

---

# 🖥️ Lab Environment

## Router Images

* Cisco 7200

## Switch Images

* Cisco IOU L2
* IOSv-L2

## Security

* Cisco ASA Firewall

## Servers

* Ubuntu Server
* Zabbix Appliance

⚠️ Cisco images are NOT included in the repository and must be obtained separately.

---

# ⚙️ Requirements

* GNS3 (latest version recommended)
* VMware Workstation
* Cisco router/switch/firewall images
* Basic knowledge of:

  * MPLS
  * OSPF
  * BGP
  * VLANs
  * Network Security

---

# 🚀 How to Run the Lab

1. Download the project archive
2. Import the `.gns3` project into GNS3
3. Configure required Cisco images
4. Start VMware VMs if needed
5. Power on all devices
6. Verify:

   * OSPF neighbors
   * MPLS LDP
   * MP-BGP VPNv4
   * HSRP
   * ASA Failover
   * DMZ connectivity

---

# 🧪 Recommended Verification Commands

## MPLS

```cisco
show mpls ldp neighbor
```

## OSPF

```cisco
show ip ospf neighbor
```

## BGP VPNv4

```cisco
show ip bgp vpnv4 all summary
```

## HSRP

```cisco
show standby brief
```

## EtherChannel

```cisco
show etherchannel summary
```

## ASA Failover

```cisco
show failover
```

---

# 📌 Notes

* Ensure all interfaces are enabled (`no shutdown`)
* Verify OSPF neighbors are in FULL state
* Confirm MPLS and BGP sessions before end-to-end testing
* Some VMware/GNS3 adapter adjustments may be required depending on your environment

For full architecture details, explanations and implementation steps, refer to the main `README.md`.
