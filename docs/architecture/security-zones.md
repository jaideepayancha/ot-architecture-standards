# Security Zones & Conduits

Following the **ISA/IEC 62443** standard, our OT environment is divided into logical zones with defined conduits for communication.

## Zone Definitions

### 1. Process Zone (Level 0-1)
Contains the physical process equipment and controllers.
- **Assets**: PLCs, I/O, Drives, Sensors.
- **Security**: Physically secured, air-gapped or restricted to local HMI access.

### 2. Control Zone (Level 2)
Contains visualization and local supervisor systems.
- **Assets**: HMIs, SCADA Gateways, Engineering Workstations.
- **Security**: VLAN segmentation, application whitelisting.

### 3. Operations Zone (Level 3)
Site-wide systems for data aggregation and manufacturing execution.
- **Assets**: Historians, MES servers, Asset Management.
- **Security**: Domain-joined to local OT AD, restricted internet access.

### 4. Industrial DMZ (Level 3.5)
The buffer zone between OT and IT networks.
- **Assets**: MQTT Brokers, Jump Hosts, Proxy Servers.
- **Security**: No passthrough traffic; all data must terminate and restart in the DMZ.

---

## Conduit Standards

Conduits are the communication paths between zones. Each conduit must be:

1. **Documented**: Purpose, protocols, and port numbers.
2. **Authorized**: Approved through the Change Management process.
3. **Restricted**: Limited to the minimum necessary traffic (Least Privilege).

### Primary Conduits

| Source Zone | Destination Zone | Allowed Protocols | Purpose |
|-------------|------------------|-------------------|---------|
| Control (L2)| Operations (L3) | OPC UA, SQL | Data Logging |
| Operations (L3)| IDMZ (L3.5) | MQTTS (8883) | Cloud Ingestion |
| IT (L4) | IDMZ (L3.5) | RDP over TLS | Remote Support |

## Firewall Implementation

- **Deny All by Default**: Only explicitly allowed traffic is permitted.
- **Deep Packet Inspection (DPI)**: Used where possible for industrial protocols.
- **Logging**: All conduit traffic is logged to the enterprise SIEM.
