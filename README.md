# Networking Labs — Cisco Packet Tracer

Hands-on Cisco networking labs covering IPv4 addressing and subnetting, switching, VLANs, routing, ACLs, firewalls, DHCP/DNS, and network troubleshooting using Cisco Packet Tracer.

## 📖 What's in here

### IP Addressing & Subnetting
- **Converting IPv4 Addresses to Binary** — binary conversion and the bitwise ANDing operation to derive network addresses, worked through with real address/subnet-mask examples
- **Implementing a Subnetted IPv4 Addressing Scheme** — designing a subnetting scheme from a single `/24` network to meet specific host-count requirements per department, configuring router and PC interfaces to match, then testing and deliberately troubleshooting a misconfigured gateway
- **General subnetting exercise**

### Switching & Layer 2
- **MAC address / MAC table exercises** — observing how switches learn and forward based on MAC addresses
- **LAN creation exercise**

### VLANs & Access Control
- **VLAN configuration** and **Homework 2** — segmenting a department-based network into VLANs with a Layer 3 core switch, trunk/access ports, inter-VLAN routing, DHCP relay, and ACLs restricting cross-department access (see full breakdown below)

### Dynamic Routing
- **Dynamic Routing Base Lab** — the same base topology configured and compared across two routing protocols: **RIPv2** and **OSPF**, plus a worked solution version

### Network Security
- **Cisco ASA firewall configuration** — configuring a dedicated ASA security appliance
- **Telnet and SSH remote access** — configuring and comparing remote device management via Telnet vs. the more secure SSH

### Quality of Service
- **QoS configuration** — traffic prioritization exercise

### Protocol Deep-Dives
- **TCP and UDP Communications** — using Packet Tracer's Simulation Mode to inspect real HTTP, FTP, DNS, and Email (SMTP/POP3) traffic PDU-by-PDU: tracing TCP flags, sequence/ACK numbers, port numbers, and multiplexing across a shared link
- **Transport Layer review (Km4.1)** — a Q&A deep-dive into TCP vs. UDP (sockets, headers, flags, the 3-way handshake, window-size flow control) and ICMP, including real `ping` and `netstat -an` command output and analysis

### Small Network Scenarios
- **Home Network build** — designing and connecting a home network (cable modem, home router, PCs, laptops, mobile devices, tablet) with Wi-Fi configuration and DHCP, laid out across physical rooms, and tracing PDU flow in Simulation Mode
- **Create a LAN** — setting up a new branch office LAN: connecting devices, DHCP for PCs alongside static addressing for a printer, and verifying connectivity and host info with `ping`, `ipconfig`, and `tracert`

### Personal Study Notes
- **Static routing notes** — self-written notes on configuring static routes between 3 routers and 5 networks, verified with `show ip route`

### Network Services
- **Homework 1 — DHCP & DNS**: two network segments connected via a router, migrated from static addressing to a DHCP server (separate pools per network), plus a DNS server with an A record so a hosted website could be reached by domain name from both segments
- **DHCP configuration from a PC** — configuring router DHCP settings from a client device
- **Web and Email server setup** — both a startup (unconfigured) and finished version, setting up hosted web and email services
- **Web Server Connectivity** — verifying end-to-end connectivity to a web server by IP, testing via ping and browser, with real troubleshooting notes
- **ARP resolution exercise**

### Homework 2 — VLAN Network Design & Security (detailed)
Designed a full department-based network for a fictional company (HR, IT, Administration, Server Room) using a star topology with a Layer 3 core switch:
- Segmented into 4 VLANs (one per department), with trunk ports between switches and the core switch, and access ports for end devices
- Enabled inter-VLAN routing with per-VLAN IP addressing
- Configured a DHCP server with **DHCP relay** (`ip helper-address`) so each VLAN could reach a centralized server
- Chose and configured **RIPv2** as the routing protocol, with reasoning based on network size
- Wrote **ACLs** enforcing department-level access rules (e.g. restricting general access to the server VLAN while granting IT full cross-VLAN access)

## 🧰 Tools & concepts used
Cisco Packet Tracer, IPv4 addressing & subnetting (binary/ANDing), static & dynamic (DHCP) addressing, DNS, VLANs, trunk/access ports, inter-VLAN routing, DHCP relay, RIPv2, OSPF, ACLs, Cisco ASA firewall, Telnet, SSH, QoS, MAC address tables/switching, TCP/UDP/ICMP protocol analysis, Wi-Fi/home networking, static routing

## 📁 What's in this repo
- `.pkt` files — Cisco Packet Tracer network topology/configuration files (open with Packet Tracer to view and interact with the simulated network)
- `.docx` files — written solutions explaining the configuration steps, calculations, and reasoning for each exercise
- `.pdf` file — personal study notes on static routing configuration

## 💡 What I learned
Practical, hands-on experience across the full range of core networking topics — from binary-level IP addressing math to designing and securing a segmented, multi-VLAN network with working routing, DHCP, DNS, and firewall configuration. Comparing routing protocols (RIPv2 vs. OSPF) on the same base topology, and deliberately troubleshooting misconfigurations, reinforced how these concepts behave in practice rather than just on paper.

---
*Coursework — Cloud and Infrastructure Specialist program, EC Utbildning.*
