# 🌐 Global Internet Simulation – Cisco Packet Tracer

## 📌 Project Overview

This project is a simulation of a global Internet infrastructure created using **Cisco Packet Tracer**. It includes three interconnected Autonomous Systems (AS) — Vodafone, Wind, and Google — as well as a simulated company network (*Innovate-Tech*) composed of a main LAN, a remote branch office, and a DMZ for public services.

The goal is to recreate a realistic networking environment where ISPs exchange routes via **BGP**, customers access the Internet through **CGNAT**, and internal corporate traffic is securely managed using firewalls, **NAT/PAT**, and **DHCP**.

---

## 🛠 Technologies & Protocols Used

- Cisco Routers and ASA Firewalls  
- **BGP (Border Gateway Protocol)** for global routing  
- **RIP** for internal routing distribution  
- **DHCP** with centralized relay via IP Helper  
- **PAT/NAT** for Internet access and IP translation  
- Access Control Lists (**ACLs**) for traffic filtering  
- **DMZ zone** for hosting HTTP, DNS, and SMTP services  

---

## 🧩 Topology Summary

- **Vodafone (AS12345)**: Public block `203.0.113.0/24`, CGNAT `100.64.0.0/10`  
- **Wind (AS23456)**: Public block `81.13.0.0/20`, CGNAT `100.64.0.0/10`  
- **Google (AS21345)**: Public services `8.8.8.0/24`, no CGNAT  
- **Innovate-Tech Company**:  
  - Core LAN: `192.168.1.0/24`  
  - Branch LAN: `192.168.2.0/24`  
  - DMZ Public: `78.21.2.0/24`  

Peering links between ISPs are implemented via `/30` subnets, and public services are announced by Vodafone using BGP.

---

## 🎯 Objectives

- Understand how Internet routing works between ISPs using BGP.  
- Simulate CGNAT and IP address translation mechanisms used by providers.  
- Create a secure and scalable enterprise network with branch offices.  
- Demonstrate the publication of public services via a DMZ.  
- Explore routing table exchange and network address management at global scale.  
