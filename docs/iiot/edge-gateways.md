# Edge Gateway Architecture

## Objectives

- Decouple PLC networks from IT/cloud
- Provide protocol normalization
- Enable store-and-forward buffering

## Approved Functions

Edge gateways may perform:

- OPC UA client/server
- Native PLC drivers
- MQTT publishing (Sparkplug B)
- Local buffering

## Prohibited

- Direct PLC writes from cloud
- Control logic execution
- Long-term storage

## Redundancy

- Dual gateways for critical lines
- Independent power and network

## Hardware

- Industrial PCs or embedded gateways
- SSD only
- Minimum 8 GB RAM
