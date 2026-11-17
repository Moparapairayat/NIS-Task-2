# Packet Tracer files

The network is provided as one file per stage, so each part of Task 2 can be opened and checked on its own. All files open in **Cisco Packet Tracer 9.0.1 or later**.

| File | Stage | State of the network | How it was produced |
|---|---|---|---|
| [`3.1-NIS-Figure 2.pkt`](3.1-NIS-Figure%202.pkt) | Task 2a – Design (AC 3.1) | All 22 devices placed, named and cabled with 21 links, before any configuration (Figure 2) | Built by hand from Table 5 of the report |
| [`NIS_Task2b_Installation.pkt`](NIS_Task2b_Installation.pkt) | Task 2b – Installation (AC 3.2) | VLANs, trunks, SVIs, static routing, firewall, NAT and static server addressing; all 21 links up | Previous file + [`install-scripts`](../04-device-configs/install-scripts) |
| [`NIS_Task2c_Services.pkt`](NIS_Task2c_Services.pkt) | Task 2c – Services (AC 3.3) | Final network: DHCP with relay, DNS, web, FTP, inter-VLAN ACLs, SSH, port security, DHCP snooping and firewall HTTP inspection | Previous file + [`service-scripts`](../04-device-configs/service-scripts) |

## Quick checks in the final file

| Check | Where | Command or action | Expected result |
|---|---|---|---|
| Addressing | Any PC › Command Prompt | `ipconfig /all` | Address from the VLAN's DHCP pool, DHCP server 192.168.40.10 |
| Name resolution and routing | ADMIN-PC1 › Command Prompt | `ping www.college.local` | Replies from 192.168.40.30 |
| Internal website | Any PC › Web Browser | `http://www.college.local` | Netron College Intranet page |
| Internet and NAT | ADMIN-PC1 › Web Browser | `http://www.internet.test` | External Test Website page |
| Access control | LAB-PC1 › Command Prompt | `ping 192.168.10.10` | Destination host unreachable |
| Secure management | ADMIN-PC1 › Command Prompt | `ssh -l admin 192.168.99.1` | `CORE-SW1#` prompt |
| Firewall | R1-EDGE › CLI | `ping 192.168.40.30` | Success rate 0 percent |

The first ping or page load after opening the file may time out while devices learn each other's addresses; repeat it once.

## Lab credentials

| Purpose | Credential |
|---|---|
| Console password (IOS devices) | `Con@2026` |
| Enable secret (IOS) / enable password (ASA) | `Netr0n@2026` |
| SSH | user `admin`, password `Adm1n@2026` |
| FTP on SRV-FILE | user `faculty`, password `Fac@2026` |

These credentials exist only in the simulation.
