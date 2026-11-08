# Network Information Systems – Task 2: Campus Network Design and Implementation

**OTHM Level 5 · Unit: Network Information Systems (R/617/2272) · Learning Outcome 3**

This repository contains the supporting files for Task 2: the network design (AC 3.1), the Cisco Packet Tracer build (AC 3.2) and the configuration of network services and applications (AC 3.3) for a small college campus network, prepared as part of the Netron plc graduate training scenario.

## Repository structure

```
NIS-Task-2/
├── README.md                     This file
├── 01-design-document/           Task 2(a) design document (PDF)
├── 02-diagrams/                  Figure 1 and Figure 3 (.drawio source and .png)
├── 03-packet-tracer/             Complete network (.pkt, Cisco Packet Tracer 9.0.1)
├── 04-device-configs/            Running configuration of every network device
├── 05-screenshots/
│   ├── task2a-design/            Figure 2 – Packet Tracer topology
│   ├── task2b-installation/      Cabling, VLAN and trunk verification
│   └── task2c-services/          DHCP, DNS, web, FTP, NAT, ACL and SSH tests
└── 06-video/                     Links to the demonstration video
```

## Network at a glance

| Item | Details |
|---|---|
| Topology | Hierarchical collapsed-core design (one Layer 3 core, four access switches) |
| Devices | 2 × Cisco 2911, 1 × Cisco ASA 5506-X, 1 × Cisco 3560-24PS, 4 × Cisco 2960-24TT, 9 PCs, 4 servers, 1 printer |
| Links | 21 copper links (7 cross-over, 14 straight-through) |
| Routing | Static routing; PAT (NAT overload) on R1-EDGE |
| Services | DHCP with relay, DNS (college.local), HTTP, FTP, network printing |
| Security | ASA firewall, inter-VLAN ACLs, port security, DHCP snooping, BPDU Guard, SSH v2 |

## VLANs and subnets

| VLAN | Name | Subnet | Gateway |
|---|---|---|---|
| 10 | ADMIN | 192.168.10.0/24 | 192.168.10.1 |
| 20 | FACULTY | 192.168.20.0/24 | 192.168.20.1 |
| 30 | LAB | 192.168.30.0/24 | 192.168.30.1 |
| 40 | SERVERS | 192.168.40.0/24 | 192.168.40.1 |
| 50 | PRINTERS | 192.168.50.0/24 | 192.168.50.1 |
| 99 | MANAGEMENT | 192.168.99.0/24 | 192.168.99.1 |
| 998 | BLACKHOLE | Unused ports (shut down) | – |
| 999 | NATIVE | Native VLAN on trunks | – |

## How to open the files

- **Packet Tracer file (.pkt):** open with Cisco Packet Tracer 9.0.1 or later (free with a Cisco Networking Academy account).
- **Diagrams (.drawio):** open at [app.diagrams.net](https://app.diagrams.net) using *File > Open from > Device*, or use the live links below.

## Live diagrams

- Figure 1 – Logical topology: [View in draw.io](https://app.diagrams.net/#Uhttps://raw.githubusercontent.com/Moparapairayat/NIS-Task-2/main/02-diagrams/Figure1_Logical_Topology.drawio)
- Figure 3 – Physical topology and port connections: [View in draw.io](https://app.diagrams.net/#Uhttps://raw.githubusercontent.com/Moparapairayat/NIS-Task-2/main/02-diagrams/Figure3_Physical_Topology.drawio)

## Demonstration video

- [View on YouTube](ADD-LINK-HERE)
- [View on Google Drive](ADD-LINK-HERE)

## Author

[Your name] · [Learner ID] · [Centre name] · November 2026
