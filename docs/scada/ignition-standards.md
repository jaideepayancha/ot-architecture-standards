# Ignition System Architecture Standards

## Objectives

- High availability for critical visualization and data
- Standardized project structure
- Scalable plant and enterprise deployments

## Approved Architectures

### Small Sites

- Single Gateway (VM)
- Local Vision + Perspective
- Local Historian

### Medium / Large Sites

- Redundant Gateway Pair
- Separate Database Server
- Separate MQTT Broker

### Enterprise

- Central Enterprise Ignition
- Site collectors via MQTT or EAM

## Gateway Standards

- OS: Windows Server or RHEL
- CPU: Minimum 8 cores
- RAM: Minimum 32 GB
- SSD required

## Redundancy

- Use Ignition redundancy, not VM snapshots
- Gateways must be on separate hosts
- Independent power and switches

## Patch Management

- Quarterly Ignition upgrades
- Test in staging gateway first
