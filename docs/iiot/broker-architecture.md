# MQTT Broker Topology

## Site Level

- Local broker for control and buffering
- No dependency on WAN

## Enterprise Level

- Central broker cluster
- Subscribes to site brokers via bridge

## Cloud

- Cloud ingestion via DMZ services only

## Bridging Rules

- One-way OT → IT
- No cloud to PLC paths

## Redundancy

- Broker clustering at enterprise
- Local site broker single node acceptable
