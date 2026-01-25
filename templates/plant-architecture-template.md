# Plant Architecture – <Plant Name>

## 1. Overview

- Plant Location:
- Production Areas:
- Criticality Level:

## 2. Network Architecture

![Plant Network](../diagrams/export/plant-network.png)

### VLANs

| Zone | VLAN | Purpose |
|--------|------|--------|
| Cell/Area | | PLCs, I/O |
| Control | | HMIs, SCADA |
| Site Ops | | Historians |
| DMZ | | Brokers, jump hosts |

## 3. Control Systems

### PLC Platforms

- Vendor:
- Firmware Standard:
- Redundancy:

### HMI / SCADA

- Ignition Version:
- Gateway Redundancy:
- Tag Providers:

## 4. Data Architecture

- MQTT Enabled: Yes / No
- Brokers:
- Store & Forward:
- Historian:

## 5. Cybersecurity

- Zones & Conduits aligned to IEC-62443
- Firewall Rules Approved:
- Remote Access Method:

## 6. Deviations from Standard

| Area | Deviation | Reason | Approved By |
|--------|--------|--------|-----------|

## 7. Risks & Mitigation

## 8. Approval

- OT Architect:
- IT Security:
- Operations:
