# Device configurations

Every command applied to the network is stored here as a plain-text script, one file per device, in the order it was applied. Together with the Packet Tracer files they make the build fully reproducible.

| Folder | Stage | Contents |
|---|---|---|
| [`install-scripts/`](install-scripts) | Task 2b – Installation (AC 3.2) | Basic hardening, VLANs, trunks, SVIs, routing, firewall and NAT for all eight network devices, plus static server addressing |
| [`service-scripts/`](service-scripts) | Task 2c – Services (AC 3.3) | Server services, DHCP relay, inter-VLAN ACLs, SSH, port security, DHCP snooping and firewall HTTP inspection |
| [`running-configs/`](running-configs) | Final state | `show running-config` output of each device |

## How to apply a script

1. Open the device in Cisco Packet Tracer and go to the **CLI** tab.
2. Press Enter. On a fresh router, answer `no` to the initial configuration dialog.
3. Paste the whole file. Lines beginning with `!` are comments and are ignored by IOS.
4. Run the `show` and `ping` commands listed at the end of the file to verify the result.

Service scripts assume the matching install script has already been applied. On an already configured device, log in first (console `Con@2026`, `enable` with `Netr0n@2026`) and paste from `configure terminal`.

---

## Install scripts – Task 2b

The access layer is configured first so that every trunk is ready when the core comes up; the firewall, edge router and ISP then follow from the inside outwards.

| Order | File | Device | Model | Main configuration |
|---|---|---|---|---|
| 1 | [`01_ACC-SW1.txt`](install-scripts/01_ACC-SW1.txt) | Admin access switch | Cisco 2960-24TT | VLAN 10 ports, trunk, management SVI .99.11 |
| 2 | [`02_ACC-SW2.txt`](install-scripts/02_ACC-SW2.txt) | Faculty access switch | Cisco 2960-24TT | VLAN 20 ports, trunk, management SVI .99.12 |
| 3 | [`03_ACC-SW3.txt`](install-scripts/03_ACC-SW3.txt) | Computer lab access switch | Cisco 2960-24TT | VLAN 30 ports, trunk, management SVI .99.13 |
| 4 | [`04_SRV-SW1.txt`](install-scripts/04_SRV-SW1.txt) | Server access switch | Cisco 2960-24TT | VLAN 40 ports, trunk, management SVI .99.14 |
| 5 | [`05_CORE-SW1.txt`](install-scripts/05_CORE-SW1.txt) | Layer 3 core switch | Cisco 3560-24PS | All VLANs, four trunks, six SVIs, routed port, default route, STP root |
| 6 | [`06_FW1.txt`](install-scripts/06_FW1.txt) | Firewall | Cisco ASA 5506-X | Inside and outside zones, static routes, ICMP inspection |
| 7 | [`07_R1-EDGE.txt`](install-scripts/07_R1-EDGE.txt) | Edge router | Cisco 2911 | Interfaces, static routes, PAT |
| 8 | [`08_ISP-R.txt`](install-scripts/08_ISP-R.txt) | Simulated ISP router | Cisco 2911 | WAN and internet-side interfaces |
| 9 | [`09_servers_and_printer_IP.md`](install-scripts/09_servers_and_printer_IP.md) | Servers and PRN1 | – | Static addresses set in the GUI |

| Script | Explained in report | Evidence |
|---|---|---|
| Basic setup block (all IOS devices) | Section 16 | Figures 4–5 |
| `01`–`04` access switches | Section 17 | Figure 6, Figures D9–D15 |
| `05_CORE-SW1.txt` | Sections 17–18 | Figures 7, 8, 11, Figures D6–D8 |
| `06_FW1.txt` | Section 18 | Figure 10, Figure D5 |
| `07_R1-EDGE.txt` | Section 18 | Figures 9, 13, Figures D3–D4 |
| `08_ISP-R.txt` | Section 18 | Figures D1–D2 |
| `09_servers_and_printer_IP.md` | Section 18 | Figure 12, Figures D16–D20 |

---

## Service scripts – Task 2c

Services are configured before any restriction, so that every later fault can be traced to the change that caused it.

| Order | File | Device | Main configuration |
|---|---|---|---|
| 1 | [`01_servers_and_PCs.md`](service-scripts/01_servers_and_PCs.md) | Servers and PCs | DHCP pools, DNS records, web pages, FTP account; PCs set to DHCP |
| 2 | [`02_CORE-SW1.txt`](service-scripts/02_CORE-SW1.txt) | CORE-SW1 | DHCP relay, `FACULTY-IN` and `LAB-IN` ACLs, SSH |
| 3 | [`03_ACC-SW1.txt`](service-scripts/03_ACC-SW1.txt) | ACC-SW1 | Port security, PortFast, BPDU Guard, DHCP snooping, SSH |
| 4 | [`04_ACC-SW2.txt`](service-scripts/04_ACC-SW2.txt) | ACC-SW2 | As ACC-SW1, VLAN 20 |
| 5 | [`05_ACC-SW3.txt`](service-scripts/05_ACC-SW3.txt) | ACC-SW3 | As ACC-SW1, VLAN 30 |
| 6 | [`06_SRV-SW1.txt`](service-scripts/06_SRV-SW1.txt) | SRV-SW1 | Port security, PortFast, BPDU Guard, SSH |
| 7 | [`07_R1-EDGE.txt`](service-scripts/07_R1-EDGE.txt) | R1-EDGE | SSH from the Admin VLAN only |
| 8 | [`08_FW1.txt`](service-scripts/08_FW1.txt) | FW1 | HTTP inspection, added after the first internet web test failed |

| Script | Explained in report | Evidence |
|---|---|---|
| `01_servers_and_PCs.md` | Sections 21–23 | Figures 14–19, Figures E1–E3, E6 |
| `02_CORE-SW1.txt` | Sections 21, 24, 25 | Figures 15, 20–23, Figures E4–E5, E8 |
| `03`–`06` switches | Section 25 | Figure 24, Figure E7 |
| `07_R1-EDGE.txt` | Section 25 | – |
| `08_FW1.txt` | Section 26 | Figures 25–27 |

---

The passwords in these scripts exist only in the Packet Tracer simulation.
