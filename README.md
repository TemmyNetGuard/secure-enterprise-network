# 🔐 Secure Enterprise Network Design (Cisco Packet Tracer)

## 📌 Project Overview
This project demonstrates the design and implementation of a secure small enterprise network using Cisco Packet Tracer.  
The organization consists of three departments connected to the same switch:
- Admin (VLAN 10)
- IT (VLAN 20)
- Sales (VLAN 30)

The objective was to implement secure network segmentation, enable inter-VLAN routing, and enforce access control policies using ACLs.

---

## 🎯 Objectives
- Create VLAN segmentation for three departments
- Configure inter-VLAN routing (Router-on-a-Stick)
- Implement Access Control Lists (ACLs)
- Allow Admin access to cloud payroll system
- Restrict Sales from accessing Admin resources
- Allow IT controlled access
- Enforce secure internal segmentation
- Simulate & Demonstrate:
  - Allowed cloud access for Admin
  - Restricted access for Sales to Admin, allowed access only to IT Support
  - Secure network segmentation
  - Controlled access to cloud resources

---

## 🌐 IP Addressing Table

| Department | VLAN | Network Address | Subnet Mask | Router Subinterface |
|-----------|------|----------------|-------------|-------------------|
| Admin | VLAN 10 | 192.168.10.0 | /24 (255.255.255.0) | 192.168.10.1 |
| IT | VLAN 20 | 192.168.20.0 | /24 (255.255.255.0) | 192.168.20.1 |
| Sales | VLAN 30 | 192.168.30.0 | /24 (255.255.255.0) | 192.168.30.1 |
| Cloud | VLAN 40 | 192.168.40.0 | /24 (255.255.255.0) | 192.168.40.1 |

---

## 🏗 Network Topology

<p align="center">
  <img src="Secure Network Topology.png" width="700">
</p>

The network uses one Layer 2 switch and a router configured for inter-VLAN routing.  
All departments share the same physical switch but are logically separated using VLANs.

---

## ⚙️ Technologies Used
- Cisco Packet Tracer
- VLAN Configuration
- 802.1Q Trunking
- Inter-VLAN Routing (Router-on-a-Stick)
- Access Control Lists (ACLs)
- IP Addressing and Subnetting

---

## 🔒 Security Implementation

### VLAN Segmentation
Each department was assigned a separate VLAN:
- VLAN 10 – Admin
- VLAN 20 – IT
- VLAN 30 – Sales

This ensures logical separation of traffic within the same physical infrastructure.

**VLAN Configuration:**
<p align="center">
  <img src="show vlan brief.png" width="700">
</p>

**Naming and Assigning Ports to VLANs:**
<p align="center">
  <img src="Nameing and Assigning port to vlans.png" width="700">
</p>

---

### Inter-VLAN Routing
Router subinterfaces were configured with 802.1Q encapsulation to allow controlled communication between VLANs.

**IP Interface Brief:**
<p align="center">
  <img src="ip interface brief.png" width="700">
</p>

**Trunk Port Configuration:**
<p align="center">
  <img src="Show interface trunk.png" width="700">
</p>

---

### Access Control Lists (ACLs)
ACLs were configured to enforce traffic filtering between departments.

<p align="center">
  <img src="access list.png" width="700">
</p>

---

## 🧪 Validation & Testing

### ✅ Admin Access to Cloud (Allowed)
<p align="center">
  <img src="Restricted access to cloud.png" width="700">
</p>

Admin devices successfully access the cloud payroll system while other departments are restricted.

---

### ❌ Sales Access to Admin (Denied) | ✅ IT Access (Allowed)
<p align="center">
  <img src="Restricted access for sale to admin, allowed to IT.png" width="700">
</p>

Sales devices are restricted from accessing Admin VLAN resources while IT is permitted.

---

### ✅ IT Unrestricted Access (1)
<p align="center">
  <img src="No restrictions for IT (1).png" width="700">
</p>

---

### ✅ IT Unrestricted Access (2)
<p align="center">
  <img src="No Restriction for IT (2).png" width="700">
</p>

IT devices have the required access for support and management purposes.

---

## 🔐 Security Principles Demonstrated
- Network Segmentation
- Least Privilege
- Controlled Inter-VLAN Communication
- Internal Access Restriction
- Basic Defense-in-Depth

---

## 🚀 Skills Demonstrated
- VLAN configuration
- Trunk port configuration
- Router-on-a-stick implementation
- ACL design and application
- Network security policy enforcement
- Traffic validation and testing

---

## 📁 Project Files
- Cisco Packet Tracer (.pkt) file
- Network topology diagram
- VLAN and trunk configuration screenshots
- ACL validation screenshots

---

## 📌 Author
**TemmyNetGuard**  
Cybersecurity Learner at **Altschool Africa** | ISC2 Certified in Cybersecurity (CC)  
Building secure systems one lab at a time. 🔐
