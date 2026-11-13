# Device configurations

This folder holds the configuration of every network device in two forms.

| Folder | Contents |
|---|---|
| `install-scripts/` | The commands used to install the network in Task 2b (AC 3.2), one file per device, in the order they were applied |
| `running-configs/` | The final running configuration exported from each device with `show running-config` |

## Install scripts (Task 2b)

| Order | File | Device | Model |
|---|---|---|---|
| 1 | `01_ACC-SW1.txt` | Admin access switch | Cisco 2960-24TT |
| 2 | `02_ACC-SW2.txt` | Faculty access switch | Cisco 2960-24TT |
| 3 | `03_ACC-SW3.txt` | Computer lab access switch | Cisco 2960-24TT |
| 4 | `04_SRV-SW1.txt` | Server access switch | Cisco 2960-24TT |
| 5 | `05_CORE-SW1.txt` | Layer 3 core switch | Cisco 3560-24PS |
| 6 | `06_FW1.txt` | Firewall | Cisco ASA 5506-X |
| 7 | `07_R1-EDGE.txt` | Edge router with NAT | Cisco 2911 |
| 8 | `08_ISP-R.txt` | Simulated ISP router | Cisco 2911 |
| 9 | `09_servers_and_printer_IP.md` | Static addresses for the servers and PRN1 | – |

**How to use:** open the device in Cisco Packet Tracer, go to the **CLI** tab, press Enter and paste the whole file. Lines beginning with `!` are comments; if Packet Tracer reports `Invalid input` on one of them, it can be ignored. Each file ends with the `show` and `ping` commands used to verify that device.

The access switches are configured before the core so that each trunk is ready when the core side comes up, and the firewall, edge router and ISP follow from the inside outwards.

**Note:** the passwords in these scripts are lab passwords used only in the Packet Tracer simulation.

## Link to the Task 2b report

These scripts are the installation itself, so they produce the results shown in every Task 2b figure, not only one. Figure 4 (all 21 links up) is the overall result of running all eight scripts; the table below shows where each script is explained and where its results are evidenced.

| Script | Explained in report | Evidence (screenshots) |
|---|---|---|
| All eight scripts, basic setup block | Section 17 Basic Device Configuration | Figure 4 (all links up), Figure 5 (banner and password) |
| `01`–`04` access switches | Section 18 VLAN and Trunk Configuration | Figure 6, Figures D9–D15 |
| `05_CORE-SW1.txt` | Sections 18 and 19 | Figures 7, 8 and 11, Figures D6–D8 |
| `06_FW1.txt` | Section 19 Routing, NAT and Firewall | Figure 10, Figure D5 |
| `07_R1-EDGE.txt` | Section 19 Routing, NAT and Firewall | Figures 9 and 13, Figures D3–D4 |
| `08_ISP-R.txt` | Section 19 Routing, NAT and Firewall | Figures D1–D2 |
| `09_servers_and_printer_IP.md` | Section 19 (static addressing) | Figure 12, Figures D16–D20 |

The screenshots themselves are stored in `05-screenshots/task2b-installation/`, and Table 10 in Section 20 of the report summarises every check.

## Running configurations

Exported after Task 2c is complete. To export: open the device's **CLI** tab, run `terminal length 0` and then `show running-config`, and copy the output into `running-configs/<DEVICE>.txt`. On FW1, press Space at each `--More--` prompt.
