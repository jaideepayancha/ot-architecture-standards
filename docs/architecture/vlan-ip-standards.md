# VLAN and IP Addressing Standards

## VLAN Strategy

Each plant must implement:

| Zone | VLAN Range |
|--------|-----------|
| Cell/Area | 10xx |
| Control | 20xx |
| Site Ops | 30xx |
| DMZ | 40xx |
| IT | 50xx |

## IP Addressing

Private Class B preferred:

- 172.PLANT.ZONE.x

Example:

| Area | Subnet |
|--------|--------|
| Packaging PLCs | 172.20.10.0/24 |
| HMIs | 172.20.20.0/24 |
| Historians | 172.20.30.0/24 |

## Rules

- No DHCP for PLCs
- Reserved IP blocks for vendors
- Document all subnets in CMDB
