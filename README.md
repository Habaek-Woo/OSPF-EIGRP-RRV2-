# OSPF-EIGRP-RRV2-
# Cisco Packet Tracer: Topology Project

## 📌 Project Overview
**Objective:** [Briefly describe the goal of this topology, e.g., "Design a multi-branch enterprise network with redundant routing and segmented VLANs."]
**Packet Tracer Version:** [e.g., 8.2.1]

## 🏗️ Topology Architecture
[Provide a high-level summary of the network design. Explain how the different branches or segments are connected.]

### Key Technologies Implemented
* **Routing Protocols:** [e.g., OSPFv2, EIGRP, Static Routing]
* **Switching:** [e.g., VLANs, Trunking (802.1Q), STP, VTP]
* **Security:** [e.g., Standard/Extended ACLs, Port Security]
* **Services:** [e.g., DHCP, NAT/PAT, DNS, HTTP]

## 📊 IP Addressing Table
| Device Name | Interface | IP Address | Subnet Mask | Default Gateway |
|-------------|-----------|------------|-------------|-----------------|
| R1-HQ       | G0/0      | 192.168.1.1| 255.255.255.0| N/A             |
| S1-Core     | VLAN 10   | 192.168.10.2| 255.255.255.0| 192.168.10.1    |
| PC-Admin    | NIC       | DHCP       | DHCP        | DHCP            |
*(Expand this table based on your topology)*

## ⚙️ Configuration Details
### VLAN Assignments
* **VLAN 10:** Management (192.168.10.0/24)
* **VLAN 20:** HR (192.168.20.0/24)
* **VLAN 30:** IT (192.168.30.0/24)

### Routing 
* [Explain the routing setup, e.g., "OSPF Area 0 is configured on all core routers to ensure dynamic reachability across the enterprise backbone."]

## 🚀 How to Test the Network
To verify that the topology is functioning as intended, perform the following tests in Packet Tracer:
1. **End-to-End Connectivity:** Open the Command Prompt on `PC-1` and `ping [Target IP]`. The ping should be successful.
2. **DHCP Verification:** Check the IP configuration on any client PC. It should successfully receive an IP address from the DHCP server.
3. **Routing Verification:** Run `show ip route` on the Core Router to verify that all remote subnets have been learned dynamically.

## ⚠️ Known Issues / Limitations
* [Document any bugs or incomplete configurations, e.g., "PC-3 currently cannot reach the web server due to an unresolved ACL dropping port 80 traffic."]

## 🏗️ Topology Architecture

Below is the visual documentation of the network design implemented in Cisco Packet Tracer.

### 1. Main Enterprise Topology
This image provides a high-level overview of the entire network infrastructure. It illustrates the core routing backbone and how the distinct sites—such as the main headquarters, server farm, and remote branches—are interconnected to facilitate enterprise-wide communication.

![Main Enterprise Topology](images_EIGRP,RRV2,OSPF.png)

### 2. Detailed Branch/Department View
This image offers a zoomed-in, detailed view of a specific local area network (LAN) segment. It highlights the distribution and access layers, showcasing the connectivity for various end devices including workstations, IP phones (VoIP), and a wireless access point handling mobile traffic.

![Detailed Branch/Department View](image_Topology.png)
