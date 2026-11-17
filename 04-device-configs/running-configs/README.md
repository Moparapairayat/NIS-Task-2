# Running configurations

The final `show running-config` output of each network device, exported from [`NIS_Task2c_Services.pkt`](../../03-packet-tracer/NIS_Task2c_Services.pkt). Passwords appear only as hashes (`secret 5`) or type 7 encrypted strings.

| File | Device |
|---|---|
| `ISP-R.txt` | Simulated ISP router |
| `R1-EDGE.txt` | Edge router |
| `FW1.txt` | Firewall |
| `CORE-SW1.txt` | Layer 3 core switch |
| `ACC-SW1.txt` · `ACC-SW2.txt` · `ACC-SW3.txt` | Access switches |
| `SRV-SW1.txt` | Server access switch |

## How to export

1. Open the device's **CLI** tab and log in (`enable`, password `Netr0n@2026`).
2. Run `show running-config` and press Space at each `--More--` prompt.
3. Copy the output from `Building configuration...` to `end` into the file for that device.
