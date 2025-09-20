Credentials for lab:
login - dontsovpl
password - monday48

_______________________________________

Lab1 Project: VLAN Segmentation and Telnet Access
Objective

Configure a small network with 6 PCs and 2 Cisco 2960 switches. The network is segmented into three VLANs, and Telnet access is restricted to one VLAN.

Configuration Highlights

VLANs created for network segmentation

Telnet access restricted to one VLAN

Redundant link between switches ensures network reliability

PCs configured to connect to their respective VLANs

Demonstration

Telnet login from allowed VLAN

Ping tests between PCs in same and different VLANs

Verification of redundant link operation


________________________________________

Lab3 Project: 

Configuration Highlights

VLANs configured with dedicated subnets for X, Y, Z segments

Trunk ports between switches and routers

L3 switch configured with default route toward router 2911

Router 2911 configured with static routes toward all internal networks

PCs configured with IPs in their respective VLANs

Inter-router connectivity configured with IPs from a reserved range

Demonstration

Test connectivity between all VLANs using ping / simple PDU

Verify routing between subnets via routers

Confirm that new segment is fully integrated with the previous network

_______________________________________

Lab4 Project:

Network Overview

Replace two PCs behind the L3 switch with two servers

Add an additional router and server beyond the 2911 router (border network)

Configure public IP addresses for border network

Set up static NAT on the border router to allow external access to the web server

Configure DHCP service for client VLANs on an internal server

Use DHCP relay on the L3 switch to forward requests from clients to the DHCP server

Ensure dynamic IP assignment for client devices

Configuration Highlights

Static NAT configured with external port mapping for web server

DHCP pools created for client VLANs; server VLANs use static addressing

DHCP relay configured on L3 switch for cross-VLAN requests

Routing and VLANs maintained from previous labs

All devices tested for connectivity and proper IP assignment

Demonstration & Verification

Ping tests and Simple PDU packets to verify connectivity within and between segments

Web server access verified from the ISP-side server

DHCP clients successfully obtain dynamic IP addresses from both internal and border DHCP servers

NAT operation confirmed for external access to web server
_______________________________________

Lab5 Project:

Network Overview

Open the network from Lab 4

Rename all switches and routers using the hostname command

Remove previous static routes on routers (no ip route)

Connect routers OF01-R01 and OF02-R01 and configure dynamic routing protocol based on student ID parity:

Even → OSPF

Odd → EIGRP

Ensure all VLANs and servers maintain full connectivity

Configuration Highlights

Hostnames configured for all switches and routers for easier identification

Static inter-network routes removed and replaced with dynamic routing

Routing tables updated to allow communication between all segments

VLANs and IP addressing preserved from previous labs

Web servers and internal services tested for accessibility

Demonstration & Verification

Connectivity tests between all network segments using ICMP and Simple PDU

Web service verification on servers to ensure proper routing

Confirmation that dynamic routing propagates routes correctly across the network
_______________________________________

Lab6 Project:

Network Overview

Limit internet access from VLAN X0

Restrict external access to internal network segments

Configure Telnet access on all L3 network devices

Restrict Telnet access to router OF01-R01 from external networks only

Maintain full connectivity between internal VLANs and servers

Configuration Highlights

ACLs and firewall rules applied to restrict traffic from VLAN X0 and external networks

Telnet enabled for management, but access restricted based on source

VLANs, IP addressing, and routing preserved from previous labs

Internal testing ensured uninterrupted access for authorized users

Demonstration & Verification

Ping tests and Simple PDU packets to verify connectivity

Verification that VLAN X0 cannot access the internet

Verification that external networks cannot reach restricted internal devices

Telnet login tests confirming restricted access policies
_______________________________________

Lab7 Project:

Network Overview

Networks segmented according to student ID numbers

Class B private networks and public IPs used for WAN simulation

One VLAN per office in the LAN

Trunk lines configured between switches and routers

Hostnames and device labeling applied according to the network scheme

IPsec tunnel configured between offices for secure communication

Central office includes an additional segment with 2 servers (BBB.BBB.Z.BBB/24)

Configuration Highlights

VLANs configured for each office

Trunk ports between switches and routers for inter-VLAN routing

IPsec tunnel established for secure office-to-office communication

ACLs configured:

Server 1 → full access from all offices

Server 2 → access restricted to central office only

Routing and connectivity configured to ensure full communication between segments

Demonstration & Verification

Ping and Simple PDU packets to verify connectivity between VLANs, offices, and servers

IPsec tunnel verified for secure communication

ACLs verified to ensure restricted server access

Hostnames and labeling verified across network devices
_______________________________________

Final Lab Project: Multi-Building Corporate Network
Objective

Design and configure a corporate network spanning four office buildings with multiple VLANs, servers, and routers. Ensure proper segmentation, routing, and security, while providing internet access and VPN connectivity where required.

Network Overview
Building 1

Computers for accounting, management, and other personnel

Network printers

File server

Router: Cisco 2911

Building 2

Computers for economic department and other personnel

Network printers

File server

Router: Cisco 2911

Building 3

Computers for accounting, economic department, management, and other personnel

6 servers: accounting server, economic server, file server, web server (external access), AAA/Syslog server, DHCP server

Router: Cisco 1841

Internet connection: 100 Mbps

Building 4

Computers for management, accounting, and economic department

Network printers

File server

VPN connection to Building 3

Router: Cisco 1841

Internet connection: 100 Mbps

Configuration Highlights

VLAN segmentation for different departments and floors

Dynamic routing between buildings using OSPF or EIGRP based on student ID parity

Inter-building VPN between Buildings 3 and 4

DHCP configuration in each segment with protection against rogue servers

Access control: employees can only access servers of their department

Internet access provided to authorized users in each building

AAA server for centralized authentication to network devices

SYSLOG logging configured on network equipment

Port security and MAC spoofing protection enabled

Unused ports disabled

Network devices and servers labeled according to a standardized scheme

Demonstration & Verification

Connectivity tests between VLANs and buildings using ICMP (ping) and test PDU packets

Internet access verified for authorized users

VPN tunnel tested for secure inter-building connectivity

Access restrictions verified per department and server

Routing tables and dynamic routing protocols verified on routers

Redundancy and failover tested via ring topology


