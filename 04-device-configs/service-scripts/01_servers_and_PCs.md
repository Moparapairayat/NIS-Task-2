# Server services and PC settings (Task 2c, order 1 of 7)

These settings are made in the Packet Tracer GUI rather than the CLI. Apply them before the switch and router scripts, so that DHCP and DNS are already running when the clients ask for them.

## SRV-DHCP-DNS: DHCP (Section 21, Table 11)

**Services → DHCP → On.** Add one pool per user VLAN (type the values, then click **Add**):

| Pool name | Default Gateway | DNS Server | Start IP Address | Subnet Mask | Maximum Users |
|---|---|---|---|---|---|
| ADMIN-POOL | 192.168.10.1 | 192.168.40.10 | 192.168.10.10 | 255.255.255.0 | 90 |
| FACULTY-POOL | 192.168.20.1 | 192.168.40.10 | 192.168.20.10 | 255.255.255.0 | 90 |
| LAB-POOL | 192.168.30.1 | 192.168.40.10 | 192.168.30.10 | 255.255.255.0 | 90 |

## SRV-DHCP-DNS: DNS (Section 22, Table 12)

**Services → DNS → On.** Add these A records:

| Name | Type | Address |
|---|---|---|
| www.college.local | A Record | 192.168.40.30 |
| files.college.local | A Record | 192.168.40.20 |
| printer.college.local | A Record | 192.168.50.10 |
| www.internet.test | A Record | 198.51.100.10 |

## SRV-WEB: HTTP (Section 23)

**Services → HTTP:** HTTP On, HTTPS Off. Edit `index.html` so the page reads *Netron College Intranet – internal web server (SRV-WEB)*.

## SRV-FILE: FTP (Section 23)

**Services → FTP → On.** Delete the default `cisco` account and add `faculty` with password `Fac@2026` and Write, Read, Delete, Rename and List permissions. Turn HTTP off on this server.

## INTERNET-SRV: HTTP

Edit `index.html` so the page reads *External test website (simulated internet)*.

## PCs (all nine)

**Desktop → IP Configuration → DHCP.**
