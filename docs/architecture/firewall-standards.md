# Firewall and Conduit Standards

## Zone Separation

Firewalls are mandatory between:

- Cell/Area → Control
- Control → Site Ops
- Site Ops → DMZ
- DMZ → IT

## Allowed Traffic Examples

| Source | Destination | Ports | Purpose |
|--------|------------|--------|--------|
| PLC | Ignition | TCP 44818 | EtherNet/IP |
| Edge | MQTT Broker | TCP 8883 | Secure MQTT |
| SCADA | Historian | TCP 1433 | SQL |

## Prohibited

- Any inbound IT → OT sessions
- Vendor VPN directly into control VLAN
- Internet access from PLC networks

## Inspection Mode

- No deep packet inspection on real-time protocols
- Avoid proxying OT traffic
