# MQTT & Sparkplug Standards

## Protocol

- MQTT v3.1.1 or v5
- Sparkplug B required for OT data

## Namespace Structure

Sparkplug standard:

spBv1.0/Group/MessageType/EdgeNode/Device

## Group ID

Plant code

Example:
spBv1.0/DANVILLE/DDATA/Edge01/PackingPLC1

## Birth & Death Certificates

- All nodes must publish BIRTH
- Death messages required for diagnostics

## QoS

| Data Type | QoS |
|--------|-----|
| Process | 0 or 1 |
| State | 1 |
| Commands | 1 |

## Retain

- Only for configuration topics
