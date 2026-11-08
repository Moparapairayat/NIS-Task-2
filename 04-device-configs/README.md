# Device configurations

One text file per device, holding its final running configuration:

| File | Device |
|---|---|
| `ISP-R.txt` | Simulated ISP router (Cisco 2911) |
| `R1-EDGE.txt` | Edge router (Cisco 2911) |
| `FW1.txt` | Firewall (Cisco ASA 5506-X) |
| `CORE-SW1.txt` | Core Layer 3 switch (Cisco 3560-24PS) |
| `ACC-SW1.txt` | Administration access switch (Cisco 2960-24TT) |
| `ACC-SW2.txt` | Faculty access switch (Cisco 2960-24TT) |
| `ACC-SW3.txt` | Computer lab access switch (Cisco 2960-24TT) |
| `SRV-SW1.txt` | Server access switch (Cisco 2960-24TT) |

How to export: open the device in Packet Tracer, go to the **CLI** tab, run `show running-config`, then copy the output into the text file.
