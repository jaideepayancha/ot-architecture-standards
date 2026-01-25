# Network Redundancy Design

## Objectives

- No single point of failure for control traffic
- Maintenance without plant outage

## Cell/Area

- Ring topology using DLR or MRP
- Redundant uplinks to distribution switches

## Control & Site

- Dual core switches
- Redundant fiber paths

## Firewalls

- Active/Passive pairs
- State sync enabled

## DNS/DHCP

- Local plant servers
- No dependency on corporate WAN

## Failure Scenarios

| Failure | Expected Behavior |
|--------|------------------|
| Core switch | No PLC disruption |
| Firewall failover | Brief IT data pause only |
