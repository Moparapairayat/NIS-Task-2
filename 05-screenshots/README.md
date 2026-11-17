# Evidence screenshots

Every screenshot used in the report, named by its figure number and grouped by stage. Red boxes in each image highlight the lines that prove the result. Test numbers refer to the verification plan in Table 9 of the report.

| Folder | Stage | Count | Report location |
|---|---|---|---|
| [`task2a-design`](task2a-design) | Task 2a – Design (AC 3.1) | 1 | Figure 2 |
| [`task2b-installation`](task2b-installation) | Task 2b – Installation (AC 3.2) | 30 | Figures 4–13, Appendix D |
| [`task2c-services`](task2c-services) | Task 2c – Services (AC 3.3) | 22 | Figures 14–27, Appendix E |

---

## Task 2a – Design

| Figure | File | Shows |
|---|---|---|
| 2 | [`Packet-Tracer -Figure-2-a.png`](task2a-design/Packet-Tracer%20-Figure-2-a.png) | All 22 devices placed, named and cabled in Packet Tracer |

---

## Task 2b – Installation

### Main body (Sections 15–19)

| Figure | File | Shows | Test |
|---|---|---|---|
| 4 | [`01_topology_all_links_up.png`](task2b-installation/01_topology_all_links_up.png) | Topology with all 21 links up | – |
| 5 | [`02_login_banner_CORE-SW1.png`](task2b-installation/02_login_banner_CORE-SW1.png) | Warning banner and password prompt on CORE-SW1 | – |
| 6 | [`03_show_vlan_brief_ACC-SW1.png`](task2b-installation/03_show_vlan_brief_ACC-SW1.png) | Access ports in VLAN 10, unused ports in VLAN 998 | 1 |
| 7 | [`04_show_interfaces_trunk_CORE-SW1.png`](task2b-installation/04_show_interfaces_trunk_CORE-SW1.png) | Four trunks, native VLAN 999, pruned VLANs | 2 |
| 8 | [`05_show_ip_int_brief_CORE-SW1.png`](task2b-installation/05_show_ip_int_brief_CORE-SW1.png) | SVIs and routed port up | – |
| 9 | [`06_show_ip_route_R1-EDGE.png`](task2b-installation/06_show_ip_route_R1-EDGE.png) | Default route and route to the campus | – |
| 10 | [`07_FW1_interfaces_and_routes.png`](task2b-installation/07_FW1_interfaces_and_routes.png) | Inside and outside interfaces and static routes | – |
| 11 | [`08_ping_core_to_fw_servers_printer.png`](task2b-installation/08_ping_core_to_fw_servers_printer.png) | Core reaches FW1, servers and printer | – |
| 12 | [`09_ping_SRV-WEB_to_internet.png`](task2b-installation/09_ping_SRV-WEB_to_internet.png) | End-to-end ping to INTERNET-SRV | – |
| 13 | [`10_nat_translations_R1-EDGE.png`](task2b-installation/10_nat_translations_R1-EDGE.png) | PAT translation for SRV-WEB | – |

### Appendix D

| Figure | File | Shows | Test |
|---|---|---|---|
| D1 | [`D01_ISP-R_ip_int_brief.png`](task2b-installation/D01_ISP-R_ip_int_brief.png) | ISP-R interfaces | – |
| D2 | [`D02_ISP-R_ping_internet_srv.png`](task2b-installation/D02_ISP-R_ping_internet_srv.png) | ISP-R to INTERNET-SRV | – |
| D3 | [`D03_R1-EDGE_ip_int_brief.png`](task2b-installation/D03_R1-EDGE_ip_int_brief.png) | R1-EDGE interfaces | – |
| D4 | [`D04_R1-EDGE_ping_ISP-R.png`](task2b-installation/D04_R1-EDGE_ping_ISP-R.png) | R1-EDGE to ISP-R | – |
| D5 | [`D05_FW1_ping_R1-EDGE.png`](task2b-installation/D05_FW1_ping_R1-EDGE.png) | FW1 to R1-EDGE | – |
| D6 | [`D06_CORE-SW1_show_vlan_brief.png`](task2b-installation/D06_CORE-SW1_show_vlan_brief.png) | Core VLANs, printer port in VLAN 50 | 1 |
| D7 | [`D07_CORE-SW1_show_ip_route.png`](task2b-installation/D07_CORE-SW1_show_ip_route.png) | Core routing table | – |
| D8 | [`D08_CORE-SW1_stp_root.png`](task2b-installation/D08_CORE-SW1_stp_root.png) | CORE-SW1 is the STP root | – |
| D9 | [`D09_ACC-SW1_trunk_mgmt_ping.png`](task2b-installation/D09_ACC-SW1_trunk_mgmt_ping.png) | ACC-SW1 trunk and management ping | 2 |
| D10 | [`D10_ACC-SW2_show_vlan_brief.png`](task2b-installation/D10_ACC-SW2_show_vlan_brief.png) | ACC-SW2 VLANs | 1 |
| D11 | [`D11_ACC-SW2_trunk_mgmt_ping.png`](task2b-installation/D11_ACC-SW2_trunk_mgmt_ping.png) | ACC-SW2 trunk and management ping | 2 |
| D12 | [`D12_ACC-SW3_show_vlan_brief.png`](task2b-installation/D12_ACC-SW3_show_vlan_brief.png) | ACC-SW3 VLANs | 1 |
| D13 | [`D13_ACC-SW3_trunk_mgmt_ping.png`](task2b-installation/D13_ACC-SW3_trunk_mgmt_ping.png) | ACC-SW3 trunk and management ping | 2 |
| D14 | [`D14_SRV-SW1_show_vlan_brief.png`](task2b-installation/D14_SRV-SW1_show_vlan_brief.png) | SRV-SW1 VLANs | 1 |
| D15 | [`D15_SRV-SW1_trunk_mgmt_ping.png`](task2b-installation/D15_SRV-SW1_trunk_mgmt_ping.png) | SRV-SW1 trunk and management ping | 2 |
| D16 | [`D16_SRV-DHCP-DNS_ipconfig.png`](task2b-installation/D16_SRV-DHCP-DNS_ipconfig.png) | SRV-DHCP-DNS addressing | – |
| D17 | [`D17_SRV-FILE_ipconfig.png`](task2b-installation/D17_SRV-FILE_ipconfig.png) | SRV-FILE addressing | – |
| D18 | [`D18_SRV-WEB_ipconfig.png`](task2b-installation/D18_SRV-WEB_ipconfig.png) | SRV-WEB addressing | – |
| D19 | [`D19_INTERNET-SRV_ipconfig.png`](task2b-installation/D19_INTERNET-SRV_ipconfig.png) | INTERNET-SRV addressing | – |
| D20 | [`D20_PRN1_ip_settings.png`](task2b-installation/D20_PRN1_ip_settings.png) | PRN1 static address | – |

