# Packet Tracer files

All files open in Cisco Packet Tracer 9.0.1 or later.

| File | Stage | Contents |
|---|---|---|
| `3.1-NIS-Figure 2.pkt` | Task 2a – Network design (AC 3.1) | All 22 devices placed, named and cabled (21 links) as in Figure 2 of the report, before any configuration |
| `NIS_Task2b_Installation.pkt` | Task 2b – Network installation (AC 3.2) | The same network fully installed: VLANs, trunks, SVIs, routing, firewall, NAT and static addressing of the servers and printer, with all 21 links up |
| `NIS_Task2c_Services.pkt` | Task 2c – Network services and applications (AC 3.3) | The final network: DHCP with relay, DNS, web and FTP services, inter-VLAN ACLs, SSH, port security, DHCP snooping and HTTP inspection on the firewall |

The commands used to move from the first file to the second are in [`04-device-configs/install-scripts`](../04-device-configs/install-scripts), and from the second to the third in [`04-device-configs/service-scripts`](../04-device-configs/service-scripts).

**Device passwords (lab only):** console `Con@2026`, enable `Netr0n@2026`, SSH user `admin` / `Adm1n@2026`, FTP user `faculty` / `Fac@2026`.
