# Network Reference Architecture

This architecture aligns to:

- Purdue Model (Levels 0–5)
- ISA-95
- IEC-62443 zones and conduits

## Objectives

- Protect control systems from enterprise threats
- Maintain deterministic control communications
- Enable secure data movement to IT and cloud

## High-Level Zones

| Purdue Level | Zone | Description |
|--------|--------|------------|
| L0/L1 | Cell/Area Zone | PLCs, drives, I/O |
| L2 | Control Zone | HMIs, SCADA nodes |
| L3 | Site Operations | Historians, batch, MES |
| L3.5 | Industrial DMZ | Brokers, patch servers |
| L4 | Enterprise IT | Corporate apps |
| L5 | Cloud | Analytics, AI, BI |

## Architecture Diagram

![Purdue Network](../../diagrams/export/purdue-networ)