---

## Task 2c – Services and applications

### Main body (Sections 21–26)

| Figure | File | Shows | Test |
|---|---|---|---|
| 14 | [`11_dhcp_pools_SRV-DHCP-DNS.png`](task2c-services/11_dhcp_pools_SRV-DHCP-DNS.png) | DHCP pools for VLANs 10, 20 and 30 | – |
| 15 | [`12_dhcp_ADMIN-PC1.png`](task2c-services/12_dhcp_ADMIN-PC1.png) | ADMIN-PC1 address through DHCP relay | 3 |
| 16 | [`13_dns_records_SRV-DHCP-DNS.png`](task2c-services/13_dns_records_SRV-DHCP-DNS.png) | DNS A records | – |
| 17 | [`14_web_www_college_local.png`](task2c-services/14_web_www_college_local.png) | Internal website by name | 6 |
| 18 | [`15_ftp_login_FAC-PC1.png`](task2c-services/15_ftp_login_FAC-PC1.png) | FTP login to files.college.local | 7 |
| 19 | [`16_ping_by_name_ADMIN-PC1.png`](task2c-services/16_ping_by_name_ADMIN-PC1.png) | SRV-WEB and PRN1 reached by name | 4 |
| 20 | [`17_acl_lab_to_admin_blocked.png`](task2c-services/17_acl_lab_to_admin_blocked.png) | LAB-PC1 to ADMIN-PC1 blocked | 5 |
| 21 | [`18_show_access_lists_CORE-SW1.png`](task2c-services/18_show_access_lists_CORE-SW1.png) | ACLs with match counters | 5 |
| 22 | [`19_ssh_ADMIN-PC1_allowed.png`](task2c-services/19_ssh_ADMIN-PC1_allowed.png) | SSH from the Admin VLAN | 10 |
| 23 | [`20_ssh_LAB-PC1_refused.png`](task2c-services/20_ssh_LAB-PC1_refused.png) | SSH from the Lab VLAN refused | 10 |
| 24 | [`21_port_security_ACC-SW3.png`](task2c-services/21_port_security_ACC-SW3.png) | Port security with sticky MAC | 11 |
| 25 | [`22_web_www_internet_test.png`](task2c-services/22_web_www_internet_test.png) | External website through NAT | 8 |
| 26 | [`23_nat_translations_R1-EDGE.png`](task2c-services/23_nat_translations_R1-EDGE.png) | PAT translations for ADMIN-PC1 | 8 |
| 27 | [`24_firewall_inbound_blocked.png`](task2c-services/24_firewall_inbound_blocked.png) | Inbound ping blocked by FW1 | 9 |

### Appendix E

| Figure | File | Shows | Test |
|---|---|---|---|
| E1 | [`E01_dhcp_FAC-PC1.png`](task2c-services/E01_dhcp_FAC-PC1.png) | FAC-PC1 address through DHCP | 3 |
| E2 | [`E02_dhcp_LAB-PC1.png`](task2c-services/E02_dhcp_LAB-PC1.png) | LAB-PC1 address through DHCP with LAB-IN applied | 3 |
| E3 | [`E03_lab_web_allowed.png`](task2c-services/E03_lab_web_allowed.png) | Lab can still open the internal website | 5 |
| E4 | [`E04_faculty_to_admin_blocked.png`](task2c-services/E04_faculty_to_admin_blocked.png) | FAC-PC1 to ADMIN-PC1 blocked | 5 |
| E5 | [`E05_lab_to_printer_blocked.png`](task2c-services/E05_lab_to_printer_blocked.png) | LAB-PC1 to PRN1 blocked | 5 |
| E6 | [`E06_ftp_users_SRV-FILE.png`](task2c-services/E06_ftp_users_SRV-FILE.png) | Only the faculty FTP account remains | 7 |
| E7 | [`E07_dhcp_snooping_ACC-SW1.png`](task2c-services/E07_dhcp_snooping_ACC-SW1.png) | DHCP snooping with trusted uplink | 11 |
| E8 | [`E08_show_ip_ssh_CORE-SW1.png`](task2c-services/E08_show_ip_ssh_CORE-SW1.png) | SSH version 2 enabled | 10 |
