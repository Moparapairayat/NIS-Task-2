# Screenshots

Screenshots are numbered in the order of the verification and testing plan (Table 9 of the design document).

## task2a-design
- `Figure2_Packet_Tracer_Topology.png` – complete topology with all links up

## task2b-installation
- `01_cabling_complete.png` – all 21 links connected
- `02_show_vlan_brief_ACC-SW1.png` – VLAN membership (Test 1)
- `03_show_interfaces_trunk_CORE-SW1.png` – trunk links and native VLAN 999 (Test 2)
- `04_show_ip_interface_brief_CORE-SW1.png` – SVIs and routed port up

## task2c-services
Main body (Figures 14–27 of the report):
- `11_dhcp_pools_SRV-DHCP-DNS.png` – DHCP pools (Figure 14)
- `12_dhcp_ADMIN-PC1.png` – address received through DHCP relay (Figure 15, Test 3)
- `13_dns_records_SRV-DHCP-DNS.png` – DNS A records (Figure 16)
- `14_web_www_college_local.png` – internal website by name (Figure 17, Test 6)
- `15_ftp_login_FAC-PC1.png` – FTP login to files.college.local (Figure 18, Test 7)
- `16_ping_by_name_ADMIN-PC1.png` – SRV-WEB and PRN1 reached by name (Figure 19, Test 4)
- `17_acl_lab_to_admin_blocked.png` – LAB-PC1 to ADMIN-PC1 blocked (Figure 20, Test 5)
- `18_show_access_lists_CORE-SW1.png` – ACL match counters (Figure 21)
- `19_ssh_ADMIN-PC1_allowed.png` – SSH from the Admin VLAN (Figure 22, Test 10)
- `20_ssh_LAB-PC1_refused.png` – SSH from the Lab VLAN refused (Figure 23)
- `21_port_security_ACC-SW3.png` – port security status (Figure 24, Test 11)
- `22_web_www_internet_test.png` – external website through NAT (Figure 25, Test 8)
- `23_nat_translations_R1-EDGE.png` – NAT table on R1-EDGE (Figure 26)
- `24_firewall_inbound_blocked.png` – inbound ping blocked by FW1 (Figure 27, Test 9)

Appendix E: `E01`–`E08`.
