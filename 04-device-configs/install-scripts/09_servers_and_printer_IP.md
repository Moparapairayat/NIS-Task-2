# Static IP settings for servers and the printer

These devices are not Cisco IOS devices, so their addresses are entered by hand rather than pasted as commands. Values come from Table 4 of the design document.

## Servers

Click the server, open **Desktop → IP Configuration**, choose **Static** and enter:

| Device | IPv4 Address | Subnet Mask | Default Gateway | DNS Server |
|---|---|---|---|---|
| SRV-DHCP-DNS | 192.168.40.10 | 255.255.255.0 | 192.168.40.1 | 192.168.40.10 |
| SRV-FILE | 192.168.40.20 | 255.255.255.0 | 192.168.40.1 | 192.168.40.10 |
| SRV-WEB | 192.168.40.30 | 255.255.255.0 | 192.168.40.1 | 192.168.40.10 |
| INTERNET-SRV | 198.51.100.10 | 255.255.255.0 | 198.51.100.1 | – |

## Printer (PRN1)

1. **Config → Settings:** Gateway `192.168.50.1`, DNS Server `192.168.40.10`
2. **Config → FastEthernet0:** Static, IPv4 Address `192.168.50.10`, Subnet Mask `255.255.255.0`

## Verification

- On each server: **Desktop → Command Prompt →** `ipconfig /all`
- From SRV-WEB: `ping 198.51.100.10` (end-to-end test through the firewall, NAT and the ISP)
