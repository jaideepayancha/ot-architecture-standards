# ADR 0001: Use MQTT Sparkplug B for OT Data Transport

## Status
**Proposed**

## Context
Traditional OT data protocols (OPC UA, Modbus) are often "poll-response" based, which can saturate network bandwidth and lack efficient store-and-forward capabilities for unreliable WAN links. We need a modern, "publish-subscribe" protocol for cloud and enterprise ingestion.

## Decision
We will adopt **MQTT Sparkplug B** as the enterprise standard for all northbound OT data transport from Level 3/3.5 to Level 4/5.

## Rationale
1. **Report by Exception (RBE)**: Only changes data is sent, significantly reducing bandwidth usage.
2. **State Management**: The "Birth" and "Death" certificate mechanism allows subscribers to know the health of the connection to the field device.
3. **Implicit Data Modeling**: Sparkplug B provides a consistent payload format that includes metadata and units.
4. **Decoupling**: Multiple subscribers (MES, BI, Cloud) can consume data from a single broker without increasing load on the PLC or SCADA gateway.
5. **Security**: MQTT supports TLS/SSL encryption and certificate-based authentication.

## Consequences
- **Tooling**: All Edge Gateways must support Sparkplug B (e.g., Ignition Edge, Opto22, Telit).
- **Broker Infrastructure**: High-availability MQTT brokers (e.g., HiveMQ, EMQX) must be deployed in the IDMZ.
- **Legacy Systems**: Systems that do not support MQTT will require a gateway/bridge at Level 3.
